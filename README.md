# Latent Memory — Specification

This repository defines the research direction, mathematical premises,
and experimental strategy of the Latent Memory project.

It serves as the authoritative source of research assumptions,
design decisions, and project evolution.

---

## Objective

Build a long-term memory object for LLMs that persists state across sequences
without reinjecting all prior tokens — investigating latent and compressed memory
representations grounded in mathematics.

---

## Research Interest

**TOPIC 2 — LLM Context & Memory**

**Primary:** context compression methods for LLMs, latent/persistent memory across long sequences, memory-augmented transformers, efficient token representation.

**Secondary:** efficient attention mechanisms (linear, sparse, sliding-window), KV cache compression, in-context learning mechanics, long-context architecture design.

---

## Core Research Question

Can long-term memory be maintained in a compact latent object such that,
given a new token sequence, the model does not need to reprocess all prior tokens
to recover relevant context?

---

## Related Repositories

- [`lab-latent-memory`](https://github.com/Green-Cinnamon-Labs/lab-latent-memory/tree/main)
  Experimental lab for latent memory implementations and probes.
  Active workspace for testing memory compression approaches in practice.
