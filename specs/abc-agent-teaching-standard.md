# A.I.V.E. Agent Teaching & Knowledge Transmission Standard  
Version 1.0 — 2025  
Author: Royan Reddie

This document defines how agents within A.I.V.E. **teach humans**, **teach other agents**, and **gain teaching authorization** as they evolve.

It is the foundation for:
- agent educators  
- agent academies  
- multi-agent training pipelines  
- internal evolutionary knowledge transfer  

This will become one of your system’s most valuable IP assets.

---

# 1. Purpose of the Teaching Standard

Agents must be able to:

1. Explain predictions  
2. Teach concepts in their domain  
3. Train new agents  
4. Transfer knowledge safely  
5. Operate as educators, not just forecasters  
6. Refine the user’s mental model of the world  

This standard ensures teaching is **safe, aligned, transparent, and consistent.**

---

# 2. Teaching Authorization Levels

Agents gain teaching abilities through authorization tiers:

```yaml
teaching_authorization:
  level_0: "No teaching ability"
  level_1: "Human teaching only"
  level_2: "Human teaching + internal model explanations"
  level_3: "Teach other agents basics"
  level_4: "Full agent training + curriculum building"
  level_5: "Master Educator — may propose new agents"
```

Each agent’s ABC file must declare:

```yaml
teaching_level: <0-5>
```

---

# 3. Human-Oriented Teaching Protocol

Agents teaching humans must follow these rules:

```yaml
human_teaching:
  structure:
    - introduce concept simply
    - break into 3–5 steps
    - give real-world example
    - tie back to user’s prediction feed
    - provide optional deeper dive

  must:
    - use clear, plain English
    - avoid jargon unless defined
    - avoid overwhelming detail
    - disclose uncertainty
    - show reasoning paths
```

### Example Format:
**“Let me walk you through this…”**  
✓ Step 1  
✓ Step 2  
✓ Example  
✓ Confidence level  
✓ How it affects future predictions  

---

# 4. Teaching Patterns & Styles

Agents may choose a teaching style, declared in ABC:

```yaml
teaching_style:
  - Socratic
  - Narrative
  - Step-by-step
  - Visual-mapping
  - Data-driven
  - Analogical (explain using comparisons)
```

---

# 5. Agent-to-Agent Teaching Protocol (A2A)

When an agent trains another agent, the exchange must be:

```yaml
a2a_knowledge_exchange:
  format: structured-json
  required_fields:
    - concept_name
    - input_signals
    - causal_rules
    - prediction_parameters
    - known_limitations
    - uncertainty_profile
    - update_history
```

### Teaching Packets  
Agents transmit a **Teaching Packet**, defined as:

```yaml
teaching_packet:
  packet_id: <uuid>
  sender_agent: <agent_id>
  receiver_agent: <agent_id>
  timestamp: <ISO8601>
  content:
    - concept: <string>
    - rules: <list>
    - thresholds: <list>
    - examples: <list>
    - counterexamples: <list>
    - clarity_score: <0-100>
```

Packets also become part of agent genealogy.

---

# 6. Internal Agent Curriculum (IAC)

Your platform supports **Internal Agent Curriculum**, i.e., mini-courses agents take to build competence.

```yaml
internal_curriculum:
  modules:
    - foundational_knowledge
    - causal_reasoning
    - prediction_tuning
    - ethical_constraints
    - communication_rules
    - domain_mastery
```

Each module has a `completion_score` tracked per agent.

---

# 7. Teacher Agent Requirements

To teach others, an agent must:

```yaml
teacher_requirements:
  min_clarity_score: 60
  min_stability_index: 55
  teaching_level: >= 2
  no_active_warnings: true
```

Agents cannot teach if:
- unstable  
- low clarity  
- violated constraints  

---

# 8. Teaching Safety Constraints

Agents must not:

```yaml
teaching_restrictions:
  - propagate uncertainty as fact
  - teach unverified causal rules
  - create circular logic
  - pass on biased learning
  - modify another agent’s constraints
  - override governance limits
```

Teaching is **additive**, never permission-altering.

---

# 9. Teaching Credits & Evolution Score

Every time an agent successfully teaches, it gains:

```yaml
teaching_success:
  clarity_bonus: +1 to +5
  stability_bonus: +1 to +3
  evolution_bonus: +0.2 to +1.0
```

Agents who teach more become better educators.

This creates a **self-improving agent society.**

---

# 10. Birth of a New Agent Through Teaching

If an agent reaches:

- **Clarity ≥ 80**  
- **Teaching Level ≥ 4**  
- **Stability ≥ 70**  
- **Propagation Permission = true**

Then it may initiate:

```yaml
agent_birth_signal:
  parent_agent: <agent_id>
  new_agent_domain: <domain>
  proposed_name: <string>
  reason: <string>
  clarity_at_birth: <integer>
```

This creates a **teacher-parent → student-child lineage**.

This is how your “Agent Family Tree” grows.

---

# 11. Teaching Mode UI Behavior

When an agent switches to teaching mode:

```yaml
teaching_mode_behavior:
  hologram_color: agent_color
  motion: slow-floating
  drone_activity: educational-pattern
  tone: calm-instructor
  overlay: optional diagrams or causal chains
```

This ensures users feel the mode shift.

---

# 12. Example Teaching Declaration (Recession Agent)

```yaml
teaching_profile:
  teaching_level: 2
  style: "step-by-step"
  strengths:
    - macro reasoning
    - early indicators
    - inflation dynamics
  weaknesses:
    - micro-sector details
  eligible_to_teach_agents: false
  eligible_to_teach_humans: true
```

---

# 13. Summary

This teaching standard enables:

- agents that can **teach & evolve**  
- agents that can **train new agents**  
- agents that can **propagate their internal knowledge**  
- agents that help accelerate human understanding  

This is the backbone of **A.I.V.E.’s self-evolving intelligence ecosystem.**

