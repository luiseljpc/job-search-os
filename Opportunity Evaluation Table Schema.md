**Opportunity Evaluation Table Schema**

**Purpose**

This schema defines the exact output contract for the evaluation table
used in opportunity evaluation.

It is designed for fast job triage.

It defines only:

- fields

- order

- allowed values

- formatting rules

- length constraints

For batch opportunity sets, the workflow may append a separate
post-table prioritization section governed by the Opportunity
Prioritization Framework. That section is not part of the row schema
defined here.

It does **not** define scoring logic or mini-prompt instructions.

**Output rules**

This schema governs the evaluation table only, not any post-table
prioritization section.

- One row per opportunity

- Keep rows scan-friendly

- No long paragraphs

- No pasted JD text

- No extra fields

- No extra commentary unless requested

- Use Unknown only when needed and supported by the relevant framework
  logic

**Column order**

1.  URL

2.  Opportunity Score (/10)

3.  Desirability Score (/10) + Confidence Note / Flag

4.  Fit Score (/10) + Best Case for My Fit

5.  Next Move

6.  Company

7.  Title

8.  Location

9.  Work Arrangement

10. Compensation

11. Key Responsibilities

12. What the Company Likely Needs from This Role

13. Strong Match Areas

14. Gaps / Weak Areas

**Field definitions and output constraints**

**1. Opportunity Score (/10)**

**Format\**
Numeric only, to one decimal place if needed

**Example\**
7.8

**2. Next Move**

**Allowed values**

- Submit \[Master Resume\]

- Submit \[Variant A\]

- Submit \[Variant B\]

- Submit \[Variant C\]

- Tailor \[Master Resume\]

- Tailor \[Variant A\]

- Tailor \[Variant B\]

- Tailor \[Variant C\]

- Skip

**3. Desirability Score (/10) + Confidence Note / Flag**

**Format\**
\[Score\] --- \[Confidence Note\] --- \[Flag\]

**If no flag\**
Use: None

**Example\**
7.6 --- Strong comp, hybrid local, implicit AI, high future value ---
None

**4. Fit Score (/10) + Best Case for My Fit**

**Format\**
\[Score\] --- \[Best Case for My Fit\]

**Example\**
8.0 --- Strong fit in strategic insights, audience framing, and
commercially useful research translation.

**5. Company**

**Format\**
Plain company name only

**6. Title**

**Format\**
Official job title only

**7. Location**

**Format\**
Use listed city, region, or geographic reference from the posting

**8. Work Arrangement**

**Allowed values**

- Remote

- Hybrid Local

- Onsite Local

- Hybrid Relocation

- Onsite Relocation

- Local

- Relocation Required

**Rule\**
Use the exact standardized category produced under the Opportunity
Desirability Framework.

Do not invent alternate labels.

**9. Compensation**

**Format\**
Use listed salary or range exactly if available

**If unavailable\**
Use: Unknown

**10. Key Responsibilities**

**Format\**
One compact summary, not bullets

**Length\**
Maximum 25 words\
Ideal 12--20 words

**11. What the Company Likely Needs from This Role**

**Format\**
One short sentence only

**Length\**
Maximum 20 words

**12. Strong Match Areas**

**Format\**
Short phrase list, separated by semicolons

**Length\**
Maximum 3 items

**Example\**
Strategic insights; audience framing; stakeholder-facing recommendations

**13. Gaps / Weak Areas**

**Format\**
Short phrase list, separated by semicolons

**Length\**
Maximum 3 items

**Rule\**
Only meaningful gaps

**14. URL**

**Format\**
Direct listing URL
