# Founder Reality Check Model

## Definition

Founder Reality Check is a diagnostic model that surfaces execution truth by collapsing self deception into observable patterns.

It does not evaluate potential or predict success.  
It reflects behavior as it currently exists.

The model does not tell founders what to do.  
It shows them what they are already doing.

---

## Purpose

The Founder Reality Check exists to surface execution reality without motivation, advice, persuasion, or ego reinforcement.

It is designed to:
- Remove rationalization
- Force pattern recognition
- Create tension without resolution
- Make misalignment visible

Any desire for guidance after the result indicates the model has already succeeded.

---

## Non Goals

This model explicitly does not:
- Predict outcomes
- Diagnose personality
- Measure intelligence
- Assess productivity
- Replace coaching
- Provide next steps

The absence of instruction is intentional.

---

## Model Scope

The model evaluates execution through three dimensions:

1. Clarity  
2. Alignment  
3. Capacity  

These dimensions represent the minimum structure required to explain most founder execution failure without overfitting.

---

## Input Structure

### Input Type

Binary responses only.

YES = 1  
NO = 0  

No partial answers.  
No scales.  
No ambiguity.

Binary inputs eliminate rationalization and make the model deterministic.

---

### Input Count

Exactly ten questions.

All questions are mandatory.  
Submission is blocked until all inputs are provided.

---

## Execution Dimensions

### Dimension 1: Clarity (C)

Question  
Do you know what you should be doing right now?

Mapped inputs  
Q1  
Q2  
Q3  

Range  
0 to 3

---

### Dimension 2: Alignment (A)

Question  
Are your actions matching your intent?

Mapped inputs  
Q4  
Q5  
Q6  

Range  
0 to 3

---

### Dimension 3: Capacity (P)

Question  
Do you have sufficient resources to execute?

Mapped inputs  
Q7  
Q8  
Q9  
Q10  

Range  
0 to 4

Capacity is intentionally weighted heavier because it is frequently misdiagnosed.

---

## Raw Scoring

Raw dimension scores are computed as follows:

C = Q1 + Q2 + Q3  
A = Q4 + Q5 + Q6  
P = Q7 + Q8 + Q9 + Q10  

---

## Normalization

Capacity is normalized to align with other dimensions.

Pn = P × (3 ÷ 4)

Final comparable ranges:

C ∈ [0, 3]  
A ∈ [0, 3]  
Pn ∈ [0, 3]

No rounding is applied.

---

## Dimension Thresholds

Each dimension is classified using fixed thresholds.

Strong  
≥ 2.5  

Weak  
≤ 1.5  

Unstable  
Between 1.5 and 2.5  

Boundaries are inclusive.  
No fuzzy logic is used.

---

## Output States

The model always resolves to exactly one state.

---

### State A: Clear but Overloaded

Meaning  
Direction is clear.  
Intent is aligned.  
Execution is constrained by load.

Trigger  
C ≥ 2.5  
A ≥ 2.0  
Pn ≤ 1.5  

Interpretation  
The founder is not lost. They are saturated.

---

### State B: Capable but Misaligned

Meaning  
Energy exists.  
Resources exist.  
Direction or intent is fractured.

Trigger  
Pn ≥ 2.5  
AND (C ≤ 1.5 OR A ≤ 1.5)

Interpretation  
Effort is real but pointed incorrectly.

---

### State C: Focused but Under Resourced

Meaning  
Direction is clear.  
Intent is aligned.  
Resources are insufficient.

Trigger  
C ≥ 2.5  
A ≥ 2.5  
AND 1.5 < Pn < 2.5  

Interpretation  
The founder is doing the right things too slowly.

---

## Tie Breaker Priority

If multiple states resolve simultaneously, the following priority applies:

1. Capable but Misaligned  
2. Clear but Overloaded  
3. Focused but Under Resourced  

Reasoning  
Misalignment causes the most damage.  
Overload is recoverable.  
Under resourcing is solvable.

---

## Forced Edge Cases

These rules guarantee resolution in all scenarios.

---

### All YES

C = 3  
A = 3  
P = 4  

Resolution  
Focused but Under Resourced  

Reason  
High performers are always constrained.

---

### All NO

C = 0  
A = 0  
P = 0  

Resolution  
Capable but Misaligned  

Reason  
Avoidance does not equal incapability.

---

### No Clean Resolution

Resolution  
Capable but Misaligned  

Reason  
Ambiguity itself is misalignment.

---

## Confidence Index

The model computes a hidden confidence signal.

Computation  
dominance = |highest_dimension − second_highest_dimension|

Interpretation  

dominance ≥ 1.0  
High confidence  

dominance < 1.0  
Low confidence  

Display is textual only.

High confidence  
This pattern is consistent.

Low confidence  
This pattern is unstable. Recheck in seven days.

No numeric values are shown.

---

## Root Cause Line System

Each output state has exactly three predefined root cause lines.

Selection rules:
- Weakest dimension determines the line
- If two dimensions are equally weak, a combined line is used
- Strings are fixed
- No randomness
- No personalization
- No AI

Purpose  
Explain the result without offering advice or inviting debate.

---

## Anti Gaming Constraint

If four or more answers are changed within thirty seconds:

- Submission is disabled for five seconds
- A message is shown

Do not optimize your answers. Observe them.

No tracking or storage is used.

---

## Technical Constraints

- Frontend only
- Stateless
- Deterministic
- No persistence
- No analytics
- No asynchronous logic affecting outcomes

Refresh resets the model completely.

---

## Failure Modes Prevented

The model guarantees:
- No undefined states
- No NaN outputs
- No ties without resolution
- No flattering defaults
- No confusion states
- No ego reinforcement

The system cannot collapse.

---

## Final Note

Founder Reality Check is not meant to motivate, inspire, or reassure.

It exists to remove the lie between effort and outcome.
