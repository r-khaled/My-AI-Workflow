# Prompt 3 — Apply the Approved Design

Run only after explicit design approval.

---

Implement only the approved AI engineering workflow design.

Blueprint directory:

<PATH_TO_CODEX_SETUP>

Approved design:

<PATH_OR_REFERENCE_TO_APPROVED_DESIGN>

Explicitly approved changes:

<LIST_OR_REFERENCE>

Requirements:

1. Re-inspect every target before editing and follow applicable guidance.
2. Preserve unrelated changes and dirty worktrees.
3. Back up existing global configuration before changing it.
4. Use minimal, focused, reversible edits.
5. Create only approved agents, skills, guidance, config, hooks, MCP entries,
   documentation, and automation.
6. Do not hardcode an unavailable model.
7. Keep agent duties narrow and non-overlapping.
8. Keep planning and review read-only unless the approved design says otherwise.
9. Keep one production-code writer per checkout.
10. Reuse suitable installed skills; do not copy third-party skill content into
    agent instructions.
11. Do not modify auth files, secrets, shell profiles, production, IAM, DNS,
    databases, or billing.
12. Do not deploy, apply infrastructure, migrate data, push Git changes, or run
    destructive commands.
13. Validate each phase and record a checkpoint before continuing.
14. Stop at mandatory gates or unsafe divergence from the approved design.

For each generated component, document its scenario, location, ownership,
permissions, invocation, validation, and removal procedure.

Report files and backups, commands and results, validation evidence, agent
settings, skill triggers, deviations, blockers, risks, and the next validation
prompt. Do not claim completion without evidence.
