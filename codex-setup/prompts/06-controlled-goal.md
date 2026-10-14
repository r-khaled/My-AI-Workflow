# Prompt 6 — Controlled Goal

Use only after the manual workflow has passed validation and the objective is
bounded, reversible, and safe without live supervision.

---

Execute this approved goal using the installed workflow:

<GOAL>

Allowed repositories and paths:

<EXACT_PATHS>

Approved milestones:

<ORDERED_MILESTONES_WITH_DEFINITION_OF_DONE>

Constraints:

- Follow the blueprint, approved design, and repository guidance.
- Respect configured concurrency and keep one production-code writer per checkout.
- Reuse the same implementer thread for bounded repair rounds.
- Validate and checkpoint after every milestone.
- Preserve existing user changes and do not push Git changes.
- Do not deploy, apply infrastructure, migrate data, access production, change
  IAM/DNS/auth/secrets/billing, or perform destructive actions.
- Do not install tools, dependencies, agents, or skills unless explicitly approved.
- Near time or usage limits, stop optional work, validate completed work, save a
  checkpoint, and prepare a resume summary.
- At a mandatory gate, record the blocker and continue only independent safe work.

Report milestones, changed files, commands and results, checks, repair rounds,
decisions, blockers, risks, the next safe action, and a copy-paste resume prompt.
