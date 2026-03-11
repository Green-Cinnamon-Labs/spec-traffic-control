# Traffic Adaptive Control — Vision

## Problem

Urban traffic control can be viewed as a sequential decision problem. At each moment, the system observes signals from the environment (vehicle queues, flows, sensor readings) and must choose an action (e.g., switching or holding a traffic light phase). The consequence of this action only becomes visible in the future, when the traffic state evolves.

The key difficulty is that decisions cannot depend only on the current observation. Traffic has inertia: queues accumulate, flows propagate through the network, and past actions influence the present. Therefore any decision mechanism must incorporate **context**, meaning information produced in previous steps of the system.

---

## Classical Control

In classical control, the system continuously measures some variables of the environment (the feedback signal) and uses them to compute the next control action. The controller is defined by an equation where the current action depends on previously observed values or accumulated signals.

In other words, the control decision is computed through a **recursive process**: information from the previous step is reintroduced into the present computation. The system therefore carries forward a representation of the past through feedback.

---

## Neural Network with Attention

A neural network controller can be trained to map sensor observations to control actions. Instead of explicitly designing equations, the system learns a function that associates patterns of observations with appropriate actions.

To incorporate context, the network receives a sequence of observations (or previously computed representations) and processes them together. Mechanisms such as attention allow the model to weigh which elements of the past sequence are most relevant for producing the next decision.

---

## Why They Are Essentially the Same

Both approaches rely on the same fundamental structure: **the present decision depends on information produced in the past**. The system must carry forward some form of historical information and reintroduce it into the current computation.

This means both systems implement a recursive computation of the form: the output at time *t* depends on the current observation and something computed previously.

---

## What Is Different

The difference lies in how the decision function is obtained. In classical control, the functional form of the controller is designed explicitly based on assumptions about the system's dynamics.

In neural approaches, the decision function is not specified analytically. Instead, the network learns it from data, discovering patterns that relate observed situations to actions without requiring an explicit mathematical model of the traffic dynamics.
