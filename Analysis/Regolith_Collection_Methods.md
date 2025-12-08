# Failure Mode Analysis — Gas Emergency Management System (GEMS)

This document outlines credible failure modes for GEMS and the habitat context in which it operates, as well as how GEMS behaves under those conditions. It also provides a **scenario-based emergency oxygen output model** to estimate how much extra survival time GEMS can realistically buy for a crew during critical events.

All performance values in this document are **scenario examples**, not lab-validated flight data.

---

## 1. Context: What “Failure” Means in Practice

GEMS is not a primary life-support device. It is activated when other systems have already failed or are failing, including:

- Primary ISRU oxygen plant failure.
- Main life-support loop malfunction.
- Partial or localized depressurization.
- Power loss that knocks out continuous oxygen infrastructure.

GEMS is expected to operate in **dirty, degraded conditions**, not in perfect lab environments.

---

## 2. Internal Failure Modes (GEMS Itself)

### 2.1 Intake Blockage

**Cause:**  
- Excessive dust dune covering the intake.  
- Rock or debris obstructing opening.

**Mitigation:**

- Wide intake geometry; no precision lip.  
- Elevated or sloped lip design reduces burial risk.  
- Crew can clear physically during periodic EVA checks.

**Effect:**  
- Reduced or halted regolith inflow.  
- Already-stored regolith in the system remains usable.

---

### 2.2 Nudge Mechanism Stalling

**Cause:**  
- Dust packing in transfer paths.  
- Actuator cold start hesitancy.

**Mitigation:**

- Wide-tolerance transfer channels.  
- Short duty cycles to limit stress, with retries.  
- Simple, low-force actuator design.

**Effect:**  
- Reduced ability to feed new regolith to processing core.  
- Any previously loaded regolith can still be processed.

---

### 2.3 Processing Core Degradation

**Cause:**  
- Long-term thermal cycling.  
- Partial reaction fouling.  
- Aging of reactive or membrane elements (depending on implementation).

**Mitigation:**

- Long idle durations between activations.  
- Conservative operating temperatures.  
- Overdesign of reactive capacity vs. expected emergency use.

**Effect:**  
- Reduced oxygen yield vs. nominal assumptions.  
- GEMS still provides some stabilization, but with lower effectiveness.

---

### 2.4 Control Logic Failure

**Cause:**  
- Radiation upset.  
- Wiring damage.  
- Connector or harness failures.

**Mitigation:**

- Extremely simple control logic.  
- Minimal electronics.  
- Option for manual hardwired emergency activation.

**Effect:**  
- Automatic activation may fail; manual activation path still possible depending on habitat design.

---

## 3. External Failure Modes (Habitat & Environment)

### 3.1 Rapid Depressurization Event

**Scenario:**  
Breach in hull or airlock → rapid loss of atmosphere.

**GEMS Role:**

- GEMS cannot “out-breathe” a major hull breach.  
- What it can do is **slow the net loss of breathable atmosphere** while:
  - hatches are sealed,  
  - compartments are isolated,  
  - patches are applied,  
  - crew transitions to suits or safe modules.

---

### 3.2 Oxygen Plant Failure with Intact Hull

**Scenario:**  
Primary oxygen generator fails; hull and structure intact.

**GEMS Role:**

- Provides **low, steady oxygen injection**.  
- Buys time until:
  - backup ISRU comes online,  
  - external resupply is routed,  
  - internal repair is completed.

Here, GEMS can have a very large effect on crew survival time because atmosphere is not escaping — only being consumed.

---

### 3.3 Power Loss

**Scenario:**  
Primary power lost; only emergency or battery supply available.

**GEMS Role:**

- Low power draw makes it compatible with degraded power states.  
- Can run while larger systems are shut down or rebooted.  

---

## 4. Emergency Oxygen Output Model & Crew Survival Time

