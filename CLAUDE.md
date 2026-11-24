# Shared Editing Rules for ChatGPT and Claude

This repository is the shared source of truth for the science-class website.

## Canonical source
- Default branch: `main`
- Eclipse simulation: `earth-science/eclipse.html`
- Always fetch the latest version from `main` before editing.
- Do not restore or overwrite files using older local downloads, chat attachments, or stale copies.

## Collaboration workflow
1. Read this file and inspect the current GitHub version of the target file.
2. Make the requested change against the latest version from `main`.
3. Preserve unrelated content, interactions, responsive behavior, and existing styling.
4. Before committing, check the changed section and verify that the HTML/CSS/JS remains structurally valid.
5. Commit the complete updated file to `main` (or use a clearly named branch and PR if a review is needed).
6. After the commit, report the commit SHA and the exact file path.
7. If another editor has updated the file since it was fetched, fetch the newest version and reconcile changes. Never force-push or replace newer work with an older snapshot.

## Handoff between assistants
ChatGPT and Claude do not message each other directly. They coordinate through this repository:
- The latest committed file on `main` is the shared baseline.
- Before making changes, each assistant must fetch the latest version.
- After making changes, each assistant must commit to GitHub and state what changed.
- The next assistant must pull/fetch that commit before continuing.

## Eclipse page requirements currently established
- Tab order begins with `개기식과 부분식`.
- The event tab label is `언제 일어날까?`.
- In the event comparison, solar-eclipse information is on the left and lunar-eclipse information is on the right on wide screens.
- Keep the solar and lunar event lists vertically organized within their respective columns.
- Do not display literal escaped newline text such as `\\n`.
- Preserve responsive stacking on narrow screens.
