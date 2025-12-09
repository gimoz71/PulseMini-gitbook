# Why Pulse Mini Can Be Used in External Systems

TradingView does not allow scripts to import or call each other internally. Because of this, most indicators cannot be combined directly in Pine Script.

Pulse Mini solves this limitation by exposing its structural reading **externally**, through:

* TradingView alert conditions
* JSON payloads
* webhook delivery
* Entry/Exit confirmations
* non-predictive behavioural signals

This makes Pulse Mini fully compatible with **any system capable of receiving alerts**, regardless of the technology stack.

***

### A Behavioural Context Layer, Not an Embedded Script

Pulse Mini is not used by embedding its code inside another script. Instead, it acts as an **external context source**, providing objective structural information that your system can read and act upon.

Your bot or indicator does not need access to Pulse Mini’s internal logic. It only needs to receive the conditions Pulse Mini detects.

***

### Compatible with Every Automation Framework

Pulse Mini can be consumed by:

* Pine-based bots
* custom Pine indicators
* Python trading engines
* Node.js bots
* 3Commas bots & SmartTrades
* Telegram/Discord automation bots
* proprietary trading systems
* hybrid off-chain/on-chain logic

Any environment that receives a webhook or reads data can use Pulse Mini.

***

### Why It Works So Well

Pulse Mini exposes:

* structural confirmations
* trend alignment
* phase clarity
* timing coherence
* exit conditions
* noise-filtered behaviour

This is the same information the engine uses visually — but delivered as machine-readable data. Your system can then:

* filter trades
* validate entries
* enhance timing
* avoid chaotic environments
* improve consistency

Pulse Mini becomes a **behavioural oracle** for your strategy.

***

### No Need to Modify Your Codebase

Because Pulse Mini outputs its signals externally:

* you don’t modify your Pine code
* you don’t rework your bot logic
* you don’t integrate new indicators
* you don’t touch existing strategies

Pulse Mini remains separate, providing a clean, non-repainting context without interfering with your internal architecture.

***

### Clean Separation of Logic

Pulse Mini respects a strict boundary: **Pulse reads → your system acts.**

This prevents:

* overlapping logic
* contradictory behaviour
* repaints
* execution errors
* indicator conflicts

It guarantees consistency across systems, bots, and timeframes.
