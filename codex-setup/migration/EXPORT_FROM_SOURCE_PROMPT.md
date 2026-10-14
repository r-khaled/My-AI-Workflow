# Export Prompt for the Source Tool

Run this in the source tool only if it can inspect its actual configuration.
Otherwise, fill source-tool-inventory.yaml manually.

---

Create a sanitized export of my current AI engineering workflow.

Do not include secrets, credentials, tokens, private keys, customer data,
production data, account identifiers, authentication state, or session data.

Inspect only configuration and repositories I am authorized to access.

Inventory:

- global and project instructions;
- file or directory-specific rules;
- custom agents and their responsibilities;
- delegation and orchestration behavior;
- skills, commands, and reusable prompts;
- MCP servers, connectors, and plugins;
- hooks and lifecycle scripts;
- scheduled and recurring automation;
- model and reasoning preferences;
- permission and approval policies;
- persistent memory and project knowledge that are actually exportable;
- recurring workflows worth preserving;
- representative tasks and validation;
- current pain points and failed patterns;
- tool-specific capabilities with no obvious portable equivalent.

For each item include:

- a stable source asset ID;
- source location or configuration surface;
- purpose and observed behavior;
- scope;
- dependencies;
- permissions or sensitive boundaries;
- whether it appears active, stale, duplicated, or unknown;
- whether it should be considered for preservation, adaptation, merge, or removal;
- information that could not be inspected.

Return:

1. YAML matching migration/source-tool-inventory.yaml;
2. a concise Markdown summary;
3. a list of files that must be reviewed manually;
4. warnings about non-portable or sensitive behavior.

Do not modify the source setup.
