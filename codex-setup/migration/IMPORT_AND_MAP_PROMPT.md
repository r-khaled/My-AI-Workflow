# Import and Mapping Prompt

Run this in the target environment after sanitizing the source inventory.

---

Map an existing AI engineering workflow into the target Codex environment.

Inputs:

- completed codex-setup blueprint;
- migration/source-tool-inventory.yaml;
- source export summary;
- allowed target repositories and configuration paths.

Rules:

- Do not copy files or implement changes in this stage.
- Verify target-client capabilities and available models instead of assuming
  source concepts have direct equivalents.
- Treat every source asset as evidence, not as a requirement to reproduce it.
- Never migrate credentials, authentication state, private memory, customer
  data, production data, or secret values.
- Prefer the smallest appropriate target surface.
- Preserve outcomes and useful behavior, not source-tool syntax.
- Identify conflicts with current target configuration and user changes.

For every source asset, recommend one decision:

- preserve with minimal adaptation;
- adapt to a different target surface;
- replace with an existing target capability;
- merge with another asset;
- drop because it is stale, unsafe, duplicated, or unnecessary;
- defer because information or capability is missing.

Map candidates across:

- one-off prompts;
- global guidance;
- project guidance;
- custom agents;
- skills;
- configuration;
- MCP or connectors;
- hooks;
- automation;
- explicit operator or project documentation.

Produce a proposed migration-decisions.yaml containing rationale, target surface,
dependencies, manual steps, security changes, and validation scenarios.

Also produce:

1. a portability report;
2. unsupported capabilities;
3. permission and behavior differences;
4. an ordered migration plan;
5. rollback and cleanup steps;
6. questions that require human decisions.

Stop after the mapping proposal. Do not implement until the decisions are
reviewed and explicitly approved.
