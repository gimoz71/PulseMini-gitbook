# Settings – Alerts & Automation

Pulse Mini operates entirely inside TradingView. It does not execute trades or manage positions — it simply detects when the market environment is clean, aligned, and structurally favourable.

To receive these confirmations, or to automate them through external systems, you will use **TradingView alerts**.

This chapter explains how alerts work, how to configure them, and how to connect them to automation tools like 3Commas.

***

### How Pulse Mini Alerts Work

Pulse Mini provides internally defined alert conditions such as:

* Entry Long
* Entry Short
* Exit Long
* Exit Short

These appear automatically in the TradingView “Condition” menu when creating an alert — no manual configuration is required.

TradingView alerts act as the bridge:

**Pulse Mini (market reading) → TradingView (alerts) → Automation tools (execution)**

***

### Pulse Mini Alert Commands

Inside the _Create Alert_ panel, select:

**Condition → Pulse Mini v1.2 → (desired signal)**

For example:

* _Pulse Mini v1.2 — Entry Long_
* _Pulse Mini v1.2 — Exit Short_

Then choose:

* **Once Per Bar Close** (recommended)
* **Webhook URL** (optional)
* **Notification settings**

Pulse Mini triggers the alert only when Trend, Phase, and Timing align structurally.

***

### Creating Your First Alert

Steps:

1. Click “Create Alert” in the TradingView toolbar
2. Set **Condition → Pulse Mini v1.2 — Entry Long**
3. Choose **Once Per Bar Close**
4. (Optional) Enable **Webhook URL**
5. (Optional) Paste your automation endpoint (e.g., 3Commas)
6. Insert a JSON message in the **Message** field
7. Save

Pulse Mini will fire the alert when the structural alignment appears.

***

### Example: JSON Payload for Entry Long

If you automate through webhooks, you may use a JSON payload like:

```json
{
  "engine": "Pulse Mini v1.2",
  "event": "entry_long",
  "symbol": "{{ticker}}",
  "price": "{{close}}",
  "timestamp": "{{timenow}}"
}
```

TradingView sends this payload to the webhook exactly when the alert triggers.

***

### Webhook Setup

A webhook is a URL that receives your alert message. Flow:

**TradingView sends alert → Webhook receives JSON → Automation tool executes**

Enable the webhook only if you automate.

Manual traders can simply use notifications.

***

### Connecting Pulse Mini to 3Commas (Optional)

3Commas can turn alerts into:

* market orders
* limit orders
* SmartTrades
* DCA bot instructions

Basic bot payload:

```json
{"signal": "buy"}
```

SmartTrade example:

```json
{"action": "sell"}
```

3Commas interprets the payload based on your SmartTrade or bot configuration.

Pulse Mini provides the signal — 3Commas executes it.

***

### TradingView → 3Commas

### Testing Your Setup

To ensure everything works:

* create a temporary alert
* use a simple test JSON
* verify reception on your automation tool
* check TradingView’s Alert Log

TradingView will report any JSON or delivery error.

***

### Best Practices

For stable behaviour:

* always use **Once Per Bar Close**
* favour 1H–4H for automation
* keep JSON minimal
* test before using live funds
* avoid ultra-low timeframes for automated signals
* use Golden Five markets

***

### Troubleshooting FAQ

#### Alert not firing

* check if Pulse Mini is active
* verify signal availability
* confirm alert type (use Once Per Bar Close)

#### Webhook not received

* confirm webhook URL
* check TradingView Alert Log for delivery errors

#### JSON invalid

* validate formatting
* avoid stray commas
* check quotes and brackets

#### 3Commas not reacting

* bots require `"signal": "buy"` / `"sell"`
* SmartTrades require `"action"` keywords
* ensure bot/SmartTrade is set to listen for TradingView alerts

***

### Important Notes

Pulse Mini:

* does not execute trades
* does not manage TP/SL
* does not replace risk management
* does not predict the future
* does not modify your payload

Pulse Mini provides **structural confirmation**. The user decides how to act on it — manually or via automation.
