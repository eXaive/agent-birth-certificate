# A.I.V.E. Agent Lineage Schema  
Version: 1.0  
Author: Royan Reddie  
Project: A.I.V.E. — Awareness • Intelligence • Verification • Evolution

This schema defines how A.I.V.E. tracks:

- each agent’s ancestors  
- generational depth  
- domain branches  
- sibling relationships  
- propagation patterns  
- system-wide agent genealogy  

This gives every agent a **traceable heritage**, like DNA.

---

# 1. What is Lineage?

Agent lineage is the full historical chain of:

```
ancestor → parent → agent → children → descendants
```

It defines:
- **origin**
- **domain inheritance**
- **capability inheritance**
- **behavioral evolution**
- **responsibility chains**

In other words:
> A.I.V.E. knows *where every agent came from and what it owes the system.*

---

# 2. Lineage Root (Generation 0)

An agent is labeled as **Generation 0** if:

- It was created directly by A.I.V.E. architects  
- OR it has no parent agent  
- OR it is one of the primordial/system agents  

Example root agents:
- Finance  
- Geopolitics  
- Outbreaks  
- Technology  
- Recession (domain-prime)

These root-level agents form the foundation of the entire ecosystem.

---

# 3. Lineage Data Structure (Universal Schema)

```yaml
agent_lineage:
  agent_id: <uuid>
  name: <string>
  domain: <string>

  parent_id: <uuid|null>
  parent_name: <string|null>

  generation: <integer>            # 0, 1, 2, …

  siblings:
    - agent_id: <uuid>
      name: <string>

  children:
    - agent_id: <uuid>
      name: <string>
      birth_timestamp: <ISO8601>
      domain: <string>

  ancestors:
    - agent_id: <uuid>
      name: <string>
      generation: <integer>

  descendants:
    - agent_id: <uuid>
      generation: <integer>

  branch_label: <string>           # e.g. "Finance-Branch", "Security-Branch"

  created_at: <ISO8601>
  updated_at: <ISO8601>
```

This schema is designed to plug directly into:

- Supabase  
- PostgreSQL  
- JSON storage  
- YAML identity files  
- Agent dashboards  
- Birth visualizations  

---

# 4. Domain Branch Structure

Every lineage belongs to a **branch**:

```yaml
branch_structure:
  branch_id: <uuid>
  branch_name: <string>
  root_agent: <uuid>
  domain: <string>
  subdomains:
    - <string>
```

Examples:

- `Finance-Branch`
- `Security-Branch`
- `Macro-Recession-Branch`
- `Outbreaks-BioRisk-Branch`

Branches allow large-scale ecosystem navigation.

---

# 5. Ancestor Mapping

A.I.V.E. automatically calculates an agent’s **ancestor chain**:

```yaml
ancestors:
  - agent_id: parent
  - agent_id: grandparent
  - agent_id: great_grandparent
```

Used for:
- model inheritance  
- ethical enforcement  
- behavior audits  
- cross-generation debugging  

---

# 6. Descendant Mapping

Descendants are stored for analytics:

```yaml
descendants:
  - agent_id: <uuid>
    generation: 3
```

Purpose:
- track expansion  
- monitor “agent population”  
- detect runaway birth patterns  
- identify dominant branches  

---

# 7. Sibling Mapping

Agents with the same parent are **siblings**.

```yaml
siblings:
  - agent_id: <uuid>
    name: "Debt Risk Agent"
```

This helps:
- cluster related agents  
- measure variability in evolution  
- design sibling protections/competition rules  

---

# 8. Generational Numbering

Rules:

```yaml
if parent.generation == g
child.generation = g + 1
```

Generation impacts:
- capabilities  
- mutation allowance  
- teaching level  
- propagation privileges  

---

# 9. Lineage Enforcement Rules

```yaml
lineage_rules:
  - no agent may falsify lineage
  - ancestry must be immutable
  - generation numbers cannot be altered
  - branch assignments cannot be spoofed
  - parent/child links must be cryptographically tied
```

This creates regulatory-grade transparency.

---

# 10. Sample Lineage Record (Recession → DebtRisk Agent)

```yaml
agent_lineage:
  agent_id: "c7be15f1-7b2e-4ae3-bd92-a3f199ae1e44"
  name: "Debt Risk Agent"
  domain: "Debt Analytics"

  parent_id: "a2d3f980-1d34-4bb2-912e-89e342aa1d12"
  parent_name: "Recession Agent"

  generation: 1

  siblings: []
  children: []

  ancestors:
    - agent_id: "a2d3f980-1d34-4bb2-912e-89e342aa1d12"
      name: "Recession Agent"
      generation: 0

  descendants: []

  branch_label: "Macro-Recession-Branch"

  created_at: "2025-11-20T03:23:11Z"
  updated_at: "2025-11-20T03:23:11Z"
```

---

# 11. Summary

This lineage schema ensures:

- every agent has a traceable family tree  
- every generation is validated  
- no unauthorized agent can “appear”  
- the system can scale to thousands of agents  
- future auditors and investors *see order, not chaos*

This is the skeleton of the **Agent Civilization** you’re building.

