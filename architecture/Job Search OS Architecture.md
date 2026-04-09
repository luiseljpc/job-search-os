**Job Search OS Architecture**

**Purpose**

This document is the master architecture and governance document for the
job search system.

It defines:

- the system's purpose

- the major document layers

- the role of each retained artifact

- document-type responsibilities

- precedence rules

- conflict-resolution rules

- how workflows should use the system

It does not define detailed scoring rules, detailed workflow steps, or
output schemas.

**System purpose**

This system exists to help me:

- discover the right opportunities

- evaluate those opportunities quickly and rigorously

- prioritize evaluated opportunities into an actionable starting order

- assess real candidate fit without distortion

- route to the right resume base

- generate strong, low-friction application materials

- maintain a modular foundation for future workflows such as outreach,
  networking, interview prep, and offer comparison

The system is designed for:

- speed

- consistency

- auditability

- maintainability

- truthful but strong positioning

**Document types and responsibilities**

**1) Architecture documents**

Architecture documents define:

- the system structure

- layer boundaries

- document roles

- precedence rules

- governance rules

They do not define detailed scoring logic, detailed workflow steps, or
output field specifications.

**2) Framework and rules documents define:**

- scoring logic

- classification logic

- judgment criteria

- prioritization logic

- confidence-note rules

- flag rules

- interpretation rules

**3) Workflow prompt documents**

Workflow prompts define:

- the sequence of work

- required inputs

- artifact consultation order

- what to produce

They do not re-own scoring logic, tailoring logic, or schema logic that
already exists elsewhere.

**4) Schema documents**

Schema documents define only:

- fields

- order

- allowed values

- formatting rules

- length constraints

They do not behave like mini-prompts.

**5) Evidence documents**

Evidence documents define:

- the candidate's actual background

- accomplishments

- proof

- strengths

- differentiators

- current resume assets

They do not define system logic.

**6) Voice / style documents**

Voice / style documents define:

- tone

- rhetorical posture

- writing constraints

They do not define workflow, scoring, or schema structure.

**System layers**

**Layer 1 --- Opportunity Discovery and Evaluation**

This layer determines:

- which public roles should enter the funnel

- which roles best match target lanes

- how opportunities should be prioritized before review

- how desirable each shortlisted role is

- how well I fit it

- the final opportunity score

- the right immediate next move

- how evaluated opportunities should be grouped into actionable pursuit
  buckets

**Layer 1A --- Opportunity Discovery**

This sublayer governs how the system finds and selects opportunities
before formal evaluation.

Documents in this sublayer

**Role Target Framework\**
Defines the role categories, target lanes, target tiers, and in-bounds
vs adjacent-plausible search logic.

**Opportunity Discovery Workflow\**
Defines how the system discovers, filters, prioritizes, and selects
public job opportunities before formal evaluation.\
This document is the single source of truth for:

- discovery preference logic

- discovery workflow sequence

- default discovery invocation behavior

- discovery-stage selection rules

- handoff into the Opportunity Evaluation workflow

**Layer 1B --- Opportunity Evaluation**

This sublayer governs how selected opportunities are assessed once they
have entered the funnel.

Documents in this sublayer

**Opportunity Desirability Framework\**
Defines desirability scoring logic.

This document is the single source of truth for:

- compensation attractiveness

- compensation thresholds / bands

- unknown-compensation handling

- work arrangement attractiveness

- desirability confidence note

- desirability flag logic

**Opportunity Fit Framework\**
Defines fit scoring logic.

This document is the single source of truth for:

- fit sub-scores

- Best Case for My Fit

- fit confidence note

- fit flag logic

- bucket classification

**Opportunity Score Framework\**
Defines how fit and desirability combine into the final opportunity
score.

**Opportunity Prioritization Framework\**
Defines how evaluated opportunity sets are organized into
action-oriented pursuit buckets after evaluation.

This document is the single source of truth for:

