Phase1/Prototype_Hardware_Definition.md
Purpose

This document defines the exact hardware scope of the Phase 1 GEMS prototype.
Its purpose is to remove ambiguity: what exists, what does not, what is tested, and what is explicitly deferred.

Phase 1 hardware exists to test feasibility and failure behavior, not performance, optimization, or mission integration.

Phase 1 Test Article — Definition
Canonical Name

GEMS Phase 1 Prototype (GEMS-P1)

Functional Intent

A passive, always-ready emergency gas-handling test article that demonstrates:

Passive intake and capture geometry

Gravity-assisted or geometry-assisted internal routing

Dormant survival behavior

Deterministic emergency activation behavior

Predictable failure modes (clogging, partial blockage, dust intrusion)

Physical Configuration
Overall Form

Single, self-contained hardware unit

Static installation (no mobility)

Bench-top or floor-mounted testable

No requirement for vacuum, lunar gravity, or cryogenic operation in Phase 1

Structural Components

Rigid outer housing (metal or polymer acceptable)

Internal partitioning defining:

Intake region

Capture / settling region

Routing channel(s)

Output interface

Geometry Rules

Geometry-driven behavior preferred over active mechanisms

No precision tolerances required

Dust-tolerant clearances

Internal surfaces may be rough, coated, or untreated

Intake & Capture Subsystem
Intake

Always-open intake geometry

No valves, shutters, or moving parts

Orientation-agnostic where practical

Capture Behavior

Relies on:

Expansion

Settling volume

Flow redirection

No electrostatic, magnetic, or powered assistance

Phase 1 Validation Focus

Does material enter the system as intended?

Does it remain inside rather than re-entraining?

What happens when intake is partially obstructed?

Routing / Feed Subsystem
Routing Method

Passive routing only:

Gravity

Geometry

Cross-section changes

No augers, pumps, blowers, or actuators

Feed Continuity

Continuous flow not required

Intermittent or stalled behavior is acceptable and expected

Bridging, rat-holing, and clogging are valid test outcomes

Phase 1 Validation Focus

Does material move at all?

Where does it stop?

Can blockage be predicted by geometry alone?

Output Interface
Output Definition

Single physical outlet

May terminate into:

Collection bin

Bag

Dummy interface plate

Interface Rules

No pressure requirements

No sealing requirements

No downstream system assumptions

Dormant / Emergency Behavior
Dormant State

System remains passive and inert indefinitely

No warm-up

No active monitoring

No power draw (except optional sensors)

Emergency Activation (Phase 1 Definition)

Activation may be manual or simulated

Purpose is to validate:

Transition from dormant to active routing

Deterministic behavior during first activation

Important Constraint

Phase 1 does not prove real emergency performance — only that the transition logic is understandable and testable.

Power & Electronics (Strictly Limited)
Allowed

Temporary instrumentation:

Mass measurement

Visual inspection aids

Basic sensors (optional)

Data logging for test observation only

Forbidden

Closed-loop control

Automation

Feedback-driven behavior

Any electronics required for core functionality

If electronics fail, the system is considered to have behaved correctly.

Materials
Allowed

Metals

Polymers

Composites

Off-the-shelf fasteners

Not Required

Space-rated materials

Radiation tolerance

Thermal cycling survival

Explicit Exclusions (Non-Negotiable)

The Phase 1 prototype does not include:

Continuous gas production claims

Oxygen purity guarantees

Pressure vessels

Habitat integration

Vacuum operation

Cryogenic operation

Autonomous decision-making

Redundancy systems

Production manufacturing constraints

Any of the above belong to later phases or Theory-only work.

Failure Behavior (Desired, Not Avoided)

Phase 1 explicitly allows:

Clogging

Partial burial

Dust intrusion

Flow stoppage

Uneven performance

These are data, not defects.

Phase 1 Success Conditions (Hardware-Specific)

The prototype definition is successful if:

A third party could build GEMS-P1 without inventing missing subsystems

Every failure mode has a physical explanation

No behavior depends on hidden control logic or operator intervention
