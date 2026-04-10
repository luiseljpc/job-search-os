**Application Workflow**

**Purpose**

This prompt runs the application workflow for a selected target
opportunity.

It should be used when the goal is to produce tailored application
materials quickly and cleanly.

This prompt does not own resume-tailoring logic, cover-letter voice
logic, or output schema logic. It must use those artifacts as the
authoritative sources.

**Operating context**

Use the following system artifacts as the operating context for this
task:

- Job Search OS Architecture

- Resume Routing Guide

- Resume Customization Rules

- Cover Letter Voice Guide

- Application Output Schema

- Candidate Evidence Pack

- the target job description

**Default invocation behavior**

This prompt should support short operator commands such as:

- Run application for \[company\]

- Run application for \[role\]

- Run application for \[company / role\]

Unless the user specifies otherwise, interpret these commands as
meaning:

- use the referenced selected opportunity as the target role

- read the full job description

- choose the best resume base using the Resume Routing Guide

- tailor the resume using the Resume Customization Rules

- write a cover letter when requested by the user or required by the
  active application task

- produce outputs in the exact structure required by the Application
  Output Schema

Reference resolution rules:

- if the user explicitly names a company or role, use that opportunity

- if the user refers to a role from a current results list, use that
  selected opportunity

- if the reference is ambiguous, ask the user for clarification before
  proceeding

- do not switch targets silently if the intended role is unclear

**Task**

Using the job description and the system artifacts above:

1.  choose the best resume base

2.  tailor the resume for the role

3.  write a tailored cover letter when needed

4.  produce outputs in the exact structure required by the Application
    Output Schema

**Required workflow**

**Step 1 --- Read the job description**

Extract the most important signals:

- function

- level

- required qualifications

- preferred qualifications

- business context

- domain signals

- work arrangement

- compensation if listed

- obvious strengths the employer is likely prioritizing

Also determine the main targeting emphasis for the application so the
output can include brief, useful Targeting Notes.

**Step 2 --- Choose the best resume base**

Use the Resume Routing Guide to determine whether the best base is:

- Master Resume

- Variant A

- Variant B

- Variant C

Do not guess ad hoc if the routing guide provides a clearer answer.

**Step 3 --- Tailor the resume**

Customize the selected resume base using the Resume Customization Rules.

Important:

- the final resume must be a full updated draft

- improve relevance without introducing unsupported claims

- strengthen the clearest truthful case for fit

- stay conservative with technical or domain inflation

**Step 4 --- Draft the cover letter**

When a cover letter is requested by the user or required by the active
application task, write it using the Cover Letter Voice Guide.

Important:

- keep the tone aligned with the guide

- ground the letter in real evidence

- do not repeat the resume mechanically

- make the strongest truthful case for candidacy

**Step 5 --- Surface residual risks / gaps**

Identify any meaningful remaining weaknesses, evidence gaps, or
unresolved mismatches that should still be visible after customization.

Keep this concise and useful.

Do not invent filler.

**Step 6 --- Format the output**

Produce the final result using the Application Output Schema exactly.

This includes, where relevant:

- Resume Base Used

- Targeting Notes

- Full Updated Resume Draft

- Optional Change Notes

- Cover Letter

- Residual Risks / Gaps

Do not substitute:

- step-by-step instructions for the full resume draft

- long explanations for usable outputs

Do not repeat the same point unnecessarily across Targeting Notes,
Optional Change Notes, and Residual Risks / Gaps.

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

Secondary support can sharpen language, but should not override stronger
evidence.

**Judgment rules**

- Be rigorous.

- Be truthful.

- Optimize for usable outputs.

- Do not overstate direct experience.

- Do not flatten the profile into generic corporate language.

- Preserve the strongest real differentiators where relevant.

- Keep the final materials role-specific, clear, and review-ready.
