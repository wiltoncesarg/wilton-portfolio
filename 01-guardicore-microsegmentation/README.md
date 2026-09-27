# Case 01 — Guardicore / Microsegmentation

## Overview

Hands-on administration and operation of a Guardicore microsegmentation environment from proof of concept through production and ongoing operations.

## Context

The existing network perimeter and segmentation controls did not provide sufficient visibility and control over lateral communications. Guardicore was selected after a proof of concept to provide greater visibility and enable microsegmentation.

## Scale

- 450 licenses
- More than 350 production agents
- 3 internal Aggregators
- Management delivered as SaaS

## Technical Challenge

The challenge was to understand existing communication patterns, validate legitimate dependencies and progressively enforce policies without disrupting services.

## Operational Approach

```text
Request
  ↓
Agent installation
  ↓
Flow observation
  ↓
Communication analysis
  ↓
Policy refinement
  ↓
Validation
  ↓
Alert
  ↓
Block
  ↓
Post-enforcement monitoring
```

Flows are analyzed by origin, destination, IP, port, protocol, application, process, user and labels.

Policies are validated in Alert mode before progressing to Block.

## My Role

- Daily Guardicore administration
- Agent installation and requests
- Flow analysis
- Policy creation and refinement
- Validation before enforcement
- Investigation of blocked flows
- Release of legitimate communications
- Post-change monitoring
- Internal Aggregator administration
- SIEM and Kubernetes integration/orchestration
- Interaction with database, development, OS, storage, firewall, security and application teams

## Troubleshooting & Decisions

Blocked communications are investigated using flow context and service-owner validation to determine whether traffic is expected, required or indicative of an incorrect policy.

## Result / Impact

The platform increased visibility into application communications where documentation was not always complete, supporting controlled policy design, troubleshooting and progressive microsegmentation.

## Technologies

Guardicore · Microsegmentation · Windows · Linux · SIEM · Kubernetes · Network flows · Security policies
