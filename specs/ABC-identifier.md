Agent Identifier Specification (AID) — v1.0

A.I.V.E — Awareness • Intelligence • Verification • Evolution
Author: Royan Reddie
Release: November 2025

The Agent Identifier (AID) defines the unique, permanent, cryptographically verifiable identity assigned to an agent at the moment of birth (creation).
It is the cornerstone of agent lineage, governance, traceability, and revocation.

1. Purpose of the AID System

The Agent Identifier ensures:

Agents have globally unique, collision-resistant identities

Agents cannot impersonate or replace each other

Lineage (which agent created which) is preserved

Governance + audit logs map cleanly to identity

Revocation and reproducibility remain possible

Agents remain accountable across their entire lifecycle

The AID is the “Social Security Number / UUID / DNA string” of your agent ecosystem.

2. Structure of an AID

Every AID must follow this structure:

AID:<version>:<uuid>:<checksum>


Example:

AID:1:a2d3f980-1d34-4bb2-912e-89e342aa1d12:9F4A

3. Field Definitions
3.1 Version Field
AID:<version>:...


Version of the identifier specification.

1 = standard UUID-based identity

future versions may incorporate cryptographic signatures, blockchain anchors, etc.

3.2 UUID Field

The core of the identity.

Rules:

must be a valid v4 UUID

must be immutable

generated at birth only

cannot be reused

cannot be overwritten

Example:

a2d3f980-1d34-4bb2-912e-89e342aa1d12

3.3 Checksum Field

A lightweight checksum used for:

corruption detection

transmission integrity

validation during lineage checks

Example: 9F4A

Computation:

first 4 hex characters of SHA-1(uuid + version)

4. Identity Requirements

To qualify as a valid AID:

Requirement	Description
Immutable	Cannot be altered after birth
Permanent	Survives evolution, reproduction, suspension
Unique	Must not collide within the ecosystem
Verifiable	Must pass checksum + format validation
Traceable	Must be logged at birth and across all actions
Serializable	Must work in JSON, SQL, YAML, binary
5. Validation Rules

An AID is valid if all conditions pass:

Matches regex:

^AID:[0-9]+:[0-9a-fA-F-]{36}:[0-9a-fA-F]{4}$


UUID is version 4

Checksum matches SHA-1 rule

Not found in revocation list

Not present in death registry

6. Identity Lifecycle

Identity persists through:

Birth → Active

Active → Suspended

Suspended → Reactivated

Active → Evolved

Active → Revoked

Revoked → Archived

Archived → Immutable historical record

Agents never lose their original AID.

Evolution does NOT issue a new AID — it issues a Revised Birth Certificate, but keeps the original identity.

7. AID in the Agent Birth Certificate

The ABC stores AID under:

identity:
  agent_id: "AID:1:a2d3f980-1d34-4bb2-912e-89e342aa1d12:9F4A"


This is the canonical home of the identifier.

8. AID JSON Schema Snippet
{
  "agent_id": {
    "type": "string",
    "pattern": "^AID:[0-9]+:[0-9a-fA-F-]{36}:[0-9a-fA-F]{4}$",
    "description": "Permanent, immutable Agent Identifier"
  }
}

9. Example AID Block
identity:
  agent_id: "AID:1:f3b2a981-22bb-4eab-9034-12de903f1d98:3A9C"
  agent_name: "Recession Agent"
  birth_timestamp: "2025-11-19T01:15:23Z"
  parent_agent: null
  generation: 0

10. Security Considerations

AID MUST NOT contain personal human data

AID MUST NOT encode capabilities

AID MUST NOT leak internal system secrets

AID MUST be validated before every privileged action

AID MUST be logged in all audit events

If future cryptographic versions (v2+) are introduced:

keys must be rotated

signatures must be verifiable via public registries
