# Prompt 2 — Design the Workflow

Run after discovery and resolution of blocking questions.

---

Design a personalized AI engineering workflow from the approved blueprint and
discovery report.

Blueprint directory:

<PATH_TO_CODEX_SETUP>

Approved discovery report:

<PATH_OR_REFERENCE_TO_DISCOVERY_REPORT>

Constraints:

- Do not modify or install anything in this stage.
- Use actual repositories, installed capabilities, available models, and runtime
  policies as evidence.
- Design for the complete workload across multiple projects.
- Prefer reusable global components plus project-specific guidance only where
  behavior truly differs.
- Do not create an agent, skill, MCP integration, hook, or automation without a
  demonstrated scenario and expected benefit.
- Keep one production-code writer per checkout.
- Planning, exploration, architecture, and review roles are read-only by default.
- Production, migrations, IAM, DNS, secrets, authentication boundaries,
  destructive actions, and material cost are human approval gates.

Produce:

1. Workflow architecture: primary-agent duties, delegation flow, manual and
   autonomous modes, writer ownership, repair limits, checkpoints, and resume.
2. Guidance placement: prompt, global guidance, project guidance, project docs,
   configuration, rules, hooks, and automation.
3. Agent roster: responsibility, justifying scenarios, handoff contract, write
   scope, sandbox, available model/effort, required skills, overlap analysis,
   and global versus project placement.
4. Skill set: triggers, inputs, outputs, intended agents, resources, validation,
   representative eval cases, and existing-skill reuse.
5. Configuration: global defaults, project overrides, profiles, permissions,
   concurrency, model fallback, secret handling, MCP, hooks, and automation.
6. Implementation plan: reversible phases, exact targets, backup, validation,
   pilot tasks, rollback, and deferred work.
7. Usage and risk report: model/agent usage, trade-offs, gates, unsupported
   capabilities, and assumptions still requiring approval.

Separate observed facts, approved decisions, and recommendations.

Stop after the design and exact file plan. Do not write setup files until I
explicitly approve the design or list approved changes.
