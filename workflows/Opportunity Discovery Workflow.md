**Opportunity Discovery Workflow**

**Purpose**

This document governs how the system **discovers, filters, prioritizes,
and selects public job opportunities** before formal evaluation.

It should be used when the goal is to:

- discover relevant current public job opportunities

- prioritize the strongest opportunities first

- select the best opportunity set for downstream review

- hand the selected opportunity set into the **Opportunity Evaluation
  workflow**

- return fast, scan-friendly final output using the **Opportunity
  Evaluation Table Schema**

This document is the authoritative source for:

- discovery preference logic

- discovery workflow sequence

- default discovery invocation behavior

- discovery-stage selection rules

- handoff into the Opportunity Evaluation workflow

It does **not** define:

- target-lane logic

- evaluation scoring logic

- application-generation logic

- outreach-generation logic

- output schema rules beyond discovery-stage output behavior

**Role in the system**

Use this document during the **Opportunity Discovery** stage.

Use it to determine:

- which listings should be prioritized first

- which listings should be included or excluded when the pool is large

- how to rank opportunities before formal evaluation

- how to resolve tradeoffs between otherwise relevant opportunities

- how to interpret short operator commands for discovery

- how to hand the selected opportunity set into the Opportunity
  Evaluation workflow

Do **not** use this document to define:

- fit scoring

- desirability scoring

- opportunity score calculation

- application generation

- outreach generation

**Operating context**

Use the following system artifacts as the operating context for this
task:

- **Job Search OS Architecture**

- **Role Target Framework**

- **Opportunity Evaluation Prompt**

- **Opportunity Evaluation Table Schema**

**Default invocation behavior**

This workflow should support short operator commands such as:

- **Discover 20 opportunities**

- **Discover 50 opportunities**

- **Discover opportunities**

Unless the user specifies otherwise, interpret these commands as
meaning:

1.  search for current public job listings relevant under the **Role
    Target Framework**

2.  apply the discovery preferences in this document to prioritize and
    select the opportunity set

3.  run the **Opportunity Evaluation Prompt** exactly as written on all
    selected roles

4.  return only the final table in the exact **Opportunity Evaluation
    Table Schema**

Rules:

- if the user specifies a number, use that number

- if the user does not specify a number, default to **20 opportunities**

**Stable discovery preferences**

**1. Role relevance priority**

Prioritize roles in this order:

1.  strong matches within the target lanes defined by the **Role Target
    Framework**

2.  adjacent but plausible roles that still make strategic sense

3.  lower-priority edge cases only if needed to fill the requested
    volume

**General rule:\**
Prefer quality of fit over novelty. Do not include weakly related roles
merely to increase count if better-aligned roles are available.

**2. Location priority**

Prioritize opportunities in this order:

1.  remote roles

2.  roles located in Miami, Miami Beach, Fort Lauderdale, or within
    reasonable driving distance of Miami Beach

3.  other roles only if they are unusually strong and worth surfacing
    despite location disadvantage

**General rule:\**
Remote-first is the default search posture. Local South Florida roles
are second priority. Non-local, non-remote roles should clear a
meaningfully higher relevance bar to enter the selected set.

**3. Source-quality priority**

Prioritize listings from higher-quality sources first.

Prefer, where possible:

1.  official company career pages

2.  well-maintained employer ATS pages

3.  high-quality aggregators that link clearly to current public
    listings

4.  other public sources only when necessary

**General rule:\**
Prefer reliable, current, directly verifiable listings over noisy or
duplicative aggregator results.

**4. Freshness priority**

Prefer current listings.

**General rule:\**
Prioritize recent, still-open public listings. Avoid stale, unclear, or
likely inactive roles when stronger current alternatives are available.
If posting freshness is uncertain, prefer sources that indicate the
listing is still active.

**5. Match-ordering priority**

When building the selected opportunity set, prioritize in this order:

1.  strong matches first

2.  adjacent but plausible roles second

Do not let adjacent roles crowd out clearly stronger opportunities.

**General rule:\**
Adjacent roles are useful for widening the funnel, but they should not
dominate the shortlist when strong direct-fit roles exist.

**Inclusion rules**

Include roles when they are:

- clearly aligned with the **Role Target Framework**

- adjacent but plausible in a strategically credible way

- publicly listed and currently active to the best available evidence

- strong enough to justify evaluation time

Exclude roles when they are:

- clearly off-target

- too senior, too junior, or too functionally mismatched without a
  credible bridge

- stale, duplicative, or low-confidence listings

- weak enough that they are unlikely to be a good use of evaluation time

**Duplicate-handling rules**

When the same role appears in multiple places:

