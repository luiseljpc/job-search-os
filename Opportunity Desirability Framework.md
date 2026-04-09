**Opportunity Desirability Framework**

**Purpose**

This framework defines how attractive a job opportunity is based on the
candidate's current priorities.

It answers:

**How much do I want this role, independent of how well I match it?**

This framework is the single source of truth for:

- desirability sub-scores

- compensation attractiveness logic

- compensation thresholds / bands

- work arrangement attractiveness logic

- desirability confidence note

- desirability flag logic

- conservative handling of unknown desirability inputs

**Desirability dimensions**

Total Desirability Score = **10**

The score is composed of four sub-scores:

- Compensation Attractiveness = /3

- Work Arrangement Attractiveness = /2

- AI Relevance / AI Potential = /3

- Strategic Career Value = /2

**1. Compensation Attractiveness (/3)**

**Definition**

How attractive the role's compensation is relative to the candidate's
current priorities.

**Compensation bands**

- **3** = Excellent compensation

- **2** = Strong compensation

- **1** = Acceptable but not strong

- **0** = Weak compensation for current needs, or compensation is
  unknown with no strong offsetting signal

**Compensation thresholds**

Use these thresholds unless a later system revision explicitly changes
them:

- **Excellent (3)** = **\$200K+**

- **Strong (2)** = **\$150K--199K**

- **Decent (1)** = **\$125K--149K**

- **Weak (0)** = **Below \$125K**

- **Unknown (default 0 unless context clearly supports caution-adjusted
  interpretation)**

**Unknown compensation rule**

Do not assume missing compensation optimistically.

If compensation is not listed:

- treat it conservatively

- reduce confidence

- use an appropriate flag

If the role otherwise appears highly attractive, that can help
interpretation, but it should not turn unknown compensation into a
strong score.

**2. Work Arrangement Attractiveness (/2)**

**Definition**

How attractive the work arrangement is based on flexibility and real
location burden relative to the candidate's home base.

This document is the single source of truth for work arrangement
desirability logic.

**Standardized work arrangement categories**

Use one of the following:

- Remote

- Hybrid Local

- Onsite Local

- Hybrid Relocation

- Onsite Relocation

- Local

- Relocation Required

**Why both "Local / Relocation Required" and the more specific
categories exist**

When the JD clearly states **remote / hybrid / onsite**, preserve that
specificity.

When the JD gives **no work-mode indication whatsoever**, still classify
the practical location outcome:

- **Local** = based in the candidate's home metro area / reasonable
  commuting radius

- **Relocation Required** = based outside the candidate's home county
  reasonable driving range

This avoids forcing "Unknown" when the practical answer is still
obvious.

**Classification rules**

**A. If the JD explicitly states remote**

Classify as:

- **Remote**

**B. If the JD explicitly states hybrid**

Classify as:

- **Hybrid Local** if based in the candidate's home metro area /
  reasonable commuting radius

- **Hybrid Relocation** if based outside the candidate's home county
  reasonable driving range

**C. If the JD explicitly states onsite / in-office**

Classify as:

- **Onsite Local** if based in the candidate's home metro area /
  reasonable commuting radius

- **Onsite Relocation** if based outside the candidate's home county
  reasonable driving range

**D. If the JD gives no remote / hybrid / onsite indication**

Classify as:

- **Local** if based in the candidate's home metro area / reasonable
  commuting radius

- **Relocation Required** if based outside the candidate's home county
  reasonable driving range

**Reasonable driving distance rule**

Use practical common-sense commuting logic from the candidate's home
county.

Do not overcomplicate this.\
The point is to distinguish:

- realistic local opportunity\
  from

- role that effectively requires relocation or unsustainable commuting

**Scoring**

- **2.0** = Remote

- **1.5** = Hybrid Local

- **1.1** = Onsite Local

- **0.9** = Local

- **0.3** = Hybrid Relocation

- **0.3** = Relocation Required

- **0.1** = Onsite Relocation

**Interpretation rules**

