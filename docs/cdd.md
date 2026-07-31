# ngGONG High Level Software Conceptual Design Document

**Project:** Next-Generation Ground-based Solar Observing Network (`ngGONG`)  
**Document:** High Level Software Conceptual Design Document (`HCDD`)  
**Review Context:** Conceptual Design Review (`CoDR`)  
**Status:** Draft

## Document Purpose

This document describes the conceptual design for ngGONG High Level Software
(`HLS`). It focuses on the software architecture, major subsystems,
responsibilities, key design decisions, logical decomposition, deployment
concept, major communication paths, external interfaces, and technical risks.

The goal of this document is to provide enough architectural clarity for CoDR
reviewers to determine whether:

- The HLS team understands the problem.
- The proposed architecture is sound.
- The major software risks have been identified.
- The architecture can realistically be carried into Preliminary Design Review
  (`PDR`).

## Scope

### In Scope

TODO: Define the boundaries of the HLS conceptual design.

At minimum, this section should identify:

- The HLS responsibilities within ngGONG.
- The major software systems and subsystems covered by this document.
- The architectural concerns addressed at CoDR.
- The level of detail appropriate for conceptual design.

### Out of Scope

The HLS Detailed Requirements Document (`HLS DRD`) defines the high-level
software requirements. Requirements should be referenced or traced here where
needed, but not repeated in full.

The Operations Concept Document (`OCD`) describes operational concepts and major
operational scenarios, including startup, observing, calibration, maintenance,
fault handling, and disconnected station operations. This document should
reference those scenarios where they affect architecture, but should not repeat
the operational concept in full.

The following items are out of scope for this CoDR-level document and belong at
PDR or later unless a limited conceptual example is needed:

- Detailed DDS topic definitions.
- Complete protobuf definitions.
- Detailed APIs.
- Complete Interface Control Documents (`ICDs`).
- Detailed state machines.
- Database schemas.
- Deployment scripts.
- Cybersecurity implementation details.
- Exhaustive verification matrix.

## Design Drivers

TODO: Describe the major drivers shaping the HLS architecture.

Potential drivers include:

- Continuous solar observing across six geographically distributed sites.
- Remote and local station operation.
- Reliability and fault tolerance.
- Observatory-wide coordination.
- Data flow from stations to downstream systems.
- Maintainability across a long system lifetime.
- Evolvability from conceptual design through PDR and implementation.

## Architecture Overview

TODO: Provide a concise overview of the proposed HLS architecture.

This section should explain:

- The overall architectural style.
- The separation between observatory-level and station-level software.
- The main responsibilities of HLS.
- The most important communication paths.
- How the architecture supports 24/7 solar observing.

### System Context

TODO: Add or reference a system context diagram.

The diagram should show ngGONG HLS in relation to the broader ngGONG system,
external systems, operators, engineers, scientists, and data consumers.

### HLS Context

TODO: Add or reference an HLS context diagram.

The diagram should show the boundary of HLS and the major systems with which it
interacts.

### HLS Decomposition

TODO: Add or reference an HLS decomposition diagram.

The diagram should show the primary HLS subsystems and their responsibilities.

## Major Software Components

TODO: Identify and describe the major HLS software components.

For each component, capture:

- Primary responsibility.
- Major inputs and outputs.
- Important dependencies.
- Operational role.
- Key design constraints or open questions.

### Observatory-Level Components

TODO: Describe software components that operate at the observatory level.

### Station-Level Components

TODO: Describe software components that operate at individual ngGONG stations.

### Shared Services and Libraries

TODO: Describe common services, libraries, frameworks, or utilities expected to
support the HLS architecture.

## Select Sequence Diagrams

TODO: Add a small number of informative sequence diagrams that clarify important
architecture-level behavior.

Candidate sequences:

- Typical observing sequence.
- Fault handling concept.
- Station startup.
- Observatory-to-station coordination.
- Disconnected station operation at a conceptual level.

These diagrams should remain conceptual. Avoid detailed API messages, complete
topic definitions, and implementation-level state transitions.

## Deployment Concept

TODO: Describe the conceptual deployment model for HLS.

This section should address:

