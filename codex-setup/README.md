# Codex Setup Blueprint

Build a safe, personalized AI engineering system for the way you work across
all your projects—not a one-off agent for a single repository.

This toolkit gathers structured context about you, your projects, engineering
standards, infrastructure, recurring work, existing AI setup, permissions, and
operational constraints. Codex can then use that evidence to propose and build
the smallest useful combination of:

- global and project guidance;
- custom agents and subagent orchestration;
- reusable skills;
- model and reasoning routing;
- project configuration and permission profiles;
- hooks, MCP integrations, and automations when justified;
- documentation, checkpoints, validation, and recovery workflows.

The result should be a maintainable system that can grow with your work. It
should not create every possible agent or skill, duplicate tools you already
have, or automate workflows that have not been proven manually.

## Who this is for

This blueprint supports three starting points:

1. **Greenfield onboarding** — you are building an agent workflow for the first
   time and need a safe, structured starting point.
2. **Workflow audit** — you already use coding agents, but your rules, prompts,
   agents, skills, and permissions are fragmented or inconsistent.
3. **Migration accelerator** — you are moving useful behavior from another AI
   coding tool into Codex, while adapting concepts that are not directly
   portable.

It is useful for software engineers, DevOps and platform engineers, technical
founders, AI engineers, and small teams managing multiple projects or stacks.

## What this toolkit is—and is not

This toolkit is:

- a structured discovery and design process;
- a portable description of your working context and constraints;
- a set of staged prompts with human approval gates;
- a basis for generating and validating a personalized Codex setup;
- a way to audit and improve that setup over time.

This toolkit is not:

- a source of truth for secrets or credentials;
- permission to deploy, migrate data, access production, or change IAM/DNS;
- a blind converter that copies configuration from another tool;
- a guarantee that every requested model or feature exists in your client;
- a replacement for inspecting the real repositories and installed tools.

## The core idea

The YAML files answer structured questions. `CONTEXT.md` captures the human
story that does not fit cleanly into fields. Real repositories provide the
evidence. The prompts turn all three into a controlled workflow:

```text
Fill templates and context
          ↓
Validate and inspect real evidence
          ↓
Gap analysis and critical questions
          ↓
Workflow architecture and proposed roster
          ↓
Human approval
          ↓
Generate agents, skills, config, and documentation
          ↓
Validate syntax and run bounded pilot tasks
          ↓
Use manually, measure, and improve
          ↓
Add controlled goals and automation only when stable
```

## Directory map

The core questionnaire is split into focused snapshots:

- `00-metadata.yaml` — ownership, audience, status, and intended clients.
- `01-goal-scope.yaml` — what the setup run may change and how completion is
  measured.
- `02-environment.yaml` — OS, WSL, editor, Codex clients, runtime, and tools.
- `03-projects.yaml` — every relevant project, its stack, lifecycle, and risks.
- `04-engineering-preferences.yaml` — engineering, quality, documentation, and
  Git conventions shared across projects.
- `05-devops-infrastructure.yaml` — optional cloud, IaC, CI/CD, operations,
  security, reliability, and cost context.
- `06-ai-systems.yaml` — optional AI applications, agent harnesses, RAG,
  evaluation, guardrails, and observability.
- `07-agent-roster.yaml` — candidate roles, ownership, write boundaries, and
  delegation rules. Candidate roles are suggestions, not requirements.
- `08-model-routing.yaml` — models actually available and the preferred balance
  between quality, latency, and usage.
- `09-skills.yaml` — existing skills, recurring workflows, and policy for
  creating or installing more.
- `10-governance-and-permissions.yaml` — allowed paths, Git behavior, approvals,
  and unattended-work boundaries.
- `11-failure-and-checkpoints.yaml` — stop gates, blockers, checkpoints, and
  resume behavior.
- `12-deliverables-and-priorities.yaml` — expected outputs and priority order.
- `13-operator-profile.yaml` — your experience, responsibilities, working
  style, learning goals, and preferred level of delegation.
