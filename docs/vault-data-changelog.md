# Private Vault Data Changelog

This changelog describes **structure changes** to the user's private vault. It is
versioned with the agent system so a running session can identify and apply the required
migrations. It never contains user data.

The active schema is declared in `.agents/vault-schema.yaml`. Migration instructions are
stored in `.agents/vault-migrations/`. A private vault records its applied schema and the
exact agent commit in `<data_root>/.agents/vault-state.yaml`, then records each migration
in `<data_root>/.agents/migration-log.md`.

## Schema 1

### Added

- Canonical private-vault directories: `decisions/`, `observations/`, `reflections/`, and
  `resources/`.
- Durable agent-context directories: `.agents/agent_journal/`,
  `.agents/user_model/`, and `.agents/migrations/`.
- Private vault state with the schema version and running agent commit hash.
- A private migration log.

### Migration

Apply `.agents/vault-migrations/001-initialize-vault.md`. The migration is additive and
does not modify or remove existing journal records.
