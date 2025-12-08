---
icon: hexagon-nodes-bolt
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
---

# Engine Documentation

Pulse Mini is a simplified expression of the Pulse Market Engine. Its purpose is to provide a **clean, stable and non-repainting** interpretation of market behaviour through three core layers:

* Trend
* Phase
* Timing

Mini does not predict future movements. It reads the present — clearly and consistently.

This chapter introduces the engine’s design philosophy before diving into each structural layer.

### What Makes Pulse Mini Different

Unlike traditional indicators built on formulas, oscillators, or smoothing functions, Pulse Mini:

* does **not** rely on moving averages
* does **not** use oscillators
* does **not** generate predictive projections
* does **not** recalc or repaint historical bars

Instead, it observes how price behaves in real time and reduces noise by focusing on elements that matter across all markets:

* structural direction
* expansion and contraction
* behavioural transitions
* momentum continuity vs instability

Pulse Mini reads behaviour — not indicators.

### Unified Interpretation Across Timeframes

The engine adapts naturally across:

* 1H
* 2H
* 4H
* 1D

It maintains:

* consistent structural reading
* identical behavioural logic
* non-repainting signals
* a unified interpretation of context

This means traders do not need to adjust settings or learn different behaviours per timeframe.

### When Signals Appear

Signals appear only when:

* Trend is aligned
* Phase is clear
* Timing is supportive

Pulse Mini does **not** force triggers during unstable environments. It prefers neutrality over noise.

This is why Pulse Mini feels “calmer” than most indicators — it ignores low-quality conditions and highlights only structural clarity.

### Why Mini Doesn’t Try to Catch Every Move

Pulse Mini is not designed to:

* chase volatility
* react to every micro swing
* compete for the highest number of signals

Its purpose is different: **to show when the environment is actually worth your attention.**

This preserves stability and dramatically reduces false or low-quality signals.

### Reading First, Acting Later

Pulse Mini separates:

* **market reading** (Pulse)
* **execution** (manual or automated)

This keeps the method clean: Pulse reads → you act (optionally via bots)

Mini does not tell you _what_ to trade. It tells you _when the environment is structurally clear_.

### What This Overview Prepares You For

The following chapters will detail:

* Market Context
* Trend Layer
* Phase Layer
* Timing Layer
* Trigger Logic
* Decision Matrix

This overview establishes the foundation — the philosophical and structural principles.
