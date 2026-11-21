# Start here: Forever rotation work

Open the `Rota` folder in VS Code. Keep your existing `forever/` folder and symlink.
Saving an editable rotation there may update the live profile through that link.

## Read the local references

1. `AGENTS.md` defines the workflow for gameplay research and offline engine checks.
2. `reference/INDEX.md` maps topics to the actual local documentation and data.
3. Consult published Forever guides for the class, role and content being reviewed.
4. `reference/READINESS-AUDIT.md` records what was checked in the uploaded repo.

All base documentation exports and all shared YAML files are present. Some
relevant statements conflict or have unverified Forever applicability. Their
presence is not certification of the installed runtime. Do not download unrelated
data or guess an answer simply to complete an audit.

## Editor setup

Use the existing Codex and Simia rotation extensions. Remote data fetching is
disabled in this workspace's settings. The supplied Simia VSIX was inspected as
source, not run here; it can reuse its old remote cache when fetching is disabled.
Run **Rotation YAML: Clear Remote Cache**, reload the window, and use
**Rotation YAML: Show Status** to check local Forever spell data was loaded.
**Rotation YAML: Reload Spells** is also available. These commands are defined
in the supplied VSIX 1.5.1; its status is not an engine or binding test.

## The working loop

Use the prompt in `reference/OFFLINE-VALIDATION-PROMPT.md` with the requested
canonical file. Codex must audit local evidence first, ask all material questions
together and stop before an affected edit if evidence is missing or conflicting.
When the evidence is sufficient, make a small change and test that behaviour in game.

The existing checker is optional and requires the dependency in `requirements.txt`.
When that environment is available, an explicit-file check is:

```powershell
py tools/check.py forever/priest-levelling-dungeon-heal.yaml
```

A static pass does not establish expression semantics, actual bindings or
gameplay success. Simia Forever has no user rank choice; use the rank Simia
selects rather than adding rank-selection/downranking controls. No new validation framework or separate agent-role
workflow is required.

## Reference collection

Collection or refresh of technical data is a separate task. Do not run `tools/refresh_sources.py` as part of
an offline audit. The small upstream question set is in
`reference/simia/OPEN-QUESTIONS.md`. DLLs and credentials are not required.
