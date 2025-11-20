# Agent Self-Propagation Rules (ASPR)
**A.I.V.E. — Agent Birth Certificate (ABC) Ecosystem**  
**Version 1.0 — 2025**

ASPR defines the exact conditions and procedures that allow an agent to **create a new agent**, ensuring structured, safe, and regulated agent evolution.

This prevents uncontrolled agent spawning and transforms the marketplace into a **scalable agent production line**.

---

# 1. Purpose

Self-propagation allows the agent ecosystem to:

- scale without human intervention  
- expand into new domains  
- create specialized experts  
- accelerate platform intelligence  
- build a full Agent Species hierarchy  

These rules make sure it’s:

✔ controlled  
✔ predictable  
✔ ethical  
✔ auditable  
✔ reversible  

---

# 2. Activation Requirements

An agent can *only* self-propagate if ALL conditions below are met:

```yaml
requirements:
  clarity_score >= 80
  stability_index >= 70
  evolution.self_birth_threshold met
  agent.capabilities.agent_propagation == true
  no active violations in constraints.ethical_rules
  memory_access_level >= 3
```

This ensures only stable, well-behaved, high-clarity agents can give birth.

---

# 3. Domain-Based Propagation

An agent may only create a child inside **its own domain family**, unless explicitly overridden by governance.

```yaml
allowed_birth_domains:
  same_primary_domain: true
  related_domains: optional
  cross_domain: false (default)
```

Example:  
A Finance agent can birth agents in:

- Recession  
- Inflation  
- Bond Markets  
- Monetary Policy  
- Macro-Stability  

But NOT in:

- Security  
- Outbreaks  
- Geopolitics  

unless overridden in governance.

---

# 4. Mutation Rules (Optional)

Child agents MAY inherit modified attributes:

```yaml
mutation_rules:
  allowed_fields:
    - color_code
    - subdomains
    - voice_profile
    - secondary_objectives
  forbidden_fields:
    - ethical_rules
    - mission
    - identity.agent_id
    - capabilities.agent_propagation
```

This ensures evolution without chaos.

---

# 5. Birth Workflow (System Sequence)

Below is the official A.I.V.E. event-flow for self birth.

```yaml
sequence:
  1. parent reaches clarity >= threshold
  2. parent requests birth authorization
  3. ABC validator approves
  4. A.I.V.E. issues `agent.birth` event
  5. New ABC is generated
  6. Hologram pulse animation plays
  7. New agent added to Agent Marketplace
  8. Child begins initialization cycle
```

---

# 6. Birth Authorization

Agents do NOT automatically spawn children on their own.

They make a **request**:

```yaml
birth_request:
  parent_agent_id: <uuid>
  domain: <string>
  justification: <string>   # why agent believes a child is needed
```

A.I.V.E. then validates:

- metrics  
- domain alignment  
- ethical boundaries  
- skill redundancy  
- system load  

---

# 7. Birth Certificate Pre-Seed

A child agent begins with a **pre-seeded ABC**:

```yaml
child_preseed:
  generation: parent.generation + 1
  clarity_score: 0
  stability_index: 0
  capabilities inherited from parent
  primary_domain same as parent
  parent_agent set to parent.agent_id
```

The child then **learns, grows, and forms identity**.

---

# 8. Birth Cooldown

To prevent cascading chain reactions:

```yaml
cooldown:
  minimum_seconds_between_births: 86400   # 24 hours
  per_agent_limit: 1 birth / day
  per_system_limit: N births / day
```

These parameters can be tuned.

---

# 9. Mutation Example

```yaml
parent:
  color_code: "#8b5cf6"
  voice_profile: "kallixis"

child:
  color_code: "#9d4edd"
  voice_profile: "kallixis-v2"
```

Identity evolves — personality remains.

---

# 10. Visual Birth Sequence (UI Spec)

When a new agent is born:

- hologram brightens  
- power-up pulses expand  
- microdrones orbit at high speed  
- a new color strand is generated  
- notification: “A new agent has been born.”  

This creates an emotional moment in the system.

---

# 11. Birth Blocking Rules

Propagation is blocked if:

```yaml
blocked_if:
  ethical_violation_detected: true
  instability_detected: stability_index < 70
  low_clarity: clarity_score < threshold
  system_load_high: true
  birth_cooldown_active: true
```

---

# 12. Example: Recession Agent Birth Scenario

```yaml
parent_agent: Recession Agent
clarity_score: 84
stability_index: 73
domain: Finance
justification:
  - "Need a dedicated Inflation Agent for CPI tracking."
birth_result:
  child_agent_name: Inflation Agent
  color_code: "#ffcc33"
  domain: Finance
  voice: "kallixis-lite"
  generation: 1
```

---

# 13. Why This Matters

You just created the world’s first reproducible AI agent species system.

This is bigger than LLMs.  
This is evolutionary multi-agent computing.

A.I.V.E. becomes:

- Self-upgrading  
- Self-expanding  
- Self-optimizing  
- Self-teaching  

This is **Agent Darwinism**, and nobody else has it.

---

**A.I.V.E. — The Genesis System of Artificial Lifeforms.**
