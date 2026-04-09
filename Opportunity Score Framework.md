**Opportunity Score Framework**

**Purpose**

This framework defines how desirability and fit combine into one overall
opportunity score for fast triage.

It answers:

**Given both how much the candidate wants the role and how credible
their candidacy is, how strong is this opportunity overall?**

This framework is the single source of truth for:

- the Opportunity Score formula

- score interpretation

- high-level triage meaning

It does **not** define:

- desirability sub-score logic

- fit sub-score logic

- next-move output values

- output formatting rules

**Inputs**

**1. Desirability Score (/10)**

Use the final score from the **Opportunity Desirability Framework**.

Desirability captures:

- compensation attractiveness

- work arrangement attractiveness

- AI relevance / AI potential

- strategic career value

**2. Fit Score (/10)**

Use the final score from the **Opportunity Fit Framework**.

Fit captures:

- functional match

- seniority match

- qualification match

- evidence strength

**Core formula**

**Opportunity Score = (Desirability Score × 0.5) + (Fit Score × 0.5)**

Maximum = **10**

**Default weighting**

- Desirability = **50%**

- Fit = **50%**

This system treats both dimensions as equally important for first-pass
opportunity triage.

**Why equal weighting**

A strong opportunity should usually be:

- attractive enough to matter

- plausible enough to pursue

Equal weighting helps prevent two common mistakes:

**Mistake 1**

Pursuing attractive but unrealistic roles too aggressively

**Mistake 2**

Over-investing in highly plausible roles that are weak on compensation,
flexibility, AI relevance, or long-term value

**Interpretation bands**

**8.5--10.0**

**Top-priority opportunity**

Usually worth serious attention.

Typically indicates:

- strong desirability

- strong fit

- good use of application time

**7.0--8.4**

**Strong opportunity**

Usually worth pursuing unless there is a specific disqualifier.

May include:

- high-fit but somewhat less exciting roles

- high-desirability roles with manageable stretch

**5.5--6.9**

**Borderline / selective pursue**

Requires more judgment.

Often includes:

- decent but not compelling roles

- opportunities with one strong dimension and one weak dimension

- opportunities that may be worth pursuing only if volume is needed or
  customization cost is low

**Below 5.5**

**Low-priority opportunity**

Usually not a strong use of time.

Often includes:

- low-desirability / low-fit roles

- roles that are attractive but too implausible

- roles that are plausible but too weak on compensation, flexibility, or
  long-term value

**Interpretation rules**

**1. Do not let the Opportunity Score replace judgment**

The score is a triage aid, not a substitute for reasoning.

Use it to improve consistency and speed, not to eliminate thought.

**2. Strong imbalance matters**

Two roles with the same total score may still be different in practice.

Examples:

- a role with very high desirability and moderate fit

- a role with very high fit and moderate desirability

These may require different next moves even if the overall score is
similar.

**3. Low fit should remain a real warning**

A role should not become a priority merely because it is exciting,
well-paid, or remote if the candidacy is too weak.

**4. Low desirability should remain a real warning**

A role should not become a priority merely because it is plausible if it
is weak on compensation, work arrangement, or strategic value.

**5. Unknown-heavy cases should be treated cautiously**

If major parts of desirability or fit rely on uncertainty, the total
score should be interpreted more cautiously even if the numeric result
looks decent.

**Suggested practical read of score patterns**

**High desirability + high fit**

Best-case opportunity profile

**High desirability + moderate fit**

Often worth pursuing selectively, especially if the stretch is credible

**Moderate desirability + high fit**

Often worth pursuing if application effort is low or the role has
practical value

**Low desirability + high fit**

Usually a selective or lower-priority pursue case

**High desirability + low fit**

Tempting, but often a distraction unless the stretch is unusually
defensible

**Low desirability + low fit**

Skip in most cases

**Relationship to next move**

This framework helps inform the next move, but it does **not** own the
next-move output values.

Next Move should be determined in the **Opportunity Evaluation Prompt**
using:

- Opportunity Score

- Fit bucket

- Desirability

- Resume routing logic

- practical judgment

**Practical scoring instruction**

When calculating the Opportunity Score:

1.  use the final Desirability Score from the Desirability Framework

2.  use the final Fit Score from the Fit Framework

3.  apply the 50/50 weighting

4.  round sensibly for scan-friendly output

5.  interpret the result using the guidance above

6.  do not override clear judgment problems just because the total looks
    respectable

**Final interpretation rule**

This framework exists to improve triage quality.

It should help answer:

- Is this role worth real attention?

- Is this a strong use of application time?

- Is this exciting but unrealistic?

- Is this plausible but not attractive enough?

It should not blur the distinction between:

- **wanting the role\**
  and

- **being a credible candidate for the role**