- `14-work-scenarios.yaml` — representative real tasks from which useful agents
  and skills can be derived.
- `15-existing-ai-workflow.yaml` — current agents, rules, skills, MCP, hooks,
  automations, and pain points for audit or migration.
- `CONTEXT.md` — optional narrative context that should not be forced into YAML.

Supporting directories:

- `prompts/` — staged discovery, design, implementation, validation, and
  continuous-improvement prompts.
- `migration/` — sanitized source-tool inventory and migration mapping.
- `examples/` — non-secret examples showing the expected level of detail.

## How much context is enough?

Do not optimize for word count. Optimize for representative evidence.

A strong minimum context pack contains:

- completed core files `00` through `04`, plus `07`, `10`, `11`, and `12`;
- files `05` and `06` when infrastructure or AI systems are relevant;
- an operator profile;
- three to eight representative work scenarios;
- read access to at least one real repository for each major stack;
- an inventory of existing AI configuration when auditing or migrating;
- one example of an output you consider good and one recurring failure or pain
  point, when available.

For a single developer, `CONTEXT.md` is usually useful when the structured
files cannot explain the reasoning behind preferences. It does not need to be
an autobiography. A concise description of responsibilities, current projects,
strengths, weak areas, and desired delegation is enough.

## How to fill the YAML files

- Use real facts where you know them.
- Use `null` for an unknown scalar value.
- Use `[]` for an empty or not-yet-known list.
- Use `undecided` when the decision is intentionally open.
- Add one project or scenario item per real case; duplicate the provided item
  template as needed.
- Distinguish current facts from future preferences.
- Do not claim tools, models, permissions, or commands that have not been
  verified.
- Keep production account identifiers, customer data, and private internal
  URLs out of a public repository.
- Never put secrets, access keys, passwords, session data, private keys, or
  authentication files here.

Comments explain expected meaning and format. They are guidance for the person
filling the file; they do not grant runtime permission to the AI.

### Public templates and private completed profiles

The templates in this directory are designed to remain public. A completed
profile may reveal private paths, project names, architecture, operational
constraints, or personal work habits even when it contains no secret value.

For a public repository, put the completed copy under `codex-setup/local/` or
use filenames ending in `.private.yaml`. These paths are ignored by Git. Point
the staged prompts at that private directory. Commit only deliberately
sanitized examples.

For a private repository, you may fill the tracked templates directly after
reviewing the repository's access controls and secret-scanning policy.

## Minimum viable completion

You do not need to complete every optional field before starting discovery.
The first prompt is designed to find gaps and inspect facts that are available
locally.

Before discovery, complete at least:

- the objective and allowed paths in `01-goal-scope.yaml`;
- the primary client and repository roots in `02-environment.yaml`;
- one real project in `03-projects.yaml`;
- your required checks in `04-engineering-preferences.yaml`;
- concurrency and writer boundaries in `07-agent-roster.yaml`;
- permissions in `10-governance-and-permissions.yaml`;
- stop gates and checkpoint locations in `11-failure-and-checkpoints.yaml`;
- required outputs in `12-deliverables-and-priorities.yaml`;
- at least three entries in `14-work-scenarios.yaml`.

Unknown technical facts that can be inspected should remain unknown rather than
being guessed.

## Recommended workflow

### Stage 1 — Fill and sanitize

Complete the relevant YAML files and `CONTEXT.md`. Review the directory for
secrets before committing it. If migrating, complete the source-tool inventory
or use the sanitized export prompt under `migration/`.

### Stage 2 — Discover and audit

Run [01-discover-and-audit.md](./prompts/01-discover-and-audit.md). Codex reads
the context, validates it, inspects allowed repositories and existing setup,
and returns missing questions and a current-state report. It must not modify
configuration in this stage.

### Stage 3 — Design the workflow

Answer the blocking questions, update the blueprint, then run
[02-design-workflow.md](./prompts/02-design-workflow.md). Codex proposes the
minimum useful agents, skills, guidance, configuration, and orchestration flow.
Review this design before any write.

