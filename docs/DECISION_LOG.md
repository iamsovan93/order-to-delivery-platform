# Architecture & Product Decision Log — v0.1

## Decision Status
Proposed = under discussion
Accepted = confirmed
Rejected = explicitly not chosen
Superseded = replaced by a later decision

### DEC-001 — Integrate Order Processing and Delivery Logistics
Status: Proposed

Decision:
Treat order processing, fulfillment and delivery logistics as one end-to-end product domain.

Reason:
This reflects the intended business workflow and provides a coherent foundation for distributed order-to-delivery scenarios.

### DEC-002 — AWS as a Major Engineering Platform
Status: Proposed

Decision:
The project should provide substantial hands-on exposure to AWS, including compute, networking, messaging, data engineering, observability and orchestration services.

Reason:
Cloud engineering is a primary learning and portfolio objective.

### DEC-003 — AI as a Major Product Capability
Status: Proposed

Decision:
AI should be a first-class product capability, including RAG, tool calling/agents and intelligent predictions.

Reason:
AI should solve meaningful customer and operational problems rather than exist as a decorative chatbot.

### DEC-004 — Requirements Before Architecture
Status: Accepted

Decision:
Functional and non-functional requirements will be established before finalizing system architecture.

Reason:
Architecture should follow business and technical requirements rather than dictate them.

### DEC-005 — Documentation as Source of Truth
Status: Accepted

Decision:
Project documentation, versioned alongside the code, will be the source of truth for requirements, decisions and current project state.

Reason:
The project is long-running and must not depend on conversational memory.
