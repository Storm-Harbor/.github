# Technical-demand delivery and traceability

GitHub is authoritative for identity, native parent/sub-issue hierarchy, status, assignees, PR links and closure. Storm Harbor uses its own organization **Project #1**, not another product's project board.

Major outcomes use a Journey umbrella and coherent Epics, with one executable delivery issue per owning repository. Create umbrellas before new `JOURNEY-<issue>-<slug>.md` / `EPIC-<issue>-<slug>.md` records. Records preserve scope, actors, contracts, security/data boundaries, dependencies and acceptance evidence without copying live status. A strategic Planet is optional when several Journeys need enduring shared strategy. Apply this hierarchy to new runtime planning; the initial publication issues retain their identities and can be attached without duplication.

Every delivery has native Feature/Bug type, an assignee, applicable labels and populated Priority, Size, Estimate, Workspace, Product and Status. Estimates are focused senior engineering hours including analysis, implementation, required tests, documentation and PR preparation; exclude review/deployment waiting. Record an explicit estimate, not a conversion from Size. Pure umbrella estimates sum direct children; executable parents separate their own effort to prevent double-counting.

Accepted work starts Todo, becomes In Progress on its owning branch, and remains open while implementation, validation, manual merge, publication or required acceptance is pending. Use `<issue>-feat-<slug>` or `<issue>-fix-<slug>` and English Conventional Commits. Keep the same branch through intermediate repairs and preserve unrelated local changes.

Open a concrete English PR with the problem, resulting behavior, relevant architecture/security impact, exact validation and migration/deployment considerations. Include a verified closing reference to the owning issue, check its linked PR field and avoid duplicate PR project items.

The user reviews and merges manually. Never merge on the user's behalf. Independent preparation is allowed; actual producer-to-consumer dependencies require the producer's checks, user merge and publication first. At handoff give exact PR order and evidence. Verify merge, issue closure and project reconciliation before marking Done.

Maintain one current issue checkpoint with ISO 8601 timestamp/timezone, objective/scope, owning branch/revision, authorization decisions, validation/result links, concrete blockers and next bounded action. Never store secrets or raw private payloads. Completed Journey/Epic records receive a `DONE-` prefix and completion timestamp only after all descendants and acceptance gates are complete.
