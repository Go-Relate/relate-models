# Momentum Flow Field Model

## Definition

Momentum Flow Field models execution as a dynamic flow system.

When aligned, execution moves forward smoothly.  
When fractured, it becomes turbulent.  
When overloaded, it reverses.

This model does not measure productivity.  
It reveals movement.

---

## Purpose

The Momentum Flow Field exists to make execution momentum visible.

It does not optimize, score, or judge.  
It exposes how effort translates into movement or fails to.

The model is designed to separate:
- Effort from progress
- Activity from direction
- Intensity from consistency

The goal is recognition, not correction.

---

## Non Goals

This model explicitly does not:
- Predict success
- Judge intelligence
- Measure productivity
- Diagnose personality
- Provide advice
- Recommend actions
- Replace coaching
- Store or track data

If a user asks for improvement steps, the model has already done its job.

---

## Core Metaphor

Execution behaves like a flow system.

- Alignment creates forward motion
- Friction creates turbulence
- Overload causes reversal

Momentum is not willpower.  
It is a systems outcome.

---

## Model Scope

The model evaluates momentum using four controllable inputs:

1. Focused execution
2. Context switching
3. Execution consistency
4. Overthinking frequency

These inputs are sufficient to explain most perceived stuckness without overfitting.

---

## Inputs

All inputs are user controlled and continuous.

### Focused Work per Day
Time spent in actual focused execution.

Range  
0 to 10 hours

---

### Context Switches per Hour
Frequency of task, app, or attention switching.

Range  
0 to 20

This input represents friction.

---

### Execution Consistency
Number of days per week execution actually occurs.

Range  
0 to 7 days

This input represents stability.

---

### Overthinking Frequency
Degree of rethinking instead of acting.

Range  
0 to 10

This input represents noise.

---

## Normalization

All inputs are normalized to a 0 to 1 range.

focus_score = focused_hours ÷ 10  
switch_penalty = context_switches ÷ 20  
consistency_score = consistency_days ÷ 7  
overthink_penalty = overthinking ÷ 10  

Rules:
- All values are clamped between 0 and 1
- NaN values fall back to defaults
- Undefined states are not permitted

---

## Momentum Calculation

Momentum is computed using a fixed weighted model.

momentum =  
( focus_score × 0.4  
+ consistency_score × 0.4 )  
− ( switch_penalty × 0.1  
+ overthink_penalty × 0.1 )

The resulting value is clamped between 0 and 1.

If calculation fails, momentum defaults to 0.5.

---

## Weighting Rationale

Focus and consistency represent movement.  
Switching and overthinking represent friction.

Friction is numerically smaller but visually destructive.

This mirrors reality:
Small friction can destroy large effort.

---

## Momentum States

Momentum resolves into exactly three states.

---

### Aligned Flow

Condition  
momentum > 0.6

Meaning  
The execution system is coherent.

---

### Turbulent Flow

Condition  
0.3 ≤ momentum ≤ 0.6

Meaning  
Forward motion exists but friction is stealing momentum.

---

### Backflow

Condition  
momentum < 0.3

Meaning  
Energy exists without forward progress.

---

No fourth state exists.  
There is no perfect state.

---

## Visual Interpretation Rules

The model maps internal values to visual behavior.

- Momentum controls flow speed
- Overthinking increases noise and jitter
- Context switching increases turbulence
- Consistency stabilizes direction

The flow never freezes.  
Even collapse must move.

---

## Output Layer

The model outputs a single verdict line.

Aligned Flow  
Your system is aligned. Protect this flow.

Turbulent Flow  
Momentum exists, but friction is stealing it.

Backflow  
You are moving, but not forward.

No variation is allowed.

---

## Edge Case Handling

The model safely handles:
- All inputs at zero
- All inputs at maximum
- Single input extremes
- Rapid input changes
- Resizing during motion
- Reduced motion preferences
- Low performance environments

Fallback behavior includes:
- Clamping values
- Reducing animation intensity
- Defaulting to stable visuals
- Never surfacing errors

---

## Accessibility and Performance

The model respects reduced motion preferences.

When enabled:
- Animation speed is reduced significantly
- Visual intensity is lowered

Additional constraints:
- Frame rate is capped
- No flashing
- No audio

---

## Data and Privacy

The model is fully client side.

- No storage
- No tracking
- No analytics
- No cookies
- No fingerprinting

All data is destroyed on refresh.

Trust is part of the system.

---

## What the Model Communicates

Without stating it explicitly, the model reveals:

- High effort does not guarantee progress
- Consistency outweighs intensity
- Friction compounds invisibly
- Execution is a system, not willpower

---

## Relationship to Relate

Momentum Flow Field does not sell Relate.

It demonstrates that Relate understands execution at a systems level.

If resonance occurs, users seek Relate on their own.

---

## Final Rule

If tempted to add:
- Advice
- Tips
- Explanations
- Scores
- Gamification
- Improvement framing

Stop.

That would turn a mirror into a lecture.
