# Workflow Migration Kit

Use this directory when an AI engineering workflow already exists in another
tool or in an older Codex setup.

Migration means preserving useful outcomes while adapting implementation to the
target tool. It is not blind file copying.

## Process

1. Run EXPORT_FROM_SOURCE_PROMPT.md in the source environment when that tool can
   inspect its own configuration.
2. Review and sanitize the export. Never include credentials, authentication
   state, private production data, or customer information.
3. Fill source-tool-inventory.yaml for anything the source tool could not export.
4. Run IMPORT_AND_MAP_PROMPT.md in the target environment.
5. Review migration-decisions.yaml and approve the mapping.
6. Continue with the normal design, apply, and validation prompts.

## Common concept mapping

Typical mappings may include:

- global rules to global guidance;
- repository rules to project guidance;
- reusable commands and prompts to skills;
- specialized roles to custom agents;
- MCP/connectors/plugins to supported integrations;
- lifecycle scripts to hooks;
- recurring stable workflows to automation;
- model preferences to verified target-client routing;
- useful memory to explicit operator or project context.

Some concepts have no portable equivalent. Authentication, cloud-only state,
proprietary memory, unsupported hooks, and tool-specific UI behavior usually
require manual setup, redesign, or omission.
