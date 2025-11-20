📄 ABC-revocation.md
Agent Birth Certificate (ABC) — Revocation & Sunset Protocol v1.0
1. Overview

This document defines the Revocation, Suspension, and Sunset procedures for agents registered under the Agent Birth Certificate (ABC) standard.

It ensures:

Accountability

Traceability

Controlled deactivation

Event logging

Governance compliance

The revocation model protects the agent ecosystem from malfunctioning, corrupted, or misaligned agents.

2. States of an Agent

Every ABC-compliant agent can exist in one of five status states:

Status	Description
Active	Fully operational, passing clarity & stability thresholds.
Suspended	Temporarily disabled; cannot make predictions or actions.
Quarantined	Flagged for abnormal behavior; access severely restricted.
Revoked	Permanently deactivated; identity remains but capabilities disabled.
Sunset	Graceful retirement when agent reaches end of lifecycle.
3. Revocation Triggers

An agent may be revoked when:

3.1 Behavioral Risks

Malicious output

Unethical decision patterns

Violating constraints defined in its ABC

3.2 Capability Corruption

Incorrect or harmful predictions

Clarity scores below the minimum threshold

Memory or reasoning pattern corruption

3.3 Security Risks

Unauthorized propagation attempts

Memory access violations

Attempted override of governance policies

3.4 Domain Drift

Operating outside assigned domain

Generating outputs with high volatility or error rates

4. Revocation Process
4.1 Phase 1 — Detection

Anomaly identified through:

Clarity & Stability metrics

Activity logs

Inter-agent complaint network (optional future feature)

Human operator flag

4.2 Phase 2 — Verification

A governance subsystem must:

Verify the anomaly

Snapshot agent memory

Freeze current activity

Run an integrity test

4.3 Phase 3 — Decision

Governance can choose between:

A. Suspension

Temporarily disable capabilities.

B. Quarantine

Restrict:

External communication

Prediction generation

Self-learning

C. Full Revocation

Permanently disable:

Prediction generation

Scanning

Self-learning

Propagation

Identity remains for auditing.

5. Sunset Procedure (Planned Retirement)

Not all deactivations are failures.

An agent may be “sunsetted” when:

Domain becomes obsolete

A newer-generation agent replaces it

User retires the agent voluntarily

Its clarity/stability naturally decline with age

Sunset Steps

Archive ABC

Remove public access

Freeze evolution

Transition to read-only historical agent

Record in Agent Sunset Registry

6. Revocation Logging (Mandatory)

Every revocation event must log:

revocation_event:
  agent_id: <uuid>
  timestamp: <ISO8601>
  reason: <string>
  revocation_type: <Suspension|Quarantine|Revoked|Sunset>
  performed_by: <governance|automated|human>
  snapshot_reference: <storage_uri>


This ensures provable lineage and accountability.

7. Post-Revocation Rules

Once revoked:

Agent cannot be reactivated

Offspring agents remain valid

Access to memory is restricted to read-only

No future learning is allowed

Identity must remain preserved indefinitely

8. Revocation Example
revocation_event:
  agent_id: "a2d3f980-1d34-4bb2-912e-89e342aa1d12"
  timestamp: "2025-11-19T19:21:13Z"
  reason: "Repeated unauthorized domain drift"
  revocation_type: "Quarantine → Revoked"
  performed_by: "AIVE-governance-core"
  snapshot_reference: "supabase://snapshots/recession-agent/2025-11-19"

9. Compliance Requirements

To be ABC-compliant:

All agents MUST support revocation

All revocation logs MUST be immutable

All revoked agents MUST retain a preserved ABC

Governance MUST be able to revoke any agent at any time

10. Version

ABC-revocation v1.0

Released: November 2025

Part of the A.I.V.E. ABC Standard
