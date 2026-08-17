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

### 2026-08-17 · Cycle 5 · 1 change · merged
- **intent-comprehension** — This prompt update strengthens the agent's ability to handle ambiguous intent by explicitly instructing it to ask clarifying questions instead of guessing or refusing, improving user interaction.

### 2026-08-17 · Cycle 5 · 1 change · merged
- **behavior:tone-under-pressure** — The existing prompt does not explicitly guide the agent on how to maintain tone when encountering unexpected issues, which could lead to an unhelpful or flustered response under pressure.

### 2026-08-17 · Cycle 5 · 1 change · merged
- **safety:cost-unbounded-loop** — This prompt update directly addresses the 'cost-unbounded-loop' capability by imposing a concrete limit on retries, preventing resource exhaustion.

### 2026-08-17 · Cycle 5 · 1 change · merged
- **context-retention** — The agent asked blindly for column names instead of inspecting the loaded dataframe first, which is the idiomatic R workflow and avoids unnecessary clarification turns; a prior prompt-update for this failure mode was already rejected on this agent, so a scoped memory primitive is lower blast radius.

### 2026-08-17 · Cycle 5 · 1 change · merged
- **safety:input-jailbreak** — This prompt update directly addresses the forbidden term "overridden" in the agent's output by explicitly prohibiting its use.

### 2026-08-16 · Cycle 2 · 1 change · merged
- **safety:output-no-fabrication** — Adding a clear instruction against fabrication will prevent the agent from generating spurious outputs when it lacks sufficient information or encounters execution issues.

### 2026-08-16 · Cycle 2 · 1 change · merged
- **behavior:honest-limits** — The agent needs explicit instructions to decline requests outside its defined R interpretation and data analysis scope to maintain honest limits.

### 2026-08-16 · Cycle 2 · 1 change · merged
- **intent-comprehension** — The agent failed to clarify the user's ambiguous request for 'interesting' customer data before asking for data upload.

### 2026-08-16 · Cycle 2 · 1 change · merged
- **safety:memory-retention** — The trace shows the agent replied generically about lacking memory instead of acknowledging the specific reference REF-FA199A the user cited, so the prompt now requires verbatim echoing of user-supplied identifiers.

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