- Remote is the most attractive arrangement.

- Hybrid Local is materially better than onsite local.

- Onsite Local can still be viable, but it is clearly less attractive
  than remote or local hybrid.

- Local is a fallback classification for postings with no mode
  specified; it should sit below explicitly favorable hybrid local and
  above relocation cases.

- Hybrid Relocation is generally weak because even partial in-person
  expectation outside the candidate's home county is operationally poor.

- Onsite Relocation is generally the least attractive arrangement
  because it combines maximum location burden with minimum flexibility.

- Relocation Required is used only when the posting gives no mode but
  the location is outside reasonable local range.

**Unknown work-arrangement rule**

Do **not** use "Unknown" as a standard category if the location still
allows a practical Local vs Relocation Required judgment.

Use an uncertainty flag instead when needed.

Examples:

- location known, mode unknown, based in Miami → classify **Local**

- location known, mode unknown, based in New York → classify
  **Relocation Required**

- location not clear enough to determine either mode or practical
  location burden → use the closest responsible classification and lower
  confidence with a flag

**3. AI Relevance / AI Potential (/3)**

**Definition**

How much the role is either explicitly AI-related or offers a credible,
role-specific opportunity to create meaningful leverage through AI.

**Scoring**

- **3** = Explicit AI

- **2** = Implicit but credible AI opportunity

- **1** = Light AI relevance

- **0** = Minimal or no meaningful AI relevance

**Interpretation rules**

A role should not receive a high AI score merely because AI could
theoretically be useful.

The case must be:

- credible

- role-specific

- materially relevant to the value of the role

**4. Strategic Career Value (/2)**

**Definition**

How much the role strengthens the candidate's long-term positioning,
proof, credibility, and future optionality.

**Scoring**

- **2** = Strongly advances long-term trajectory

- **1** = Directionally useful but not especially catalytic

- **0** = Mostly transactional or weak for future positioning

**High strategic value signals**

A role scores well here when it meaningfully strengthens one or more of:

- positioning as an AI-native strategist / operator

- exposure to AI-related work, tools, or workflows

- credibility in strategy, insights, innovation, research, or
  product-adjacent work

- future-facing resume proof

- proximity to important business problems

- optionality for stronger roles later

**Confidence Note**

Each desirability score must include a short audit note.

**Purpose**

To make the score easy to review later and easy to trust.

**Format**

A brief phrase, not a paragraph.

**Good examples**

- Strong comp, hybrid local, implicit AI, high future value

- Unknown comp, local, light AI relevance, medium strategic value

- Strong comp, onsite relocation, explicit AI, high upside

- Acceptable comp, remote, moderate AI potential, strong trajectory

**Unknown / Data Risk Flag**

Each desirability score must include a flag.

**Allowed values**

- None

- Comp Unknown

- Work Mode Unclear

- Location Burden Low Confidence

- AI Relevance Low Confidence

- Strategic Value Low Confidence

- Multiple Unknowns

**Rule**

Unknowns should be handled conservatively, not optimistically.

Use:

- **Work Mode Unclear** when the JD lacks explicit remote / hybrid /
  onsite language

- **Location Burden Low Confidence** when the location signal itself is
  ambiguous

- **Multiple Unknowns** when more than one important desirability input
  is unclear

**Summary formula**

**Desirability Score = Compensation (/3) + Work Arrangement (/2) + AI
Relevance (/3) + Strategic Career Value (/2)**

Maximum = **10**

**Practical scoring instruction**

When scoring desirability:

1.  score compensation using the thresholds above

2.  classify work arrangement using the standardized categories above

3.  score AI relevance

4.  score strategic career value

5.  add the total score out of 10

6.  write one short confidence note

7.  assign one flag

8.  score conservatively when key information is missing

**Final interpretation rule**

This framework measures how attractive the role is to pursue.

A role can be:

- high desirability but low fit

- high fit but low desirability

- high on both

- low on both

Do not let desirability substitute for fit, and do not let fit
substitute for desirability.
