# Service 7000 Steering Board

Single-file HTML dashboard (`index.html`), also published as a Claude artifact.
Artifact URL: https://claude.ai/artifact/9PzB5mNy5GWe3QM2poprD9 (also in `artifact.md`).

## Workflow
- For every change: edit `index.html`, then publish it to the artifact URL above (same URL, never a new artifact). Skip the publish only if the user says local only.
- Publishing is refused until the live version has been viewed. If refused, read the live version (Artifact action `read`), merge any live-only changes into `index.html`, then publish again.
- If the same content is refused as "identical", copy the saved live file to the scratchpad, apply the edits to the copy, and publish the copy.
- Keep the page wrapper at the top and bottom of `index.html` (`<!doctype html><html><head>...` and the final `</body></html>`); the platform added it.
- The `comments` capability is declared on the artifact; keep it when republishing.

## Where the content lives (inside `<script>` in `index.html`)
- `ITEMS`, `LANES`, `ST`: board items per portal and stage (Planned, In Progress, Staging, Live, On hold)
- `HEALTH`, `SIMPLE`, `MAINT`: portal health cards and the simple detail pages (SAM, Tenant, AI)
- `PROJ`: full project pages (Customer Portal, S7000 Akademie)
- `HOME`: overview "Decisions needed" and "Top risks and blockers"
- `Q4`, `COLLAB`: Q4 plan and the "Working together" / "Collaboration with AI" pages

## Conventions
- Plain, short wording. Write "SELISE X Service 7000" for the collaboration.
- When a status changes, update every place it appears (board stage, health card, detail page, overview decisions and risks, Q4 plan).
- The login is demo only (`demo@service7000.com` / `steering2026`), not real security.
