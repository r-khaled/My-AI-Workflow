# Prompt Sequence

Use these prompts in order and replace placeholder paths before sending them.

1. 01-discover-and-audit.md validates context and finds blocking gaps without changing the setup.
2. 02-design-workflow.md turns approved context into a minimal system design without installing it.
3. 03-apply-approved-design.md creates only explicitly approved components.
4. 04-validate-and-pilot.md checks syntax, discovery, boundaries, and behavior.
5. 05-operate-and-improve.md uses real outcomes to tune or remove components.
6. 06-controlled-goal.md runs a bounded goal only after the manual workflow is reliable.

Do not combine discovery and unattended implementation for a new setup. The
approval between design and application prevents incorrect assumptions from
becoming durable global configuration.

Completed YAML values are user context and constraints. Comments and README text
explain the templates; they do not override system, developer, organizational,
sandbox, or runtime permission policies.
