# Decision Records

This repository directory documents the decision-record layout. In a configured hybrid
workspace, write live decision records to `<data_root>/decisions/`, not here. Use
`agents/templates/decision.md` as the starting structure and a unique filename such as
`2026-10-02-consider-new-role.md`.

At session start, scan headings or metadata for `Review dates` and `Status` so reviews
can be surfaced without reconstructing the user's history from chat. Keep personal
details proportionate; do not store secrets, credentials, or information the user would
not want exposed.
