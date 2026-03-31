---
title: "Flow explorer"
company: "SevOne SaaS"
role: "UX Designer + 6 months"
thumbnail: "/assets/projects/flow.png"
weight: 2
---

#### Objective

Flow explorer was initially positioned as a usability improvement initiative. However, early analysis revealed a deeper opportunity: users were not only struggling to navigate flow data — they were struggling to trust it.

Enterprise customers manage thousands of devices and interfaces generating high volumes of network flow data. Misconfigured ingestion rules, unclear interface permissions, and inconsistent device-level policies slowed troubleshooting and increased operational risk.

The objective evolved into a systems-level redesign that would:

- reduce time-to-insight during network investigations
- increase transparency into flow ingestion across devices and interfaces
- enable scalable governance through rule-based ingestion management
- align configuration and exploration into a cohesive experience

The goal was to transform flow explorer from a visualization tool into a governed, scalable flow management ecosystem.

#### Problem statement

Flow explorer surfaced complex traffic data, but the ingestion logic determining what data was available lacked visibility and clarity.
Users managing multi-interface devices could not easily determine which interfaces were allowing or disallowing flow ingestion, how rule
inheritance behaved across device groups, and whether missing data was caused by traffic behavior or misconfiguration.
Because many devices allow flow across multiple interfaces, rule precedence and overrides introduced technical edge cases that were
difficult to understand. These gaps created ingestion ambiguity, excess data collection, and longer troubleshooting cycles.
Configuration and exploration had been designed as separate systems, yet users experienced them as one continuous workflow.
The friction in analysis was often rooted in governance.

#### Discovery

Cross-functional discovery sessions mapped the full lifecycle of flow data — from ingestion rule creation to anomaly investigation.
Support ticket reviews revealed that troubleshooting frequently began with verifying whether flow data had been ingested correctly before analysis could begin.
Technical deep-dives uncovered additional complexity around device-level flow permissions, interface-level overrides, hierarchical rule inheritance, conflict resolution behavior.
This discovery phase reframed the initiative. Rather than optimizing isolated UI components, the solution required making ingestion logic visible, explainable, and manageable at scale.
Stakeholders aligned around a unified vision: connect governance and exploration into a single, transparent system.

![flow requirements](/assets/project/flow/flow-requirements.png)

#### Design process

A simplified mental model for ingestion governance was developed by mapping backend rule inheritance and multi-interface device
behavior into a clear hierarchical framework. Close collaboration with engineering ensured that the frontend experience
accurately reflected backend logic, preventing discrepancies between system behavior and user expectations.

![flow low-fi](/assets/project/flow/flow-low-fi.png)

The flow interface manager was introduced as a centralized control layer for managing ingestion across devices and interfaces.

The design emphasized hierarchy, state clarity, and relational context. Users gained system-wide visibility into ingestion coverage and could quickly identify misconfigured interfaces.

Special consideration was given to devices that allow flow across multiple interfaces. Rule precedence and override
behavior were made explicit through clear visual indicators, reducing ambiguity and preventing silent conflicts. This shifted ingestion management from reactive troubleshooting to proactive governance.

A scalable flow rules system was designed to support device-level rule application, interface-level overrides, and bulk policy management.
A core principle of the framework was explainability. Each rule state communicates both status and cause, allowing administrators to understand how inheritance and overrides impact ingestion behavior.
Iterative prototyping and validation ensured that flexibility did not introduce fragility. The result was a governance system capable of scaling across thousands of interfaces while maintaining clarity and predictability.
With ingestion governance clarified, Flow Explorer itself was restructured to reduce cognitive friction and accelerate anomaly detection.

Stronger visual hierarchy, persistent filtering controls, and streamlined drill-down patterns improved investigative efficiency.
Because ingestion status was now transparent and reliable, users could move directly into traffic analysis without questioning data completeness.

![flow make devices](/assets/project/flow/make-flow-devices.png)

#### Final deliverables

- Redesigned flow explorer with improved hierarchy and faster troubleshooting workflows
- Flow interface manager for centralized ingestion visibility and control
- Scalable flow rules framework supporting multi-interface device governance
- Clear rule precedence and inheritance modeling
- High-fidelity prototypes and implementation-ready specifications

![flow rules](/assets/project/flow/flow-rules.png)

By connecting configuration and exploration, the redesign reduced ingestion ambiguity and improved troubleshooting
efficiency in complex enterprise environments.
The introduction of governance visibility and scalable rule management strengthened user confidence in flow data integrity.
The flow explorer evolved from a dense visualization interface into a transparent, governed system capable of supporting enterprise-scale network operations.

![flow rules expanded](/assets/project/flow/flow-rules-expanded.png)
