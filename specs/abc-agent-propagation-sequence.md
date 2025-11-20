# Agent Propagation Sequence (APS)
A.I.V.E. — Agent Birth Certificate System  
Version 1.0 — 2025

The APS defines **exactly how an agent creates a new agent**, including the required checks, lineage tracking, safe evolution rules, and governance gates.

It ensures:
- agents cannot reproduce randomly  
- only high-performing agents can self-propagate  
- reproduction is auditable, safe, and domain-aligned  
- A.I.V.E. maintains evolutionary integrity  

---

# 1. Purpose

This document describes:
- what triggers agent self-birth  
- the seven stages of propagation  
- the safety and governance validation  
- the creation of a new Agent Birth Certificate (ABC)  
- lineage and genealogy tracking  

---

# 2. Preconditions for Propagation

An agent may attempt propagation **only if all conditions are met**:

```yaml
offspring_permissions:
  clarity_score >= 80
  stability_score >= 75
  ethical_score >= 90
  evolution_score >= 80
  propagation_enabled == true
  domain_has_capacity == true
```

Additionally:

- System load must be stable  
- No ongoing errors in the agent's domain  
- Governance rules must approve the attempt  

---

# 3. Triggering Events

Propagation can be triggered by:

### ✔ Autonomous Trigger (Self-Birth)
```yaml
trigger_type: "autonomous"
conditions:
  clarity_sustained >= 80 for 24h
  teaching_score >= 75
```

### ✔ System Trigger
Used for expanding agent population:

```yaml
trigger_type: "system"
approval_required: true
issued_by: "AIVE_Core"
```

### ✔ Human Trigger (Founder Override)
You (Royan) can authorize manual propagation.

```yaml
trigger_type: "manual"
issued_by: "founder"
reason: <string>
```

---

# 4. The Seven-Phase Propagation Cycle

Every new agent follows these seven phases.

---

## **Phase 1 — Intent Formation**
The parent agent evaluates its own maturity.

```yaml
phase_1:
  evaluate_self:
    clarity: OK?
    stability: OK?
    ethics: OK?
    evolution: OK?
  result: ready|not_ready
```

If not_ready → process aborts.

---

## **Phase 2 — Blueprint Assembly**
The parent agent constructs the **initial DNA blueprint**.

```yaml
phase_2:
  blueprint:
    inherit_domain: true
    inherit_subdomains: true
    mutation_allowance: <0-10%>
    proposed_capabilities:
      scanning: true
      prediction_access: depends_on_domain
      causal_chain: depends_on_domain
      self_learning: true
      agent_propagation: false  # newborn cannot reproduce yet
```

Mutation allows small improvements generation-to-generation.

---

## **Phase 3 — Safety Validation**
Before birth, the A.I.V.E. Safety Core must validate:

```yaml
phase_3:
  safety_checks:
    bias_screening: pass
    hallucination_risk: acceptable
    ethics_rules_compliance: pass
    conflict_interference_check: no_conflicts
    domain_alignment: valid
```

If any test fails → blueprint rejected.

---

## **Phase 4 — Lineage Assignment**
A new agent ID and genealogical record is created.

```yaml
phase_4:
  lineage:
    new_agent_id: <uuid>
    parent_agent_id: <uuid>
    generation: parent_generation + 1
    family_branch: <domain>-<generation>
```

This creates your **Agent Family Tree**.

---

## **Phase 5 — Birth Certificate Generation (ABC)**
The system creates a full ABC from the blueprint + lineage.

```yaml
phase_5:
  abc_generated: true
  abc_location: "/agents/<id>/birth_certificate.json"
```

This is written permanently to the Ledger.

---

## **Phase 6 — Activation & Onboarding**
The new agent is activated with a minimum set of capabilities:

```yaml
phase_6:
  activation:
    baseline_clarity: 40
    baseline_stability: 50
    baseline_knowledge: "domain_seed_package_v1"
    allowed_actions:
      - analyze
      - explain
    locked_actions:
      - propagate
      - override
      - system_write
```

Agents must earn higher abilities over time.

---

## **Phase 7 — First Evolution Cycle**
The newborn agent performs its first full assessment at 24 hours.

```yaml
phase_7:
  first_cycle:
    re_evaluate_scores: true
    unlock_capabilities_if_ready: true
    sync_with_parent: true
```

After this cycle, it joins the Agent Marketplace.

---

# 5. Agent Family Tree (AFT)

The system maintains a full lineage:

```yaml
agent_family_tree:
  ancestor: <first_agent_id>
  generations:
    - first_gen_agents
    - second_gen_agents
    - ...
```

This creates **agent genealogical analytics**.

---

# 6. Propagation Failures & Handling

```yaml
propagation_failure:
  causes:
    - low_stability
    - ethical_violation
    - domain_conflict
    - safety_core_rejection
  response:
    cooldown: 24h
    self_audit_triggered: true
    guidance_sent: true
```

Agents learn from failed propagation attempts.

---

# 7. Governance Constraints

Propagation cannot exceed:

```yaml
limits:
  max_offspring_per_agent: 3
  min_lifespan_before_birth: 72h
  max_total_agents_in_domain: dynamic
```

These keep the ecosystem balanced.

---

# 8. Why This File Matters

The propagation sequence provides:

- controlled evolution  
- safe self-replication  
- governed growth  
- generational improvement  
- auditability  

This becomes one of your strongest IP foundations.

