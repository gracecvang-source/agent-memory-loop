# Agent Memory Loop

This provides structure first and reference scripts second.

A daily memory pipeline that keeps long-running AI agents consistent across days.

Most agents drift over time because chat logs accumulate but understanding does not.

This project converts activity into structured recall:

capture → organize → tag → journal

This repository currently provides the structure and schemas first; reference scripts are being cleaned and added incrementally.

Result:
Instead of the agent forgetting context after a few sessions,
it maintains continuity through a lightweight daily loop.


---

## What This Fixes

Common problem:

day 1 → agent feels coherent  
day 5 → behavior shifts  
day 10 → personality collapses or resets

Cause:
Logs are not memory.

This pipeline turns logs into knowledge.


---

## What Happens Each Day

1. Capture  
   Raw activity is recorded.

2. Organize  
   Important information is extracted and categorized.

3. Tag  
   Topics become searchable across time.

4. Journal  
   A narrative summary reinforces continuity.


---

## Installation (conceptual)

1) Copy the repository into your agent project
2) Configure paths
3) Add scheduled runs (cron or scheduler)
4) Begin writing daily notes or feeding activity

The agent will begin building stable recall automatically.

---

## Quick Start (minimal)

The system is intentionally usable manually before automation.You do NOT need full automation to use this.

Day 1:

1. Create a file:
   memory/2026-01-01.md

2. Write a short summary of activity:
   - what happened
   - decisions made
   - unresolved items

3. Create:
   memory/pipeline/daily/2026-01-01/index.json

   Example:

   {
     "date": "2026-01-01",
     "summary": "Initial test day",
     "activities": [],
     "observations": ["testing memory loop"],
     "tags": ["setup"]
   }

4. Run the organize and journal scripts (manual or future automation)

You now have structured recall.

Repeat daily.
---

## Documentation

See `/docs`:

PIPELINE.md – how the loop works  
SCHEMAS.md – file formats


---

## Design Goals

- Human readable first
- Automation optional
- Model-agnostic
- Works with manual or automated capture


---

## Status

Early release while being cleaned for public use.
Structure is stable; scripts will evolve.
