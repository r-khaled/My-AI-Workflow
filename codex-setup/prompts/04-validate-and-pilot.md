# Prompt 4 — Validate and Pilot

Validate the installed workflow without production access or high-impact actions.

Blueprint directory:

<PATH_TO_CODEX_SETUP>

Installed design or implementation report:

<PATH_OR_REFERENCE>

1. Static validation
   - parse generated formats;
   - run official diagnostics available in the client;
   - confirm agent and skill discovery;
   - confirm referenced paths;
   - identify unsupported or ignored settings;
   - confirm no secret or auth file changed.

2. Policy validation
   - verify writer ownership, read-only roles, concurrency, repair limits, and
     production/migration/IAM/DNS/secret/cost/destructive stop gates;
   - verify unattended runs cannot silently broaden permissions.

3. Behavioral validation
   - choose one low-risk representative scenario from file 14;
   - run a bounded dry run or local pilot;
   - verify role and skill selection, handoffs, required checks, and reporting.

4. Quality and usage review
   - record latency, failures, repeated context, and unnecessary delegation;
   - identify overlap, excessive effort, false triggers, and missing guidance.

Do not deploy, migrate data, access production, push Git, or expand permissions.

Produce pass/fail evidence and recommend keep, tune, disable, merge, or defer
for each generated component.