- Station deployment concept.
- Observatory deployment concept.
- Major runtime environments.
- Expected deployment boundaries.
- Relationship between deployed components and physical sites.
- High-level operational dependencies.

### Station Architecture

TODO: Add or reference a station architecture diagram.

### Observatory Architecture

TODO: Add or reference an observatory architecture diagram.

### Software Deployment

TODO: Add or reference a software deployment diagram.

## Communication Paths

TODO: Describe the major communication paths used by HLS.

This section should summarize:

- Communication between observatory-level and station-level software.
- Communication between HLS and lower-level control systems.
- Communication between HLS and data systems.
- Communication between HLS and users or operator interfaces.
- Major assumptions about latency, availability, and disconnected operation.

### Communications Overview

TODO: Add or reference a communications overview diagram.

## External Interfaces

TODO: Identify external interfaces at a conceptual level.

This section should describe interface boundaries and responsibilities without
including complete ICDs, detailed APIs, protobuf definitions, or DDS topic
definitions.

Potential interface categories:

- Telescope and instrument control interfaces.
- Observatory control interfaces.
- Data management interfaces.
- Operator and engineering user interfaces.
- Site infrastructure interfaces.
- External monitoring, logging, or alerting interfaces.

## State Model

TODO: Describe the conceptual state model if needed to explain the architecture.

This section should remain high-level. Detailed state machines are out of scope
for CoDR and should be deferred to PDR unless a simplified state model is needed
to explain architectural behavior.

## Major Design Decisions

TODO: Summarize the key architectural decisions made for HLS.

For each decision, include:

- Decision statement.
- Context.
- Alternatives considered.
- Rationale.
- Consequences.
- Open issues, if any.

## Trade Studies

TODO: Include one- or two-page summaries of important trade studies where they
justify architectural decisions.

Each trade study summary should include:

- Question or decision being studied.
- Options considered.
- Evaluation criteria.
- Recommendation.
- Rationale.
- Risks or follow-up work.

## HLS DRD Traceability

TODO: Provide traceability from system-level needs to HLS requirements and then
to major architectural elements.

This section should reference the HLS DRD rather than repeat the full set of
requirements.

Suggested columns:

| System Need | HLS Requirement Reference | Architectural Element | Notes |
| --- | --- | --- | --- |
| TODO | TODO | TODO | TODO |

## Architecture Decision Summary

TODO: Provide a compact summary of the most important architectural decisions.

Suggested columns:

| Decision | Status | Rationale | Related Trade Study | Follow-Up |
| --- | --- | --- | --- | --- |
| TODO | TODO | TODO | TODO | TODO |

## Technical Risks and Mitigations

TODO: Identify major technical risks and planned mitigations.

Suggested columns:

| Risk | Impact | Likelihood | Mitigation | Owner | Status |
| --- | --- | --- | --- | --- | --- |
| TODO | TODO | TODO | TODO | TODO | TODO |

## Development Approach

TODO: Describe the planned software development approach at a conceptual level.

This section may include:

- Development phasing from CoDR toward PDR.
- Prototype or pathfinder work.
- Modeling, simulation, or integration strategy.
- Documentation strategy.
- Risk reduction activities.
- Expected evolution of architecture decisions.

## Open Questions

TODO: Track open architectural and documentation questions that need resolution
before or during CoDR preparation.

Suggested columns:

| Question | Context | Needed By | Owner | Status |
| --- | --- | --- | --- | --- |
| TODO | TODO | TODO | TODO | TODO |

## Appendix A: Candidate Diagrams

The following diagrams are candidates for inclusion if they materially clarify
the conceptual design:

- System context.
- HLS context.
- HLS decomposition.
- Station architecture.
- Observatory architecture.
- Software deployment.
- Communications overview.
- Typical observing sequence.
- Fault handling concept.
- State model.

## Appendix B: CoDR Review Question Checklist

Use this checklist to evaluate whether the document is addressing the expected
CoDR-level concerns:

- Does the document show that the HLS team understands the problem?
- Does the document present a sound architecture?
- Does the document identify the major software risks?
- Does the document show that the architecture can realistically be carried into
  PDR?
