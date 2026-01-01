# Focus Fracture Heat Map Model

## Definition

Focus Fracture Heat Map visualizes how attention is fragmented across a workday.

The day is not empty.  
It is broken into pieces too small to compound.

This model exposes fragmentation directly rather than estimating productivity or optimizing time.

---

## Purpose

The Focus Fracture Heat Map exists to make attention damage visible.

It answers one question visually:

Where did the day actually go.

The model separates:
- Time spent from attention preserved
- Long hours from continuous focus
- Busyness from depth

The goal is recognition, not correction.

---

## Non Goals

This model explicitly does not:
- Measure productivity
- Judge discipline
- Diagnose attention disorders
- Provide solutions
- Recommend routines
- Track behavior
- Store data
- Predict outcomes

If a user asks how to fix the result, the model has already succeeded.

---

## Core Metaphor

Attention does not disappear in gaps.  
It dies in fragments.

A day can be full and still be ineffective.

---

## Model Scope

The model represents a workday as a fixed timeline of attention blocks and assigns each block a state based on switching and interruption behavior.

It does not infer intent or effort.  
It only shows distribution.

---

## Time Model

The workday is modeled as:

Total duration  
12 hours

Resolution  
5 minute blocks

Blocks per hour  
12

Total blocks  
144

Each block represents one uninterrupted five minute window of potential attention.

---

## Inputs

All inputs are user controlled and unambiguous.

### Context Switches per Hour

Represents task switching, app hopping, or attention redirection.

Range  
0 to 20

This input models micro fractures.

---

### Interruptions per Day

Represents messages, calls, pings, or external disruptions.

Range  
0 to 40

This input models macro breaks.

---

## Visual States

Each block exists in exactly one of three states.

---

### Deep Focus

Meaning  
Sustained attention

Color  
Blue

---

### Fractured

Meaning  
Broken focus due to switching

Color  
Red

---

### Transition

Meaning  
Attention lost to interruptions or switching overhead

Color  
Gray

---

Only these three states exist.  
No gradients or intermediate values are allowed.

---

## Distribution Logic

### Constants

TOTAL_BLOCKS = 144  
HOURS = 12  
BLOCKS_PER_HOUR = 12  

---

### Step 1: Calculate Fractures

fractures_per_hour = context_switches_per_hour  
total_fractures = fractures_per_hour × HOURS  

Rules:
- total_fractures is clamped to a maximum of 144
- if context switches equal zero, no fractured blocks are created

---

### Step 2: Calculate Interruptions

interruption_blocks = interruptions_per_day  

Rules:
- each interruption consumes exactly one block
- interruption_blocks is clamped to a maximum of 144

---

### Step 3: Initialize Timeline

All 144 blocks are initialized as Deep Focus.

---

### Step 4: Assign Fractured Blocks

If total_fractures is greater than zero:

interval = floor(144 ÷ total_fractures)

Algorithm:
- Traverse the timeline left to right
- Mark every interval-th block as Fractured
- Skip blocks already assigned
- Stop once total_fractures blocks are placed

This produces evenly distributed micro fractures.

---

### Step 5: Assign Transition Blocks

Algorithm:
- Spread interruption_blocks evenly across the timeline
- Use deterministic spacing
- No randomness is permitted

Priority rule:
- Transition overrides Fractured
- Fractured overrides Deep Focus

---

## Safety Override

If total_fractures + interruption_blocks is greater than or equal to 144:

- Enforce a minimum of ten percent Deep Focus
- min_focus_blocks = floor(144 × 0.10) = 14
- Remaining blocks = 130
- Remaining blocks are split proportionally between Fractured and Transition

This prevents visual nihilism while preserving truth.

Zero Deep Focus blocks are never allowed.

---

## Validation Rules

Before rendering:
- Total blocks must equal 144
- No block may have more than one state

If any calculation fails:
- Fallback distribution is used

Fallback:
- 70 percent Deep Focus
- 20 percent Fractured
- 10 percent Transition

Errors are never shown to the user.

---

## Output Metrics

Optional secondary outputs may display:

- Count of Deep Focus blocks
- Count of Fractured blocks
- Count of Transition blocks

Rules:
- Counts only
- No percentages
- No scores
- No interpretation text

---

## Verdict Anchor

A single static line is always visible:

You do not need more time. You need fewer fractures.

No variation is allowed.

---

## Accessibility and Performance

The model:
- Respects reduced motion preferences
- Uses high contrast colors
- Avoids flashing
- Renders quickly
- Fails gracefully

Performance issues never surface to the user.

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

- Time is not the constraint
- Continuity determines depth
- Switching destroys compounding
- Interruptions accumulate invisibly

The message is seen, not taught.

---

## Relationship to Relate

Focus Fracture Heat Map does not sell Relate.

It demonstrates that Relate understands execution at the level of attention systems.

If the mirror resonates, users will seek more.

---

## Final Rule

If tempted to add:
- Advice
- Fixes
- Tips
- Improvement framing
- Gamification
- Scores
- Coaching language

Stop.

That would turn a mirror into a lecture.
