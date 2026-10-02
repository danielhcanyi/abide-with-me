# Migration 002: Unhide the agent metadata directory

**From schema:** `1`
**To schema:** `2`
**Safety:** Lossless directory rename. Journal records are not transformed.

## Operations

1. Inspect `<data_root>/.agents/` and `<data_root>/agents/`.
2. If `<data_root>/.agents/` exists and `<data_root>/agents/` does not, rename
   `.agents/` to `agents/`. Preserve every file and subdirectory, including the vault
   state, migration log, coaching journal, and user model.
3. If `<data_root>/agents/` already exists and `.agents/` does not, verify that it
   contains the schema-1 state and required metadata, then retain it as already migrated.
4. If both directories exist, stop without changing either. Explain the collision and ask
   the user to choose how to reconcile the two directories.
5. Verify that `<data_root>/agents/vault-state.yaml` and
   `<data_root>/agents/migration-log.md` are readable, then record the schema-2 result in
   the migration log.

This migration is a same-filesystem rename only. Do not copy, merge, overwrite, or delete
files. If the rename fails, leave the source directory untouched and stop.