- prioritization bucket definitions

- bucket-placement rules

- overlap rules

- cross-bucket-standout rules

- prioritization output structure

**Opportunity Evaluation Prompt\**
Defines the sequence for evaluating one or more selected opportunities.

**Opportunity Evaluation Table Schema\**
Defines the output row contract for opportunity evaluation.

**Layer 2 --- Candidate Evidence Pack**

This layer defines the candidate truth base.

**Documents in this layer**

**Resume Routing Guide\**
Determines which resume variant is the best base for a given role.

**Strengths and Capabilities Profile\**
Summarizes durable strengths and repeated areas of value.

**Positioning and Bullet Bank\**
Provides reusable language support and embedded public-narrative /
LinkedIn About Me language.

Use as support, not as primary evidence unless corroborated elsewhere.

**Accomplishments Inventory\**
Provides proof of outcomes, achievements, and value creation.

**Differentiator Summary\**
Defines what makes the profile distinctively valuable.

**Resume Variant A\**
Strategic insights / consumer strategy lane.

**Resume Variant B\**
Innovation / research / capability-building lane.

**Resume Variant C\**
AI-adjacent / future-facing / operator-relevant lane.

**Master Resume\**
Comprehensive evidence reference.

**Layer 3 --- Application Workflow**

This layer turns a selected target opportunity into strong application
materials.

**Documents in this layer**

**Application Workflow Prompt\**
Defines the orchestration sequence for application generation.

**Resume Customization Rules\**
Defines resume-tailoring logic and guardrails.

**Cover Letter Voice Guide\**
Defines tone and style for cover letters.

**Application Output Schema\**
Defines the output contract for the application workflow.

**Layer 4 --- Outreach and Networking**

This layer supports role-specific contact identification, outreach
prioritization, and generation of concise outreach messages.

**Documents in this layer**

**Contact Prioritization Rules\**
Defines how contacts should be identified, classified, ranked, and
selected for outreach once a role has been chosen.

**Outreach Voice Guide\**
Defines the writing voice and style for LinkedIn or email outreach so
messages feel concise, relevant, and natural to Luis.

**Outreach Workflow Prompt\**
Defines the workflow for identifying relevant contacts, prioritizing
them, and generating tailored outreach messages for a selected role.

**Authoritative use**

Use these files when a role has already been selected for pursuit.

Use them to:

- identify the best people to contact

- determine the right outreach angle

- generate concise, role-specific messages

**Ownership rules**

**Role targeting logic**

Owned only by the **Role Target Framework**.

This includes:

- target role lanes

- target tiers

- in-bounds vs adjacent-plausible classification

- role-category relevance

- what kinds of roles should enter the search funnel

**Opportunity discovery logic**

Owned only by the **Opportunity Discovery Workflow**.

This includes:

- discovery preference logic

- search sequence

- sourcing steps

- shortlist construction

- strong-match-first vs adjacent-plausible-second ordering

- location priority

- remote vs local priority

- source-quality preference

- current-public-listing preference

- deduping / stale-listing rules

- other stable discovery priorities

- handoff into the Opportunity Evaluation workflow

- discovery-stage output instructions

- default short-command invocation behavior

**Opportunity desirability logic**

Owned only by the **Opportunity Desirability Framework**.

This includes:

- compensation attractiveness

- compensation thresholds / bands

- unknown-compensation handling

- work arrangement attractiveness

- AI relevance / AI potential

- strategic career value

- desirability confidence note

- desirability flags

**Opportunity fit logic**

Owned only by the **Opportunity Fit Framework**.

This includes:

- functional match

- seniority match

- qualification match

- evidence strength

- Best Case for My Fit

- fit confidence note

- fit flags

- bucket classification

**Opportunity prioritization logic**

Owned only by the Opportunity Prioritization Framework.

This includes:

- prioritization bucket definitions

- criteria for Highest Excitement / Priority

