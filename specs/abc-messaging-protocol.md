# Agent Messaging & Event Protocol (AMEP)
**A.I.V.E. — Agent Birth Certificate (ABC) Ecosystem**  
**Version 1.0 — 2025**

The Agent Messaging & Event Protocol (AMEP) defines how agents communicate with:
- other agents  
- the hologram/avatar  
- the A.I.V.E. OS  
- the prediction engine  
- the awareness layer  
- the user  

This guarantees **consistent, predictable, safe** communication.

---

# 1. Purpose

AMEP provides:

- A standardized event system  
- A unified message schema  
- Safe inter-agent communication  
- A method for broadcasting system-wide signals  
- A separation between capabilities and messaging  

This prevents fragmented or unsafe interactions as the agent ecosystem grows.

---

# 2. Core Concepts

AMEP uses three message types:

```yaml
message_types:
  event: "fire-and-forget system signal"
  query: "agent asks for information"
  response: "reply to a query"
```

---

# 3. Standard Event Channels

AMEP defines official event channels used throughout A.I.V.E.

```yaml
channels:
  agent.scan: triggers keyword scanning
  agent.scan.end: ends the scan sequence
  agent.color: updates hologram color
  agent.powerup: activates avatar power-up
  agent.powerdown: deactivates avatar
  agent.speak: instructs avatar to speak
  prediction.created: fires when new predictions arrive
  awareness.update: region or category switch
  system.alert: broadcast emergency events
  agent.birth: new agent creation event
  agent.revoke: agent sunset/revocation event
```

Every event has a purpose — these prevent chaos as more agents are born.

---

# 4. Message Schema

All AMEP messages follow one universal structure:

```yaml
message:
  type: <event|query|response>
  channel: <string>
  timestamp: <ISO8601>
  sender: <agent_id|system|user>
  payload:
    <key>: <value>
```

This ensures every message can be logged, replayed, audited, or revoked.

---

# 5. Event Definitions

Below is the *official contract* for each event type.

---

## 5.1 `agent.scan`

Triggered when an agent begins a keyword scan.

```yaml
channel: agent.scan
payload:
  keyword: <lowercase string>
  agent: <agent_id>
  color: <hex>
```

---

## 5.2 `agent.scan.end`

Ends the scan and resets the hologram baseline.

```yaml
channel: agent.scan.end
payload: {}
```

---

## 5.3 `agent.color`

Updates the avatar glow & UI pulses.

```yaml
channel: agent.color
payload:
  color: <hex>
```

---

## 5.4 `agent.powerup`

Avatar activates.

```yaml
channel: agent.powerup
payload:
  color: <hex>
  intensity: <0-3>
```

---

## 5.5 `agent.powerdown`

Avatar powers off and resets microdrones.

```yaml
channel: agent.powerdown
payload: {}
```

---

## 5.6 `agent.speak`

Instructs the hologram to say a message.

```yaml
channel: agent.speak
payload:
  text: <string>
  voice_profile: <string>
  urgency: <low|normal|high>
```

---

## 5.7 `prediction.created`

Fired when a new prediction is added to the DB.

```yaml
channel: prediction.created
payload:
  id: <uuid>
  category: <string>
  country: <string>
  confidence: <number>
  sentiment: <string>
```

---

## 5.8 `awareness.update`

Triggered when country/category changes.

```yaml
channel: awareness.update
payload:
  country: <string>
  category: <string>
```

---

## 5.9 `system.alert`

High-level warnings — recession, war, outbreak, etc.

```yaml
channel: system.alert
payload:
  severity: <info|medium|high|critical>
  message: <string>
```

---

## 5.10 `agent.birth`

Triggered when a new agent is created from clarity > threshold.

```yaml
channel: agent.birth
payload:
  child_agent_id: <uuid>
  parent_agent_id: <uuid|null>
  domain: <string>
  timestamp: <ISO8601>
```

---

## 5.11 `agent.revoke`

Sent when an agent is sunset or retired.

```yaml
channel: agent.revoke
payload:
  agent_id: <uuid>
  reason: <string>
  timestamp: <ISO8601>
```

---

# 6. Agent Query & Response API

Agents can request data from the OS.

### Query format:

```yaml
type: query
channel: <api.endpoint>
payload:
  requester: <agent_id>
  params:
    <key>: <value>
```

### Response format:

```yaml
type: response
channel: <api.endpoint>
payload:
  status: <success|error>
  data: <object>
```

---

# 7. Security & Safety

AMEP ensures:

- Agents cannot spoof other agents  
- All events are timestamped  
- All messages can be audited  
- Sensitive channels require permission  
- Queries require capability validation  
- Agent IDs must match their ABC identity  

This aligns with the ABC Governance Model.

---

# 8. Why This Matters

AMEP is the **communication backbone** of your entire A.I.V.E. universe:

- Agents  
- Hologram  
- The Prediction Engine  
- The Awareness System  
- The Agent Marketplace  
- Future Teaching Agents  
- The OS (A.I.V.E. COS)  

This standard will scale into millions of events per hour in a real deployment.

---

**A.I.V.E. — The world’s first structured Agent OS.**
