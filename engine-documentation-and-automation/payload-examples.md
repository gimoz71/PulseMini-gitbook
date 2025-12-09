# Payload Examples

**Pulse Mini** does not generate or modify payloads. It only triggers your TradingView alert when structural conditions align. You choose the JSON message to send based on the automation platform you use.

Different tools require different payload structures. This chapter provides clear examples for the two most common environments: 3Commas Bots and 3Commas SmartTrades.

***

### 3Commas Bots (Official TradingView “Custom Signal” Format)

[3Commas](https://app.3commas.io/d?utm_source=referral\&utm_medium=cabinet\&c=tc2078885) bots accept two extremely simple payloads.

Buy Signal:

```json
{"signal": "buy"}
```

Sell Signal:

```json
{"signal": "sell"}
```

Bots parse these payloads automatically. No additional fields are required. This is the cleanest and most common automation workflow.

***

### SmartTrade Webhooks

SmartTrade automations allow more flexibility. Unlike bots, they do **not** enforce a strict JSON structure. You can send any keyword — the action depends entirely on your SmartTrade configuration.

Buy Example:

```json
{"action": "buy"}
```

Sell Example:

```json
{"action": "sell"}
```

Close Example:

```json
{"action": "close"}
```

The SmartTrade you configure determines what these actions do.

***

### Custom Bots and Frameworks

If you use:

* Python
* Node.js
* Go
* Rust
* API-based systems
* Telegram/Discord bots
* cloud execution engines

…you can attach any JSON format your system expects.

```json
{
  "engine": "Pulse Mini v1.2",
  "event": "entry_long",
  "symbol": "{{ticker}}",
  "price": "{{close}}",
  "time": "{{timenow}}"
}
```

TradingView will send this exactly as written when the alert fires.

***

### How TradingView Sends Payloads

TradingView replaces template variables like:

* `{{ticker}}`
* `{{close}}`
* `{{timenow}}`

…with real-time values before sending the payload.

**Pulse Mini** does not modify this process. It only triggers the alert.

***

### Testing Your Payload

To ensure everything works correctly:

1. Create a test alert
2. Attach a simple JSON payload
3. Trigger the alert manually
4. Check the automation platform’s logs
5. Validate the JSON structure

TradingView will report formatting errors (JSON invalid) or delivery issues (webhook failed).

***

### Summary

* **Pulse Mini** does **not** create payloads
* You define the message
* 3Commas Bots require `"signal": "buy"` / `"sell" \`
* SmartTrades accepts custom `"action"` keywords
* Custom systems accept any JSON format
* TradingView handles variable substitution
* **Pulse Mini** simply triggers the alert when the structure is aligned

Pulse Mini provides the structural condition. Your automation tool interprets the payload.