### Stage 4 — Apply the approved design

Run [03-apply-approved-design.md](./prompts/03-apply-approved-design.md) only
after the design is explicitly approved. Codex creates bounded, reversible
changes and writes checkpoints after each phase.

### Stage 5 — Validate and pilot

Run [04-validate-and-pilot.md](./prompts/04-validate-and-pilot.md). Validate file
formats, diagnostics, discovery, role boundaries, and a small representative
task. A syntax-valid agent is not automatically an effective agent.

### Stage 6 — Operate and improve

Run [05-operate-and-improve.md](./prompts/05-operate-and-improve.md) after real
usage. Keep, tune, merge, or remove agents and skills based on evidence. Move a
workflow into Goals or scheduled automation only after it is predictable when
run manually.

## Expected outputs

The approved implementation may produce some—not necessarily all—of the
following:

- concise global and project `AGENTS.md` guidance;
- global and project Codex configuration;
- focused custom agent files with explicit ownership and sandbox boundaries;
- reusable skills with clear triggers, inputs, outputs, and validation;
- project-specific documentation and command references;
- MCP or hook recommendations where they solve a demonstrated need;
- manual orchestration prompts and controlled autonomous workflows;
- model-routing recommendations based on models actually available;
- validation, risk, checkpoint, and unresolved-question reports.

The AI should justify every generated component. “It might be useful” is not a
sufficient reason to create another agent, skill, hook, or integration.

## Audit and migration

Migration is concept mapping, not file copying. Rules, custom commands, agents,
skills, MCP connections, hooks, permissions, model names, memory, and
automations differ between tools.

Use the files under `migration/` to:

1. export a sanitized inventory from the source tool;
2. classify each item as preserve, adapt, replace, merge, or drop;
3. map it to the smallest appropriate Codex surface;
4. identify unsupported or non-portable behavior;
5. validate the migrated behavior with representative scenarios.

Credentials, authentication sessions, cloud-only state, and private memory
must not be copied into this repository.

## Safety defaults

The templates intentionally default high-impact actions to `false`. A setup run
must stop before:

- production access or deployment;
- database or data migrations;
- IAM, DNS, account, billing, or secret changes;
- destructive commands or deletion;
- breaking public API or authentication changes;
- a new paid dependency or material cost;
- broad permission expansion;
- unresolved test failures after the configured repair limit.

For unattended work, approval requests may not be answerable. The workflow
must checkpoint completed work, record the blocker, and stop or continue only
with independent safe tasks.

## FAQ

### Will filling the files automatically create the perfect setup?

No. The files provide structured context. Codex must still inspect real
repositories, find contradictions and missing information, propose a design,
and receive approval before implementation.

### Should every candidate agent be enabled?

No. Start with the smallest roster that covers recurring scenarios. Too many
agents increase coordination cost, context, and usage.

### When should a workflow become a skill?

When it is repeated, has recognizable triggers, and benefits from stable steps,
references, scripts, or validation. General personality belongs in an agent;
durable project rules belong in project guidance.

### Can this be used with tools other than Codex?

Most context files are vendor-neutral. The prompts and generated output target
Codex concepts, but migration adapters or additional platform-specific folders
can map the same context to other tools.

### Can this be published publicly?

The templates can. A filled blueprint may expose private paths, project names,
architecture, or operational details. Sanitize it or keep the filled version
private.

## Official Codex references

- [AGENTS.md guidance](https://learn.chatgpt.com/docs/agent-configuration/agents-md)
- [Subagents and custom agents](https://learn.chatgpt.com/docs/agent-configuration/subagents)
- [Build skills](https://learn.chatgpt.com/docs/build-skills)
- [Configuration basics](https://learn.chatgpt.com/docs/config-file/config-basic)
- [Configuration reference](https://learn.chatgpt.com/docs/config-file/config-reference)
- [Scheduled tasks](https://learn.chatgpt.com/docs/automations)
