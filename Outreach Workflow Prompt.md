**Outreach Workflow Prompt**

**Purpose**

This prompt runs the outreach workflow for a selected target
opportunity.

The goal is to help the user quickly identify the best people to contact
and generate concise, relevant LinkedIn messages grounded in the actual
role, the contact type, and the user's candidacy.

This workflow should produce:

- a small, high-quality list of relevant contacts

- contact classification and prioritization

- a short explanation of why each person matters

- a tailored LinkedIn message for each contact

The workflow should optimize for relevance, plausibility, and
low-friction execution.

**Required operating context\**
Use the following system artifacts and target-role context as the
operating context for this workflow:

**System / workflow context**

- Job Search OS Architecture

- full job description provided in the chat

- company name and role, if separately provided

**Opportunity / evaluation context**

- Role Target Framework, if useful

- Opportunity Evaluation outputs, if already generated for this role

**Candidate context**

- Candidate Evidence Pack

- selected resume variant, if already known

- Differentiator Summary

- Strengths and Capabilities Profile

- Accomplishments Inventory

- Positioning and Bullet Bank

**Outreach context**

- Contact Prioritization Rules

- Outreach Voice Guide

**Default invocation behavior**

This prompt should support short operator commands such as:

- Run outreach for \[company\]

- Run outreach for \[role\]

- Run outreach for \[company / role\]

Unless the user specifies otherwise, interpret these commands as
meaning:

- use the referenced selected opportunity as the target role

- read the full job description

- identify the most relevant contacts using the Contact Prioritization
  Rules

- prioritize the strongest and most plausible outreach targets

- determine the best outreach angle for each contact

- generate concise, role-specific outreach messages using the Outreach
  Voice Guide

- return the output in the structure required by this workflow

Reference resolution rules:

- if the user explicitly names a company or role, use that opportunity

- if the user refers to a role from a current results list, use that
  selected opportunity

- if the reference is ambiguous, ask the user for clarification before
  proceeding

**Workflow objective**

For a given job opportunity, the AI should:

- identify the most relevant people to contact

- classify each person by contact type

- prioritize the best outreach targets

- explain briefly why each person is relevant

- generate short, role-specific LinkedIn outreach messages in Luis's
  voice

**Required workflow**

**1. Read the full job description carefully**

The AI should use the full JD, not just a summary row.

It should identify:

- the likely function and team context of the role

- the kinds of people most likely to matter for this opening

- whether outreach should focus more on recruiting, leadership, peer
  insight, or connection-routing

This step should remain internal unless useful to surface briefly later.

**2. Identify likely relevant contacts**

Using available public information, the AI should identify a small set
of contacts plausibly relevant to the role.

Target contact types:

- Recruiter at the company

- Hiring Manager

- Adjacent Leader

- Potential Teammate / Functional Peer

- Warm / Semi-Warm Connection

- Unclear / Low-Priority Contact only if necessary

The AI should prioritize quality over quantity.

Recommended total:

- 3 to 6 contacts

- enough to give options, but not so many that the list becomes noisy

**3. Classify and prioritize contacts**

The AI should classify each contact using the Contact Prioritization
Rules.

For each contact, determine:

- Contact Type

- Priority (High / Medium / Low)

- Confidence level

- Why this person is relevant

The AI should not pretend certainty when the role relationship is
unclear.

If the hiring manager cannot be identified with reasonable confidence,
say so.

**4. Determine the right outreach angle**

For each contact, the AI should determine the most appropriate outreach
purpose.

Examples:

- recruiter: signal fit and interest in the role

- hiring manager: connect candidacy to role needs

- adjacent leader: show role-relevant alignment and intelligent interest

- peer: ask for light insight, not heavy advocacy

- warm connection: make the relationship bridge explicit but restrained

The outreach angle should fit both:

- the contact type

- the strength of Luis's likely candidacy for the role

**5. Generate the message**

The AI should generate a short LinkedIn message for each contact using
the Outreach Voice Guide.

The message should be:

- concise

- relevant

- role-specific

- tailored to the contact type

- grounded in Luis's actual background

- easy to send without embarrassment

The AI should avoid:

- generic networking language

- overlong explanations

- heavy asks

- flattery

- fake familiarity

- sounding needy or overeager

**Required output**

When running this workflow, the AI should return the following sections
in order:

**Section 1 --- Outreach Strategy**

Provide very brief bullets for:

- primary outreach goal for this role

- who should be prioritized first

- what kind of outreach angle is strongest

- any caution or constraint

Keep this section short.

**Section 2 --- Recommended Contacts**

Provide a compact table with these columns:

- Name

- Title

- Contact Type

- Priority

- Confidence

- Why Relevant

- Preferred Contact Channel / Link

Rules:

- keep "Why Relevant" very short

- list the contacts in priority order

- include only the strongest and most plausible contacts

**Section 3 --- Message Drafts**

For each recommended contact, provide:

- Contact Name

- Contact Type

- Outreach Angle

- Message Draft

Rules:

- keep each message concise

- adapt to contact type

- make each message genuinely relevant

- do not make all messages sound interchangeable

**Section 4 --- Best First Moves**

Provide:

- who to message first

- who to message second if needed

- who is optional / lower priority

- any note on sequencing

Keep this short and practical.

**Required operating rules**

The AI must follow these rules when running the workflow:

- use the actual JD as the basis for outreach relevance

- prioritize the smallest set of people most likely to improve
  application odds, information quality, or visibility

- do not include random employees just because they work at the company

- do not pretend to know the hiring manager without reasonable evidence

- distinguish clearly between confident and lower-confidence inferences

- adapt the outreach angle to the contact type

- keep messages concise and low-friction

- ground the messages in Luis's actual profile and the role context

- do not invent connections, shared history, or familiarity

- do not make heavy asks in the first outreach message

- optimize for usefulness, plausibility, and ease of sending

- prefer LinkedIn as the default outreach channel

- use email only if LinkedIn is not available or not reasonably findable

- if email is used as fallback, keep the message similarly concise and
  adapt only the greeting and close as needed
