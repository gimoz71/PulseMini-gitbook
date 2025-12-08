# Important Note

Pulse Mini does not create, define, or modify any payloads used for automation. It only triggers your TradingView alert when structural market conditions are aligned.

All automation, execution, and order-handling behaviour depends entirely on the tools you connect.

This distinction is essential for clarity, safety, and correct usage of the Pulse Method.

### What Pulse Mini Does Not Do

Pulse Mini does **not**:

* execute trades
* place orders
* manage TP/SL
* handle risk or position sizing
* interact with exchange APIs
* generate payload formats
* send instructions to bots
* operate autonomously

Pulse Mini is not a trading bot, not a signal service, and not an automated system.

It is a **market-reading engine**.

### Who Generates the Payload

The payload inside your alert is:

* written by **you**
* interpreted by your **automation platform**
* executed by your **exchange or bot**

TradingView delivers the message. 3Commas interprets it. Bots execute it. Exchanges fill it.

Pulse Mini does **not** participate in any of these steps.

### Why This Matters

Keeping the reading layer separate from the execution layer ensures:

* full control over automation
* safety and oversight for users
* compliance across platforms
* modular design
* clean integration workflows
* predictable behaviour regardless of tools used

Pulse Mini remains neutral, consistent, and independent.

### Where to Get Accurate Payload Instructions

The correct instruction formats vary based on your setup. Always refer to:

* 3Commas Bot documentation (TradingView Custom Signal format)
* 3Commas SmartTrade webhook documentation
* your API bot or framework documentation
* your custom automation logic

Pulse Mini cannot generate payload standards because each system has its own requirements.

### Final Reminder

Pulse Mini provides:

* structural clarity
* behavioural consistency
* Trend–Phase–Timing alignment

You decide how to use that clarity:

* manually
* with alerts
* with automation tools
* through custom bots

Pulse reads the market. Your tools interpret the message. You remain in control.