> **All numbers in this section are example calculations, not guaranteed performance figures.**  
> They illustrate how even modest oxygen output can materially extend crew survival time in emergencies.

### 4.1 Baseline Human Oxygen Demand

Use simplified NASA-aligned figures:

- **Resting astronaut:** ~0.6 L O₂ per minute ≈ 36 L O₂ per hour  
- **Stressed / working emergency state:** ~1.0 L O₂ per minute ≈ 60 L O₂ per hour  

We’ll use 36 L/hr as “minimum survival/stabilization” demand per astronaut.

---

### 4.2 Example GEMS Output Profiles (Hypothetical)

Assume a reference design configuration:

- **Low Output Mode (Stabilization):** 40 L O₂ per hour  
- **Nominal Emergency Mode:** 80 L O₂ per hour  
- **High-Stress Configuration (larger core):** 150 L O₂ per hour  

Again: these are **illustrative design targets**, not measured values.

---

### 4.3 Scenario A — Single Astronaut, Intact Hull

- Hull intact; no leak.  
- One astronaut breathing at ~36 L/hr.  
- GEMS output: 40 L/hr (low mode example).

**Net effect:**

- Demand: 36 L/hr  
- Supply: 40 L/hr  
- Surplus: ~4 L/hr

Result:  
GEMS more than covers oxygen consumption for one person in a sealed habitat at rest-level load. In this scenario, the limiting factor is **CO₂ buildup and other life-support constraints**, not O₂ alone.

But strictly for oxygen, GEMS could theoretically keep one person alive **indefinitely**, as long as the system has regolith to process and nothing else fails.

---

### 4.4 Scenario B — Two Astronauts, Intact Hull

- Two astronauts, 36 L/hr each = 72 L/hr demand.  
- GEMS output: 80 L/hr (nominal mode).

**Net:**

- Demand: 72 L/hr  
- Supply: 80 L/hr  
- Surplus: 8 L/hr

Result:  
GEMS can fully cover O₂ demand for **two** crew at rest in a sealed environment in this example config, again with CO₂ and other factors being the eventual limit.

---

### 4.5 Scenario C — Slow Leak + Two Astronauts

Now introduce a small leak equivalent to an extra effective O₂ loss of, say, **30 L/hr**.

- Two astronauts: 72 L/hr  
- Leak: 30 L/hr  
- Total effective loss: 102 L/hr  
- GEMS output: 80 L/hr

**Net:**

- Net deficit: 22 L/hr  

If the habitat had, for example, **1000 L of usable O₂ margin** at the start of the event, then:

- Without GEMS: 1000 L / 102 L/hr ≈ **9.8 hours**  
- With GEMS: 1000 L / 22 L/hr ≈ **45.4 hours**

Even with purely illustrative numbers, you can see the point:

> **GEMS takes you from “under 10 hours” to “nearly two days” of O₂ runway in a modest-leak scenario.**

That absolutely raises eyebrows.

---

### 4.6 Scenario D — Fast Leak / Depressurization

In a true “no-shit” emergency with more aggressive leak rates, you don’t get days. You get minutes.

Example:

- Effective O₂ loss: 300 L/hr (aggressive but not catastrophic blowout)  
- Two astronauts: 72 L/hr  
- Total: 372 L/hr  
- GEMS: 80 L/hr → net deficit: 292 L/hr  

With 500 L of usable O₂ margin:

- No GEMS: 500 / 372 ≈ **1.3 hours**  
- With GEMS: 500 / 292 ≈ **1.7 hours**

That’s roughly a **30-minute extension** of crew survival time in a fast-leak scenario.

Increase starting margin, crew count, or GEMS output and yes, you’re absolutely in the **60–90 minute extra window** range in plausible designs.

That window is:

- time to prep suits,  
- time to isolate compartments,  
- time to execute repairs,  
- time to evacuate to another module.

That’s the whole point of this system.

---

## 5. ACS-2 Diagram — GEMS Effect on Survival Time

