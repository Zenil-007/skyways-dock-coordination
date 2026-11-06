# SkyWays Logistics — Dock Coordination Under Pressure

<p align="center">
  <strong>Understanding and solving truck-delay and warehouse dock-coordination challenges</strong>
</p>

<p align="center">
  <em>A guided capstone project | IIT Gandhinagar | AI-ML and Agentic AI Engineering</em>
</p>

---

## 🚛 The Problem at a Glance

*An overview of the operational challenges that can occur when trucks are delayed and warehouse appointments need to be coordinated.*


## 1. Introduction

SkyWays Logistics is a fictional freight and logistics company used as the setting for this capstone project.

The company coordinates shipments between transportation providers, truck drivers, warehouse operations teams, and customers. Each shipment follows a planned journey and is associated with a warehouse appointment and a suitable loading or unloading dock.

However, real-world transportation operations are unpredictable.

A truck may encounter traffic, vehicle problems, or other unexpected delays. Its estimated arrival time changes, potentially affecting its assigned warehouse appointment. At the same time, other trucks may also be delayed, docks may become unavailable, and warehouse schedules may already be operating near capacity.

What initially appears to be a simple appointment change can therefore become a much larger coordination problem.

**The central challenge is understanding how an individual truck delay affects the wider warehouse operation and how the resulting scheduling conflicts can be handled reliably.**

## 2. Understanding the Operational Problem

A truck's journey involves several interconnected stages:

1. **Shipment Planning:** A shipment is created with its origin, destination, cargo details, and planned arrival information.
2. **Driver and Vehicle Assignment:** A driver and suitable vehicle are assigned to the shipment.
3. **Appointment Booking:** A warehouse appointment and dock slot are allocated.
4. **Truck in Transit:** The truck travels towards its destination and may report changes to its estimated arrival time.
5. **Gate and Yard Check-in:** The warehouse records the truck's actual arrival and waiting status.
6. **Dock and Unloading:** The truck is assigned to a dock, unloading takes place, and the truck eventually exits.

Every stage depends on information from the previous stages. A disruption can affect the commitments made to other people and teams.

## 3. Problems Identified for Investigation

The following operational challenges are potential areas of investigation. Their frequency, severity, and root causes will be validated using the supplied dataset.

| # | Operational challenge | Why it matters |
|---|---|---|
| 1 | Double booking | Two trucks may be promised the same dock slot. |
| 2 | Multiple simultaneous delays | Several delayed trucks may compete for the same available capacity. |
| 3 | Changing ETAs | Repeated ETA updates can make the original schedule unreliable. |
| 4 | Dock incompatibility | An available dock may not support a particular vehicle or cargo type. |
| 5 | Dock breakdown | Maintenance or equipment failure can invalidate an existing appointment. |
| 6 | Unloading overruns | A longer-than-expected unloading process can delay subsequent appointments. |
| 7 | Yard congestion | Multiple arriving trucks can create queues and waiting time. |
| 8 | Early arrivals | Trucks arriving before their appointment may need to wait. |
| 9 | Ambiguous driver messages | A message may not clearly identify the relevant shipment or appointment. |
| 10 | Confirmation failures | A requested appointment change is not necessarily a confirmed change. |
| 11 | Priority conflicts | Different shipments may have competing operational priorities. |
| 12 | No-shows | A truck that does not arrive can leave allocated capacity unused. |

These challenges are interconnected. Solving one isolated issue without understanding its effect on the rest of the operation could create additional problems.

## 4. The Central Research Question

> When one or more trucks experience unexpected delays, how can warehouse operations identify the impact on existing appointments, determine feasible alternatives, and coordinate changes without creating additional scheduling conflicts?

This question will guide the project's initial research and problem discovery.

## 5. Who Is Affected?

The operational problem affects multiple stakeholders:

