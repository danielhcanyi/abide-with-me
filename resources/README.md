# Resources

This repository directory documents the resource layout. In a configured hybrid workspace,
write live resources to `<data_root>/resources/`, not here. Resources are shared or large
supporting material referenced by decision, observation, and reflection records. Examples
include meeting notes, research summaries, exports, source documents, and long-form
working notes.

Use clear, stable filenames and link a resource from a record with a relative Markdown
link, for example:

```md
[Meeting notes](../resources/2026-10-02-team-meeting.md)
```

Keep each journal record concise by recording its conclusion and the resource link rather
than copying a large source into several files. Do not store credentials, secrets, or
material the user would not want exposed to the local AI/chat environment.
