# Codex Setup Blueprint

Vendor-neutral, Git-safe YAML blueprints for describing an engineering workflow before asking Codex or another coding agent to design agents, skills, project guidance, and automation.

## Intended use

1. Fill the YAML files with real, non-secret information.
2. Keep unknown values as null, empty lists, or undecided; do not invent details.
3. Give the completed directory to an AI and ask it to inspect actual repositories before proposing changes.
4. Review the proposed agent roster, skills, and configuration before allowing writes.
5. Start manually; automate only workflows that have proved stable.

## Safety

- Never put API keys, passwords, tokens, certificates, or production data in these files.
- False is intentionally the safe default for deployment, migrations, destructive actions, and secret changes.
- A completed blueprint is planning context, not authority to bypass approvals or modify production.

## Files

- 00-metadata.yaml: ownership, audience, and blueprint metadata.
- 01-goal-scope.yaml: the initial setup goal, scope, and completion criteria.
- 02-environment.yaml: OS, WSL, editor, Codex client, and runtime facts.
- 03-projects.yaml: projects, stacks, repositories, and product constraints.
- 04-engineering-preferences.yaml: conventions and validation expectations.
- 05-devops-infrastructure.yaml: optional cloud, IaC, CI/CD, and operations context.
- 06-ai-systems.yaml: optional AI, agent, RAG, evaluation, and observability context.
- 07-agent-roster.yaml: candidate roles, ownership, and write boundaries.
- 08-model-routing.yaml: available models and task-routing preferences.
- 09-skills.yaml: installed skills, desired skills, and installation policy.
- 10-governance-and-permissions.yaml: approvals, Git, paths, and unattended-work boundaries.
- 11-failure-and-checkpoints.yaml: stop gates, blockers, checkpoints, and recovery.
- 12-deliverables-and-priorities.yaml: required outputs and priority order.

## Generality

The core files work for software development, platform engineering, and DevOps. Files 05 and 06 are optional extensions, so this blueprint does not assume AWS, a language, a framework, a package manager, or a specific Codex model.

