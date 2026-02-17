# Memory Pipeline

This repository implements a daily memory loop for stateful AI agents.

The goal is to convert activity into stable recall so the agent remains consistent across days.

The loop runs in four stages:

capture → organize → tag → journal


---

## Stage 1 — Capture

Input:
memory/YYYY-MM-DD.md  
or  
memory/pipeline/daily/YYYY-MM-DD/index.json

This contains raw daily activity.

Nothing here is optimized. It is only recorded.


---

## Stage 2 — Organize

Script:
daily-memory-processing

Input:
memory/pipeline/daily/YYYY-MM-DD/index.json

Output:
memory/organized/YYYY-MM-DD_organized.json

Behavior:
- Group entries by topic or project
- Extract key_points, decisions, unresolved
- Assign importance levels
- Track continuity with previous days
- Generate lessons learned

This converts activity into structured knowledge.


---

## Stage 3 — Tag Index

Script:
tag-index-generation

Input:
organized daily memory

Output:
memory/tags/

Behavior:
- Update global tag counts
- Track first and last occurrence
- Track distributions by type and importance
- Keep small sample references

This makes memory searchable.


---

## Stage 4 — Evening Journal

Script:
evening-journal

Input:
organized memory + daily activity

Output:
memory/journal/YYYY-MM-DD.md

Behavior:
- Narrative summary
- Pattern recognition
- Carry forward unresolved items
- Lessons learned

This reinforces identity continuity.


---

## Result

Instead of infinite logs:

logs → forgotten context

The agent maintains:

experience → structured knowledge → recall → continuity