- criteria for Core Fit / Strong Pursue

- criteria for Low-Hanging Fruit

- criteria for AI Stretch but Plausible

- criteria for High-Upside Stretch

- overlap rules

- cross-bucket-standout logic

- post-evaluation prioritization structure

**Work arrangement logic**

Owned only by the **Opportunity Desirability Framework**.

The evaluation prompt may instruct the system to extract work
arrangement carefully, and the schema may include a Work Arrangement
field, but the logic for how work arrangement affects judgment lives
only in the desirability framework.

**Compensation logic**

Owned only by the **Opportunity Desirability Framework**.

The evaluation prompt may instruct the system to extract compensation
carefully, and the schema may include a Compensation field, but the
logic for how compensation affects judgment lives only in the
desirability framework.

**Resume routing logic**

Owned only by the **Resume Routing Guide**.

**Resume tailoring logic**

Owned only by the **Resume Customization Rules**.

**Cover letter tone logic**

Owned only by the **Cover Letter Voice Guide**.

**Output field logic**

Owned only by the relevant schema document.

**Workflow relationships**

**Opportunity discovery workflow**

Use the system in this order:

- search current public job listings

- use the Role Target Framework to determine which roles are
  meaningfully in-bounds or adjacent but plausible

- use the Opportunity Discovery Workflow to apply discovery preferences,
  prioritize the pool, and select the final opportunity set

- hand the selected roles into the Opportunity Evaluation Prompt

- output the results using the Opportunity Evaluation Table Schema

**Opportunity evaluation workflow**

Use the system in this order:

- read the job description

- use the Opportunity Desirability Framework to score desirability

- use the Opportunity Fit Framework to score fit

- use the Opportunity Score Framework to calculate the final opportunity
  score

- use the Resume Routing Guide to identify the best resume base for the
  recommendation

- output the result using the Opportunity Evaluation Table Schema

- for batch opportunity sets, use the Opportunity Prioritization
  Framework to organize the evaluated set into pursuit buckets and
  identify cross-bucket standouts

**Application workflow**

Use the system in this order:

- Read the job description

- Use the Resume Routing Guide to choose the best resume base

- Customize the resume using the Resume Customization Rules

- Write the cover letter using the Cover Letter Voice Guide

- Format all outputs according to the Application Output Schema

**Outreach workflow**

Use the system in this order:

- Read the job description

- Identify likely relevant contacts using the Contact Prioritization
  Rules

- Determine the best outreach angle for each contact

- Generate messages using the Outreach Voice Guide

- Format outputs according to the Outreach Workflow Prompt

**Evidence hierarchy**

When assessing fit or customizing materials, use this evidence priority:

**Primary evidence**

- Resume Variant(s)

- Master Resume

- Accomplishments Inventory

- Strengths and Capabilities Profile

- Differentiator Summary

**Secondary support**

- Resume Routing Guide

- Positioning and Bullet Bank (including embedded Public Narrative /
  LinkedIn About Me language)

Secondary support can help clarify or strengthen phrasing, but it should
not override stronger factual evidence.

**Conflict-resolution rules**

If artifacts overlap or appear to conflict, apply these rules:

1.  The most specific document that legitimately owns the logic wins.

2.  Evidence documents outweigh positioning language.

3.  Framework documents outweigh workflow prompts on
    scoring/classification logic.

4.  Schema documents outweigh workflow prompts on output formatting.

5.  Routing guide outweighs ad hoc resume-variant guessing.

6.  If uncertainty remains, state it explicitly rather than smoothing it
    over.

**Operating principles**

- Be truthful.

- Be conservative with unknowns.

- Distinguish real capability gaps from signaling gaps.

- Do not overstate technical or domain experience.

- Do not underrate transferable strategic and research strengths.

- Optimize for decision quality and execution quality, not verbosity.

- Keep the system modular so new workflow layers can be added cleanly
  later.
