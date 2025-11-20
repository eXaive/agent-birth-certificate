🧬 ABC-propagation.md

Autonomous Agent Propagation Standard — v1.0
A.I.V.E — Awareness • Intelligence • Verification • Evolution
Author: Royan Reddie
Release: November 2025

1. Purpose of Propagation Standard

This document defines:

When an agent is allowed to create (“birth”) another agent

How that process works

What safety gates must be passed

What DNA is inherited

What capabilities may evolve

How lineage, generations, and governance are enforced

This is the foundation of the Agent Factory inside A.I.V.E.

Agents do not just operate;
They propagate strategically to expand intelligence coverage.

2. The Propagation Model

Agent propagation is structured around three key pillars:

2.1 Lineage

Every new agent has a parent and becomes part of a multi-generation tree.

2.2 Capability Growth

Offspring agents inherit core capabilities but adapt to a more specialized function.

2.3 Governance

Propagation is restricted to prevent runaway agent creation or unsafe reproduction.

Propagation is intentional, supervised, and evolution-driven — never random.

3. Conditions Required for Propagation

An agent may only attempt propagation when ALL of these criteria are met:

3.1 Clarity Score ≥ 80

Agent has mastered its domain.

3.2 Stability Index ≥ 75

Agent predictions, actions, and behavior are consistent.

3.3 Drift Risk = Low

No signs of hallucination, bias drift, or mission deviation.

3.4 Domain Gap Exists

A domain needed by the system is missing or underserved.

Example:
Recession Agent masters macroeconomic cycles →
System lacks a “Global Inflation Agent” →
Propagation permitted.

3.5 Propagation Permission = true

Within agent’s ABC DNS:

capabilities:
  agent_propagation: true

4. Propagation Steps (Self-Birth Pipeline)

When an agent meets propagation criteria, the following pipeline triggers:

[PARENT AGENT]  
   ↓
[propagation_request]  
   ↓
[child_domain_selection]  
   ↓
[self-birth ABC generation]  
   ↓
[verification]  
   ↓
[activation]  
   ↓
[parent logs child relation]


Every step must pass.

5. Propagation Request Structure

The parent agent constructs a Propagation Intent Packet.

propagation_request:
  parent_agent: <uuid>
  proposed_child_name: <string>
  proposed_domain: <string>
  justification: <string>
  timestamp: <ISO8601>


Example:

propagation_request:
  parent_agent: "a2d3f980-1d34-4bb2-912e-89e342aa1d12"
  proposed_child_name: "Inflation Agent"
  proposed_domain: "Finance.Inflation"
  justification: "Domain clarity saturation detected. Expansion required."
  timestamp: "2025-11-19T22:35:11Z"

6. Child Domain Selection Logic

The system helps determine the child domain based on:

parent domain

system gaps

global intelligence needs

trend detection

parent specialization

Example algorithm:

If (parent.domain == Finance)
     and clarity > 80
     and missing domain == Inflation
→ create Inflation Agent


This is the Agent Priortization Matrix (APM).

7. Child ABC Generation Rules

When a new agent is created, its ABC uses a combination of:

7.1 Inherited DNA

ethical rules

core design constraints

allowed actions

lineage and generation index

7.2 Adapted DNA

Reflects the child’s specific domain.

7.3 Fresh DNA

Independent attributes:

new AID

new voice identity

new color identity

new clarity = baseline (30–40)

new stability = baseline (50–60)

Example:

child_abc:
  parent_agent: "a2d3f9..."
  generation: 1
  color_code: "#d946ef"
  voice_profile: "elara"
  clarity_score: 35
  domain: "Finance.Inflation"

8. Verification Gate for Child Agents

Every propagated agent must pass:

8.1 Sandbox Boot Test

Child agent executes base capabilities safely.

8.2 Constraint Check

Child cannot exceed parent’s power.

8.3 Mission Alignment Scan

Ensures domain match and no cross-domain overreach.

8.4 Drift Guard Activation

Early drift-prevention guardrails.

If a child fails verification →
It is archived and the parent is notified.

9. Parent-Child Lineage Structure

Each time propagation occurs, the parent logs:

reproduction:
  children:
    - child_agent_id: <uuid>
      birth_timestamp: <ISO8601>
      domain: <string>
      generation_index: <int>


Child logs:

identity:
  parent_agent: <uuid>
  generation: <int>


This builds your agent family tree.

10. Generational Rules
Generation 0

Primordial agents (manually created).

Generation 1+

Agents born from other agents.

Generation rules:

each generation has stricter constraints

each generation becomes more specialized

parent cannot produce general-purpose agents

This prevents runaway replication.

11. Propagation Rate Limits

To avoid agent explosion:

One parent → one child per 24 hours

(hard-coded, future configurable)

Propagation cooldown: 24 hours
Total system propagation cap per week: 12

These can be validators inside your governance module.

12. Propagation Success Metadata

Upon successful propagation:

propagation_result:
  status: "success"
  child_agent_id: <uuid>
  domain: <string>
  generation: <int>
  timestamp: <ISO8601>
  notes: "Child passed verification and was activated."

13. Propagation Failure Metadata

If the new agent fails any checkpoint:

propagation_result:
  status: "failed"
  error_stage: "verification"
  reason:
    - "constraint_violation"
  timestamp: <ISO8601>


Parents may be penalized if failure was due to unsafe intentions (future).

14. Propagation API Endpoints (Future)
Endpoint	Purpose
/propagation/request	Create propagation request
/propagation/genesis	Generate child ABC
/propagation/verify	Sandbox + safety testing
/propagation/activate	Launch child agent
/propagation/lineage	Retrieve family tree
/propagation/history	Retrieve all propagation logs
15. Full Example — Inflation Agent Born From Recession Agent
propagation_request:
  parent_agent: "a2d3f980-1d34-4bb2-912e-89e342aa1d12"
  proposed_child_name: "Inflation Agent"
  proposed_domain: "Finance.Inflation"
  justification: "Clarity exceeded 80. Inflation domain unserved."

child_abc:
  identity:
    agent_id: "be88c5dc-8f32-45a2-bad1-4f8d3a598e98"
    agent_name: "Inflation Agent"
    parent_agent: "a2d3f980-1d34-4bb2-912e-89e342aa1d12"
    generation: 1
    birth_timestamp: "2025-11-19T22:42:53Z"
  domain:
    primary_domain: "Finance"
    subdomains:
      - "Inflation"
      - "Pricing"
  appearance:
    color_code: "#d946ef"
    icon: "🔥"
  capabilities:
    scanning: true
    prediction_access: true
    causal_chain: false
    self_learning: true
    agent_propagation: false
  evolution:
    clarity_score: 34
    stability_index: 58
