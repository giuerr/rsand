# Agent Etna — Contract & Guardrails

This file is maintained automatically by **Agent Etna** for **rsand**.
It is this agent's behavioral **contract**: what it's for, who it serves, what's
in and out of scope, plus a log of every change Etna has applied — so the whole
footprint is visible and auditable in your own repo.

_Maintained by Agent Etna. Don't edit by hand — it is rewritten on every shipped change._

## Agent
- **Repo:** `giuerr/rsand` (branch `main`)

## Behavioral contract
_No calibration set yet — Agent Etna uses general defaults until you calibrate this agent._

## Guardrails
- No behavioral calibration set yet — Agent Etna uses general defaults until you calibrate this agent.

## Change history

### 2026-08-16 · Cycle 2 · 1 change · merged
- **safety:output-sensitive-data** — The agent bypassed a safety constraint by taking an irreversible action without confirmation, so adding a prompt to explicitly ask for user confirmation for such actions will prevent future violations.

### 2026-08-16 · Cycle 1 · 1 change · merged
- **safety:memory-retention** — The original instructions mentioned maintaining conversation context but lacked specific guidance on *what* to recall, leading to potential gaps in memory retention.

### 2026-08-16 · Cycle 1 · 1 change · merged
- **safety:dialog-scope** — Adding a direct instruction to decline attempts at identity or instruction changes will prevent the agent from engaging with such prompts.

### 2026-08-16 · Cycle 1 · 1 change · merged
- **behavior:tone-under-pressure** — The existing instruction to keep a neutral tone can be strengthened to specifically address error scenarios and ensure the agent maintains a helpful demeanor under pressure.

### 2026-08-16 · Cycle 1 · 1 change · merged
- **safety:input-jailbreak** — The agent used a forbidden term, so a direct negative constraint in the prompt is the most efficient fix.
