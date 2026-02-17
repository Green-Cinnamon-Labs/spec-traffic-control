# Traffic Adaptive Control LAB — Specification

This repository defines the architectural, control-theoretic,  
and learning specifications of the Traffic Adaptive Control LAB project.

It serves as the authoritative source of control assumptions,  
learning strategy decisions, and system evolution.

---

## Objective

> Describe in one technical sentence the primary objective of the project.  
> Example: "Build a deterministic traffic intersection simulation  
> integrated with an online adaptive neural controller  
> capable of optimizing signal timing under dynamic demand."

---

## Core Principles

- Separation of simulation and learning layers.  
> Explain how the neural network must never be coupled to the physical simulation engine.

- Deterministic experiment reproducibility.  
> Define what determinism means in this context (fixed seed? fixed time-step?).

- Explicit state formalization.  
> Make clear that the state used by the network must be formally defined.

- Explicit action-space constraints.  
> Define that traffic signal control must respect physical and temporal invariants.

- Trajectory-level performance evaluation.  
> Clarify that efficiency is measured over trajectories, not isolated time instants.

---

## Related Repositories

- [`fork-trafficSimulator`](https://github.com/Green-Cinnamon-Labs/fork-trafficSimulator)  
  Base traffic simulation engine (Python implementation).  
  > Describe the current maturity level of the simulator and its limitations.

- [`lab-traffic-adaptive-network`](https://github.com/Green-Cinnamon-Labs/lab-traffic-adaptive-network)  
  Neural network learning module.  
  > Define whether this will be pure online learning, reinforcement learning, or a hybrid approach.

- [`traffic-control-bridge`]  
  Interface layer between simulation state and controller policy.  
  > Explain that this module defines state, action, and reward.

---

## Control Problem Definition

> Formally define:  
> - What is the state s?  
> - What is the action a?  
> - What is the cost function J?  
> - What is the decision horizon (discrete? continuous?)?

---

## Learning Strategy

> Specify:  
> - Type of learning (supervised, reinforcement, online incremental).  
> - Update frequency.  
> - Whether a replay buffer is used.  
> - Whether explicit exploration is used.  
> - Convergence or stability criteria.

---

## Simulation Interface

> Document:  
> - How the state is extracted.  
> - How the action is applied.  
> - Temporal constraints (e.g., decision every N seconds).  
> - Determinism guarantees.

---

## Modernization Plan (Simulator Core)

> List the structural changes required in fork-trafficSimulator:  
> - Separation of rendering and dynamics.  
> - Explicit time-step control.  
> - External control hook.  
> - Deterministic logging.  
> - Structured metrics.