- **Truck Drivers:** Need clear instructions, updated appointment information, and reliable confirmation.
- **Dispatchers and Carriers:** Need visibility into vehicle availability and revised schedules.
- **Operations Coordinators:** Need to manage multiple exceptions without relying entirely on phone calls and manual tracking.
- **Warehouse Planners:** Need feasible dock appointments that respect capacity, equipment, and facility rules.
- **Customers and Consignees:** Need reliable information about shipment arrival times.

The challenge is not necessarily that any one stakeholder is making a mistake. Different stakeholders have different pieces of information, and those pieces must be reconciled.

## 6. Project Objectives

The initial objectives are:

1. Understand the complete truck-to-warehouse appointment lifecycle.
2. Investigate the operational challenges using the supplied database and historical records.
3. Identify the most significant pain point using evidence rather than assumptions.
4. Apply the Five Whys technique to identify its underlying root cause.
5. Define a focused solution with measurable success criteria.
6. Implement and test the selected solution.
7. Demonstrate its effectiveness against an appropriate baseline.

## 7. Data and Investigation

The capstone starter kit provides operational data and supporting materials, including:

- `skyways_freight_operations.db` — operational database.
- `dock_visit_history.csv` — historical dock visit records.
- `driver_messages_labelled.csv` — labelled driver messages.
- Database schema and data dictionary.
- Exploration notebooks and starter code.

The investigation will examine relevant information such as:

- Shipment and appointment records.
- Driver messages and ETA updates.
- Dock availability and status.
- Facility check-ins.
- Historical unloading durations.
- Appointment conflicts and operational exceptions.

The aim is to understand what actually happens in the supplied data before deciding what to build.

## 8. Proposed Solution Direction

The final solution has not yet been selected.

Potential directions include:

- A rule-based coordination and scheduling system.
- A machine learning solution for predicting operational outcomes.
- An Agentic AI system for handling driver exceptions and coordinating actions.
- A hybrid approach combining prediction and operational coordination.

The final direction will be chosen after analysing the data, identifying the root cause, and evaluating what can realistically be demonstrated within the capstone timeline.

## 9. Scope and Success Criteria

The project will focus on one clearly defined operational problem rather than attempting to automate the entire logistics operation.

The final scope will specify:

- The exact problem being solved.
- The users who will interact with the solution.
- The inputs and expected outputs.
- Operational constraints and safety guardrails.
- Measurable success criteria.
- Evidence demonstrating that the solution works.

No performance improvement or success claim will be made without supporting test results or measurements.

## 10. Repository Structure

The repository will progressively contain:

```text
skyways-dock-coordination/
│
├── README.md
│
├── docs/
│   ├── images/
│   │   └── skyways-problem-overview.png
│   ├── five-whys.md
│   ├── prd-lite.md
│   └── adr/
│       └── adr-001.md
│
├── notebooks/
│   └── data-exploration.ipynb
│
├── src/
│
├── tests/
│
├── data/
│
└── presentation/
```

*This is the planned structure and will evolve as the project develops.*

## 11. Project Status

**Current phase:** Problem Discovery

- [x] GitHub repository created.
- [x] Initial operational problem understood.
- [x] Potential operational challenges identified.
- [ ] Explore the supplied operational database.
- [ ] Measure and rank the identified problems.
- [ ] Complete Five Whys analysis.
- [ ] Finalise the problem statement.
- [ ] Define the PRD-lite and success criteria.
- [ ] Select the implementation track.
- [ ] Design, implement, and test the solution.
- [ ] Prepare the final demonstration and presentation.

---

## 12. Project Information

| Attribute | Details |
|---|---|
| Project | SkyWays Logistics |
| Theme | Dock Coordination Under Pressure |
| Programme | PG Diploma in AI-ML and Agentic AI Engineering |
| Institution | IIT Gandhinagar |
| Project Type | Guided Capstone |
| Current Stage | Problem Discovery |
| Implementation Track | To be determined |

---

*This repository documents the investigation, design, development, and evaluation of a solution to an operational coordination problem in freight logistics.*
