# Execution Debt Model

## Definition

Execution debt is the accumulated cost of delayed, softened, or avoided execution.  
It represents momentum lost before work meaningfully begins.

Execution debt is not time waste.  
It is outcome destruction.

This model exists to make that loss visible.

---

## Purpose

The Execution Debt model confronts users with the hidden cost of non execution by converting invisible friction into measurable loss.

It does not:
- Teach productivity
- Offer advice
- Track behavior
- Optimize time
- Compare users

It does:
- Quantify momentum leakage
- Expose decision friction
- Create irreversible self recognition
- Anchor discomfort to clarity

This model is a mirror, not a guide.

---

## Foundational Beliefs

- People do not lack time. They leak execution.
- Most damage occurs before work begins.
- Small delays compound into large outcome loss.
- Awareness must carry weight to be remembered.
- Trust is built through conservative assumptions.

All calculations and constraints flow from these beliefs.

---

## Model Scope

This model measures execution debt through four independent loss channels:

1. Task postponement
2. Decision delay
3. Context switching
4. Rework and replanning

Each channel is modeled conservatively and independently to avoid exaggeration or overlap.

---

## Inputs

All inputs are measured per week unless stated otherwise.

### Tasks Postponed per Week (TPW)
Number of tasks intended for execution but pushed forward.

Range  
0 to 20

Default  
5

---

### Average Decision Delay (ADD)
Average time between deciding to act and starting.

Range  
0 to 60 minutes

Default  
10 minutes

---

### Context Switches per Day (CSD)
Number of times attention shifts between tasks, apps, or mental contexts.

Range  
0 to 50

Default  
15

---

### Rewrites or Replans per Task (RPT)
Number of times a task is rethought, rewritten, or redesigned instead of shipped.

Range  
0 to 5

Default  
1

---

## Fixed Constants

These values are fixed and not user adjustable.

WORK_DAYS_PER_WEEK = 5  
WEEKS_PER_MONTH = 4.33

Rationale  
Fixed constants prevent manipulation, preserve comparability, and maintain credibility.

---

## Loss Models

Execution debt is calculated as the sum of four conservative loss models.

---

### A. Task Postponement Loss (TPL)

Assumption  
Postponed tasks incur reorientation cost and priority decay.

Loss per postponed task  
25 minutes

Weekly calculation  
TPL = TPW × 25

---

### B. Decision Delay Loss (DDL)

Assumption  
Decisions block real work, not abstract thought.

Weekly calculation  
DDL = TPW × ADD

---

### C. Context Switching Loss (CSL)

Assumption  
Cognitive switching cost increases after saturation.

Per day calculation  

If CSD ≤ 20  
daily_loss = CSD × 2.5  

If CSD > 20  
daily_loss = (20 × 2.5) + ((CSD − 20) × 4)

Weekly calculation  
CSL = daily_loss × WORK_DAYS_PER_WEEK

This avoids underestimation, unrealistic explosions, and disbelief.

---

### D. Rework and Replanning Loss (RWL)

Assumption  
Rework destroys momentum more than it costs time.

Loss per rewrite  
15 minutes

Weekly calculation  
RWL = TPW × RPT × 15

---

## Total Execution Debt

Weekly total in minutes  

TOTAL_MINUTES =  
TPL + DDL + CSL + RWL

Weekly execution debt in hours  

WEEKLY_DEBT_HOURS = TOTAL_MINUTES ÷ 60

---

## Monthly Lost Outcomes

Assumption  
One meaningful outcome requires approximately eight focused hours.

Monthly execution debt  

MONTHLY_DEBT_HOURS = WEEKLY_DEBT_HOURS × 4.33

Lost outcomes  

LOST_OUTCOMES = floor(MONTHLY_DEBT_HOURS ÷ 8)

Values are always rounded down.

---

## Output Interpretation

Primary outputs are:

- Weekly execution debt expressed in hours
- Monthly lost outcomes expressed as an integer

These values represent work that never shipped.

---

## Verdict Thresholds

Based on WEEKLY_DEBT_HOURS:

Less than 5  
Execution is intact. Minor friction only.

5 to 15  
Execution is leaking. Busyness is masking loss.

15 to 30  
Momentum is being traded for comfort.

Above 30  
Activity exists without effectiveness.

Verdicts are blunt by design.

---

## Edge Cases

### All inputs equal zero

Interpretation  
Execution is not the bottleneck. The constraint lies elsewhere.

No artificial debt is generated.

---

### Extreme inputs

All values are calculated fully.  
Only visual display may be capped.  
Internal accuracy is preserved.

---

## Skepticism Defense

All values are conservative.

The model excludes:
- Emotional fatigue
- Confidence erosion
- Identity drift
- Opportunity cost of delayed compounding

Measured debt represents a lower bound.

---

## What This Model Excludes

This model intentionally does not:
- Offer advice
- Suggest improvements
- Explain formulas by default
- Personalize interpretation
- Compare individuals
- Act as a coach

The moment it helps, it breaks.

---

## Final Note

Execution debt is not a feature.  
It is a filter.

It does not attract everyone.  
It reveals who is ready.

That is the point.
