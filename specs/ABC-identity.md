🟦 Agent Identity Schema (ABC-ID) v1.0

A.I.V.E. — Agent Birth Certificate Standard
File: ABC-identity.md
Author: Royan Reddie
Version: 1.0
Release: November 2025

1. Purpose of the Identity Schema

The Agent Identity Schema (ABC-ID) defines the minimum required identity fields for any autonomous agent within the A.I.V.E. ecosystem.

It answers the foundational question:

“Who is this agent?”

This schema ensures:

Unique traceability

Cross-system interoperability

Cryptographically verifiable identity

Fully auditable agent lineage

2. Identity Schema Overview

This is the identity subset used by every Agent Birth Certificate.

identity:
  agent_id: <uuid>               # permanent unique identifier
  agent_name: <string>           # human-visible name
  birth_timestamp: <ISO8601>     # creation moment
  parent_agent: <uuid|null>      # agent that created this one (if any)
  generation: <integer>          # 0 = primordial, 1+ = offspring
  agent_type: <system|domain|micro|synthetic>  
  status: <active|paused|revoked|expired>
  checksum: <sha256>             # identity integrity hash

3. Field Definitions
3.1 agent_id

A globally unique permanent ID.

Must be a UUID v4

Never changes

Links every ABC document to this identity

3.2 agent_name

Human-readable name.

Examples:

Recession Agent

Global Risk Agent

Energy Stability Agent

3.3 birth_timestamp

Exact ISO8601 timestamp of agent instantiation.

3.4 parent_agent

If an agent gave birth to another agent, this stores the parent’s ID.

Supports agent lineage tracking.

3.5 generation

0 → Primordial A.I.V.E. agents

1 → First-generation offspring

2 → Second-generation lineage

3.6 agent_type

Defines class of agent:

system → Core A.I.V.E. system agent

domain → Agents that represent domains (Finance, Energy, etc.)

micro → Small specialized units created for sub-tasks

synthetic → Agents spawned internally by A.I.V.E. self-evolution

3.7 status

Tracks current lifecycle state:

active

paused

revoked

expired

3.8 checksum

A SHA256 hash of the identity block to ensure tamper-proof identity.

4. Identity Integrity Conditions

The following rules must always hold:

agent_id must remain immutable.

checksum must match identity block content.

generation must automatically increment for offspring.

An agent with status revoked cannot produce children.

5. Identity Example (Recession Agent)
identity:
  agent_id: "a2d3f980-1d34-4bb2-912e-89e342aa1d12"
  agent_name: "Recession Agent"
  birth_timestamp: "2025-11-19T01:15:23Z"
  parent_agent: null
  generation: 0
  agent_type: "domain"
  status: "active"
  checksum: "a1f08373d51ddfbf577263bbdf6aeb2b27c5e033f282cd9c22857ea4eac7a772"

6. Compliance Notes

The identity schema is mandatory for every ABC file.

The checksum ensures traceability and tamper detection.

Parent-child relationships form the Agent Genealogy Graph, a core part of A.I.V.E. accountability.