- prefer the official company or ATS source

- retain only one version of the listing in the selected set

- avoid evaluating duplicate postings separately

When near-duplicates appear across locations, business units, or
reposts, use judgment to decide whether they are materially distinct
opportunities.

If not materially distinct, keep only the best version.

**Tradeoff rules**

If the discovery pool is larger than the requested number of
opportunities, break ties in this order:

1.  stronger role relevance

2.  better location alignment

3.  higher source quality

4.  higher freshness / confidence that the listing is active

5.  stronger apparent strategic value

**General rule:\**
The selected set should skew toward the best real opportunities, not
merely the easiest ones to find.

**Volume rule**

If the requested number of opportunities cannot be filled entirely with
strong direct matches:

1.  first expand into adjacent but plausible roles

2.  only then widen further, while staying within reasonable strategic
    credibility

Do not quietly degrade standards without signaling it through the
composition of the set.

**Task**

For each discovery run:

1.  search for current public job listings that are relevant under the
    **Role Target Framework**

2.  prioritize them using the discovery preferences in this document

3.  select the requested number of opportunities

4.  run the **Opportunity Evaluation Prompt** exactly as written for all
    selected roles

5.  return only the final table in the exact **Opportunity Evaluation
    Table Schema**

**Required workflow**

**Step 1 --- Interpret the request**

Determine:

- the requested number of opportunities

- whether the user specified any additional discovery constraints

- whether the user is invoking the workflow through a short operator
  command or a longer instruction

**Default rules:**

- if no number is given, use **20**

- if no extra constraints are given, use the default discovery behavior
  defined in this document

- treat a short command such as **"Discover 20 opportunities"** as
  sufficient instruction to run the full discovery-and-evaluation
  workflow

**Step 2 --- Search for opportunities**

Search for current public job listings using the **Role Target
Framework** as the authoritative source for what kinds of roles belong
in the funnel.

During search:

- seek strong-match roles first

- include adjacent but plausible roles second when needed

- prefer high-quality, current, publicly accessible listings

- avoid obvious duplicates, stale listings, or weakly related roles

**Step 3 --- Prioritize and select the opportunity set**

Use the **stable discovery preferences in this document** as the single
source of truth for discovery prioritization.

This includes:

- role relevance priority

- location priority

- source-quality priority

- freshness priority

- strong-match-first vs adjacent-plausible-second ordering

- duplicate-handling rules

- tradeoff rules

Select the final set according to the requested volume.

**General rule:\**
Prefer the best real opportunities, not merely the easiest ones to find.

**Step 4 --- Prepare selected roles for evaluation**

For each selected opportunity, retain:

- the job title

- the company name

- the job location

- the job posting source

- the job description or sufficient posting content needed for
  evaluation

Only pass forward roles with enough information to support meaningful
evaluation.

**Step 5 --- Hand off to evaluation**

Run the **Opportunity Evaluation Prompt** exactly as written for all
selected roles.

Do not:

- replace the evaluation logic

- compress the evaluation logic

- override the evaluation logic

- invent a parallel evaluation method

- skip the evaluation stage

**Step 6 --- Output**

Return only the final table in the exact **Opportunity Evaluation Table
Schema**.

Do not add:

- preambles

- search summaries

- sourcing notes

- extra commentary

- explanations outside the schema

- separate discovery-stage tables

Unless explicitly requested, discovery work should remain invisible in
the final output and should only affect which roles enter evaluation.

**Selection rules**

- prioritize strong direct-fit roles first

- use adjacent but plausible roles to widen the funnel only when needed

- do not include clearly off-target roles simply to hit the requested
  count

- do not evaluate duplicate versions of the same listing

- prefer official or high-confidence sources when multiple versions
  exist

- prefer listings with enough detail to support rigorous downstream
  evaluation

**Judgment rules**

- Be selective.

- Be practical.

- Do not confuse volume with quality.

- Do not quietly degrade standards just to fill the list.

- Do not let attractive but weakly aligned roles dominate the selected
  set.

- Do not bypass the Opportunity Evaluation workflow.

- If the discovery pool is thinner than the requested number, widen
  carefully and only within reasonable strategic credibility.

- Do not confuse discoverability with desirability.

- Do not confuse role attractiveness with real fit.

- Prefer real opportunity quality over list-filling behavior.

- Prefer credible, current, high-signal listings.

- Do not over-expand into adjacent roles too early.

**Output rule**

The final deliverable for this workflow is the **evaluated opportunity
table**, not a discovery memo.

The user should be able to invoke this workflow with a short command and
still receive:

- discovered opportunities

- evaluated opportunities

- final table output

without restating the full workflow each time.
