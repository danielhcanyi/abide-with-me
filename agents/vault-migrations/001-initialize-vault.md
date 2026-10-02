# Migration 001: Initialize private vault layout

**From schema:** `0` or no state file
**To schema:** `1`
**Safety:** Additive; no existing user records are changed or removed.

## Operations

1. Create the schema-1 private directories: `decisions/`, `observations/`,
   `reflections/`, `resources/`, `.agents/agent_journal/`, `.agents/user_model/`, and
   `.agents/migrations/`.
2. Create `<data_root>/.agents/vault-state.yaml` with:

   ```yaml
   schema_version: 1
   code_revision: <full-current-git-commit-hash>
   updated_at: <ISO-8601-timestamp>
   ```

3. Create `<data_root>/.agents/migration-log.md` if it does not exist.
4. Append an entry to the migration log recording migration `001`, the schema transition,
   timestamp, and code revision.

Do not overwrite an existing state file or migration log. Preserve existing records and
unrecognized files.
