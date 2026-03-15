# Agents for life.web.siglattice.com.git

Type: codesmith_service

## What this repo is
- Codesmith is a thin wrapper around the OpenAI Codex CLI.
- It is meant to be run *inside* git-backed substrate domains under /substrate.
- Each domain declares itself via '_domain.json' with fields 'domain' and 'type'.

## Substrate fundamentals
- Substrate root: /substrate (do not hard-code other mountpoints).
- Domains map dots to path segments: life.services.codesmith.git -> /substrate/life/services/codesmith/git.
- Librarian HTTP API: http://atlas.lan/substrate/librarian (source of truth for domains, stones, tomes).
- Use domains + Librarian instead of absolute filesystem paths for cross-domain work.

## Codesmith expectations
- _domain.json must exist and type must end with '_service' for Codesmith to run.
- Session history is logged to tome: life.services.codesmith.sessions.tome, keyed by payload.git_domain.
- Codesmith resumes Codex sessions using GUIDs returned by '/tome/latest'.

## How to introspect
- Inspect _domain.json for domain/type.
- Use Librarian for live info:
  - http://atlas.lan/substrate/librarian/domain/list
  - http://atlas.lan/substrate/librarian/tome/latest?domain=life.services.codesmith.sessions.tome&type=codesmith_session&per=payload.git_domain&depth=1
- Avoid shelling into other repos via absolute paths; prefer Librarian APIs.

## Repo-specific notes
- Keep Codesmith CLI minimal and transparent; avoid clever shell tricks.
- When extending behavior, align with substrate conventions and domain metadata.
- If unsure, ask clarifying questions before large changes.

<!-- Substrate: domain=life.web.siglattice.com.git type=codesmith_service -->
