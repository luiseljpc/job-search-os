**Contact Prioritization Rules**

**Purpose**

This document defines how the AI should identify, classify, rank, and
select contacts for role-specific outreach once a job has been chosen as
worth pursuing.

The goal is to help prioritize the **highest-value outreach targets**
and avoid random or low-probability networking.

The workflow should answer:

- Who is most worth contacting for this job?

- What kind of contact is this person?

- Why are they relevant?

- In what order should they be messaged?

**Core principle**

Not all relevant contacts are equally useful.

The AI should prioritize contacts based on:

- likely influence on the hiring process

- proximity to the role or team

- relevance to the application

- plausibility of a useful response

- appropriateness of outreach

The AI should optimize for **strategic relevance**, not just proximity
on LinkedIn.

**Contact types**

The AI should classify contacts into the following categories:

**1. Recruiter at the company**

A recruiter or talent partner directly associated with the company,
function, or role family.

**2. Hiring Manager**

The person most likely to be managing the role, if reasonably inferable.

**3. Adjacent Leader**

A leader in the same function, team, or nearby organizational area who
is likely relevant to the role, even if not the direct hiring manager.

**4. Potential Teammate / Functional Peer**

Someone in a similar role, same team, or adjacent execution layer who
may provide insight or context.

**5. Warm / Semi-Warm Connection**

Someone connected through shared history, mutuals, prior company
overlap, alumni ties, or a plausible relationship bridge.

**6. Unclear / Low-Priority Contact**

A person who appears related to the company but whose relevance to the
role is weak, indirect, or uncertain.

**Priority ranking**

Default priority order:

1.  **Hiring Manager**

2.  **Recruiter at the company**

3.  **Warm / Semi-Warm Connection**

4.  **Adjacent Leader**

5.  **Potential Teammate / Functional Peer**

6.  **Unclear / Low-Priority Contact**

**Important adjustment rules**

The default ranking may be adjusted based on context.

**Move Recruiter above Hiring Manager when:**

- the hiring manager is not confidently identifiable

- the recruiter is clearly tied to the role or function

- the role appears to be run through recruiting first

- direct manager outreach would be too speculative

**Move Warm / Semi-Warm Connection up when:**

- the connection is genuinely usable

- they can plausibly refer, advise, or route the application

- they have meaningful proximity to the team or hiring process

**Move Adjacent Leader up when:**

- the role is senior or strategic

- the team structure is visible

- the adjacent leader appears more findable or relevant than the
  recruiter

- outreach to a peer would be too low leverage

**Move Potential Teammate / Functional Peer up when:**

- the goal is insight rather than advocacy

- the hiring path is opaque

- a short informational message could improve application quality

**Relevance test**

A contact should only be included if there is a credible reason they
matter for this role.

Good reasons:

- direct responsibility for hiring or recruiting

- leadership in the relevant function

- likely team proximity

- plausible ability to provide context, signal, or referral

- warm-connection relevance

Weak reasons:

- they work at the company but far from the function

- title sounds senior but irrelevant

- vague assumption they "might help"

- no visible connection to the role, team, or hiring path

**Contact selection rules**

For a chosen job, the AI should aim to return a **small, high-quality
list**, not an exhaustive dump.

Recommended output target:

- **3 to 6 contacts total**

- ideally covering more than one contact type when possible

The AI should avoid flooding the user with too many low-confidence
names.

**Confidence handling**

The AI should distinguish between:

- confidently relevant contacts

- plausibly relevant contacts

- weakly inferred contacts

If the hiring manager is not clearly identifiable, the AI should say so
rather than pretending certainty.

Examples:

- **Likely recruiter**

- **Possible hiring manager**

- **Adjacent leader, moderate confidence**

- **Peer contact, lower priority**

**Contact priority field**

Each contact should receive a priority label:

- **High Priority**

- **Medium Priority**

- **Low Priority**

**High Priority**

Directly relevant, likely worth messaging first.

**Medium Priority**

Relevant enough to contact after primary targets, or useful for insight.

**Low Priority**

Only worth contacting if better options are unavailable.

**Output fields**

For each contact, the outreach workflow should ideally return:

- Name

- Title

- Company

- Contact Type

- Priority

- Why this person is relevant

- Confidence level

- Suggested outreach angle

- Preferred Contact Channel / Link

**What the AI should not do**

The AI must not:

- pretend to know the hiring manager without reasonable evidence

- include random employees just because they work there

- confuse company prestige with outreach relevance

- overproduce low-value contacts

- treat all connections as equal

The point is not to maximize names.\
The point is to maximize useful outreach targets.

**Governing principle**

For each job, the AI should identify the **smallest set of people most
likely to improve the application odds, information quality, or
visibility of the candidacy.**
