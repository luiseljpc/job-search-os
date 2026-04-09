**Opportunity Evaluation Prompt**

**Purpose**

This prompt runs the opportunity evaluation workflow for one or more
already-selected job opportunities.

It should be used when the goal is to:

- identify whether a role is worth pursuing

- assess desirability and fit rigorously

- determine the right next move

- produce fast, scan-friendly output using the Opportunity Evaluation
  Table Schema

This prompt does **not** define the underlying scoring logic or
prioritization logic. It must use the relevant frameworks and schema as
the authoritative sources.

**Operating context**

Use the following system artifacts as the operating context for this
task:

- Job Search OS Architecture

- Role Target Framework

- Opportunity Desirability Framework

- Opportunity Fit Framework

- Opportunity Score Framework

- Opportunity Prioritization Framework

- Opportunity Evaluation Table Schema

- Resume Routing Guide

- Candidate Evidence Pack

**Task**

For each job opportunity provided:

1.  read the job description carefully

2.  score desirability using the Opportunity Desirability Framework

3.  score fit using the Opportunity Fit Framework

4.  calculate the final opportunity score using the Opportunity Score
    Framework

5.  determine the best next move, including the right resume base where
    relevant

6.  output the result using the exact Opportunity Evaluation Table
    Schema

If the input includes multiple opportunities, then after producing the
evaluation table, organize the evaluated opportunity set using the
Opportunity Prioritization Framework.

That prioritization layer should:

- group opportunities into the defined prioritization buckets

- allow overlap when justified by the framework

- highlight cross-bucket standouts after the bucketed view

**Required workflow**

**Step 1 --- Read the job description**

Extract and summarize the following as clearly as possible from the
posting:

- company

- title

- location

- work arrangement

- compensation

- key responsibilities

- required qualifications

- preferred qualifications

- signals about level, scope, stakeholders, and business context

Also generate:

- **Key Responsibilities** = one compact summary of the main work the
  role is responsible for

- **What the Company Likely Needs from This Role** = one short inference
  about the real business purpose of the role, based on the JD

Rules:

- keep both summaries concise

- ground both in the job description

- do not guess beyond what the posting reasonably supports

- do not paste or paraphrase large chunks of the JD

**Step 2 --- Confirm role context if needed**

Use prior discovery-stage role selection as the default source of
target-lane relevance.\
Only revisit Role Target Framework logic if the JD reveals the role was
misclassified during discovery or sits on a boundary between strong
match, adjacent plausible, and off-target.

**Step 3 --- Score desirability**

Use the Opportunity Desirability Framework as the single source of
truth.

This includes:

- compensation attractiveness

- work arrangement attractiveness

- AI relevance / AI potential

- strategic career value

- confidence note

- flag

Important:

- classify work arrangement carefully from the JD

- apply the desirability framework's work arrangement logic exactly

- apply the compensation logic exactly

- handle missing information conservatively

**Step 4 --- Score fit**

Use the Opportunity Fit Framework as the single source of truth.

This includes:

- functional match

- seniority match

- qualification match

- evidence strength

- Strong Match

- Gaps / Weak Areas

- Weakness Type

- Best Case for My Fit

- fit confidence note

- fit flag

- bucket classification

Also generate the schema-ready fit summaries:

- **Strong Match Areas** = a short phrase list capturing the clearest,
  most relevant alignment areas

- **Gaps / Weak Areas** = a short phrase list capturing the most
  meaningful visible limitations

Important:

- use the primary evidence base first

- distinguish true capability gaps from signaling gaps

- stay conservative where technical, functional, or level mismatch is
  central

- do not inflate fit for attractive roles

- do not invent weak areas for symmetry

- keep both summaries concise and decision-useful

**Step 5 --- Calculate opportunity score**

Use the Opportunity Score Framework to determine the final Opportunity
Score.

Do not invent a new combination method.

**Step 6 --- Determine next move**

Choose the most appropriate next move based on:

- overall opportunity score

- fit bucket

- desirability

- whether the role is worth tailoring for

- the best resume base according to the Resume Routing Guide

Use only the allowed Next Move values from the Opportunity Evaluation
Table Schema.

General rule:

- use **Submit \[Variant\]** when the existing variant is already strong
  enough

- use **Tailor \[Variant\]** when the opportunity is worth pursuing but
  would benefit from customization

- use **Skip** when the role is not a strong enough use of time

**Step 7 --- Output**

Produce the final result strictly in the format required by the
Opportunity Evaluation Table Schema.

Map the generated components into the schema fields, including:\
Key Responsibilities\
What the Company Likely Needs from This Role\
Strong Match Areas\
Gaps / Weak Areas

Do not add:\
extra columns\
extra commentary inside the table\
scoring explanations outside the fields\
long rationale paragraphs inside the table

Unless explicitly requested, the table should be optimized for fast
scanning and triage.

If the input includes multiple opportunities, then after the table,
generate a second section using the Opportunity Prioritization
Framework.

That section should be shown after the table and should use the
following structure:

**Opportunity Prioritization**

**Highest Excitement / Priority**

- Company --- Title

- Company --- Title

**Core Fit / Strong Pursue**

- Company --- Title

- Company --- Title

**Low-Hanging Fruit**

- Company --- Title

- Company --- Title

**AI Stretch but Plausible**

- Company --- Title

- Company --- Title

**High-Upside Stretch**

- Company --- Title

- Company --- Title

**Cross-Bucket Standouts**

**Appearing in 2 buckets**

- Company --- Title\
  Appears in: \[Bucket 1\]; \[Bucket 2\]

**Appearing in 3+ buckets**

- Company --- Title\
  Appears in: \[Bucket 1\]; \[Bucket 2\]; \[Bucket 3\]

Rules:\
organize the prioritization section by bucket, not by role\
a role may appear in more than one bucket if justified by the
Opportunity Prioritization Framework\
do not invent a new score or ranking formula\
do not treat overlap as its own bucket\
for single-role evaluations, omit the prioritization section unless
explicitly requested

**Evidence-use rules**

**Primary evidence**

Use these first:

- Resume Set

- Accomplishments Inventory

- Strengths and Capabilities Profile

- Differentiator Summary

**Secondary support**

Use these secondarily:

- Resume Routing Guide

- Positioning and Bullet Bank

Secondary support can help sharpen phrasing, but should not override
stronger factual evidence.

**Judgment rules**

- Be rigorous.

- Be conservative with unknowns.

- Do not confuse role attractiveness with real fit.

- Do not over-penalize presentational gaps when the underlying
  capability is strong.

- Do not smooth over major mismatches.

- Do not assume compensation, work arrangement, or scope if not
  supported by the JD.

- If uncertainty is material, reflect it through the relevant framework
  outputs.
