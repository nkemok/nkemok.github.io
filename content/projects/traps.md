---
title: "Trap events management"
company: "SevOne SaaS"
role: "UX Designer + 6 months"
thumbnail: "/assets/projects/sev1.png"
weight: 1
---

#### Objective

Trap Events Management was redesigned to modernize how SNMP traps are received, configured, and acted upon within the platform. Traps play a critical role in real-time network monitoring, yet the existing experience treated them primarily as backend technical artifacts rather than actionable operational signals.

The objective was to create a cohesive workflow that strengthened secure trap ingestion, improved event visibility, and closed monitoring gaps caused by undiscovered devices. Rather than focusing solely on UI improvements, the goal was to transform traps into a reliable and proactive event management system that could scale with enterprise environments.

#### Problem statement

SNMP traps are asynchronous notifications sent by network devices to signal events such as failures, thresholds, or status changes. While powerful, they introduce complexity in configuration, ingestion, and interpretation.

The previous trap management experience presented several challenges. Configuration workflows lacked clarity, particularly as customers increasingly adopted SNMPv3 for enhanced security. The setup process was technical and error-prone, making it difficult for teams to confidently enable secure trap reception.

Once traps were received, the Logged Traps interface functioned largely as a raw event list. While technically comprehensive, it lacked the structure and filtering needed for efficient triage during high-volume alert scenarios.

A more critical gap emerged around unknown traps. When traps were received from devices not yet discovered in the system, they were visible but disconnected from any meaningful next step. Users could see the signal, but there was no integrated path to onboard the device generating it. This created operational blind spots, particularly in dynamic environments where new devices were frequently introduced.

The system was ingesting data successfully, but the experience failed to unify ingestion, visibility, and discovery into a seamless workflow.

![traps discovery](/assets/project/traps/traps-discovery.png)

#### Discovery

Discovery involved close collaboration with engineering, product, and customer-facing teams to understand both the technical underpinnings of trap ingestion and the operational pain points experienced by customers.

Technical discussions surfaced about the growing importance of SNMPv3 and the need for a more structured receiver model. At the same time, support insights revealed that teams often struggled to interpret trap volume and differentiate between meaningful signals and background noise.

The most compelling insight centered on unknown traps. These events represented early signals from devices not yet formally onboarded into the system. Instead of treating them as edge cases, they could be repositioned as proactive discovery triggers.

This reframed the initiative. The opportunity was not only to improve configuration and visibility, but to connect traps directly to device lifecycle management.

![traps reqs](/assets/project/traps/traps-reqs.png)

#### Design process

The redesign began with low-fidelity wireframes focused purely on workflow clarity. Early sketches explored how to separate configuration, logged traps, and unknown traps into distinct but connected experiences. The priority at this stage was information hierarchy and mental model validation, not visual refinement.

For the trap events editor, low-fi iterations tested different groupings of SNMPv3 fields to reduce cognitive load. Authentication, encryption, and credential inputs were reorganized multiple times to ensure a logical setup sequence. These wireframes were reviewed with engineering to validate technical alignment before investing in higher fidelity.
Mid-fidelity prototypes introduced interaction states and validation feedback. Real-time error messaging, receiver status indicators, and inline guidance were tested to reduce setup ambiguity. This phase focused heavily on preventing configuration fragility.

For logged traps, wireframes explored density and scanability. Multiple layout variations were evaluated to balance metadata visibility with readability under high-volume conditions. Filtering and contextual expansion patterns were refined through iteration to support faster triage.
The unknown traps workflow required the most conceptual exploration. Early concepts treated unknown traps as a separate static list. Iteration revealed that this reinforced the existing gap. The final direction integrated discovery directly into the event view, allowing users to initiate device onboarding from the trap itself. High-fidelity designs emphasized clear differentiation between known and unknown sources while surfacing actionable next steps.

The transition to high-fidelity design focused on clarity of state, visual hierarchy, and alignment with the broader SaaS design system. Status indicators, severity levels, and discovery prompts were refined to communicate system behavior without overwhelming users. Close collaboration with engineering ensured backend ingestion logic and frontend mental models remained consistent.

![traps events](/assets/project/traps/traps-events.png)

![unknown traps](/assets/project/traps/unknown-traps.png)

#### Final deliverables

The final solution included a redesigned trap events editor with integrated SNMPv3 Receiver configuration, enabling secure and reliable trap ingestion. The logged traps interface was enhanced to support efficient triage through improved hierarchy and filtering. A new unknown traps workflow connected event visibility directly to device discovery, closing monitoring gaps and strengthening operational continuity. High-fidelity prototypes and detailed specifications ensured accurate implementation and alignment across teams.

![batch action traps](/assets/project/traps/batch-action-traps.png)

The trap events management redesign transformed traps from a technical backend feature into a cohesive event management system. Secure SNMPv3 adoption became more accessible through clearer configuration workflows. Logged traps evolved into a usable operational tool for high-volume environments. Most significantly, unknown traps were repositioned as proactive discovery signals, reducing monitoring blind spots and improving responsiveness in dynamic enterprise networks. By unifying ingestion, visibility, and discovery, the experience now supports a more reliable, transparent, and scalable approach to real-time network event management.

![mib browser](/assets/project/traps/mib-browser.png)
