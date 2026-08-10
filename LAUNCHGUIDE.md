# Klarefi

## Tagline

Complete regulated intake work before human review.

## Description

Klarefi guides applicants, reads submitted documents, resolves workflow facts with cited evidence, and prepares case files for operators. It also lets approved clients create intake sessions, inspect the operator queue, save workflow drafts, and run controlled connector actions.

Klarefi completes the intake. It does not decide the case.

The hosted MCP server uses the stateless MCP `2026-07-28` protocol. Local clients can also run the same server through the `@klarefi/mcp` package.

## Setup Requirements

- `Authorization` (optional): Use `Bearer` followed by a Klarefi API key for customer and operator tools. Create a key in Klarefi Developer Settings.
- Signed intake URL (optional): Applicant tools accept the signed URL from an intake invitation. They do not need an API key.
- `KLAREFI_API_KEY` (optional, local package only): Klarefi API key for customer and operator tools.
- `KLAREFI_API_BASE_URL` (optional, local package only): A Klarefi deployment URL. The hosted server does not accept caller-selected API origins.

## Category

Business Tools

## Features

- Create hosted applicant intake sessions
- Open applicant intake from a signed URL
- Answer free-text and structured intake questions
- Upload requested applicant documents
- Save and submit applicant intakes
- Wait for the next intake action
- Retrieve cases and resolved facts
- Inspect cited case evidence and blockers
- Download a cited case package
- List the operator review queue
- Submit auditable review commands
- List Form, Fact, Verify workflows
- Validate and save workflow drafts
- Create, import, update, and delete verification connectors
- Render a read-only case review workspace in MCP Apps hosts

## Getting Started

- "Open this signed Klarefi intake URL and tell me what information is still required."
- "Show the operator queue and summarize why each case needs review."
- "Get the cited case package for this case. Do not make a decision."
- "Save this Form, Fact, Verify declaration as a workflow draft."
- Tool: `open_intake` — Open an applicant intake from a signed URL.
- Tool: `get_case_workspace` — Inspect facts, cited evidence, blockers, ownership, and timeline.
- Tool: `get_case_package` — Retrieve the cited case artifact and its read-only URL.
- Tool: `save_workflow_draft` — Validate and save a workflow draft without publishing it.

## Tags

regulated-intake, workflow, compliance, document-ingestion, fact-extraction, cited-evidence, human-review, applicant, operator, business-tools, mcp-apps, stateless-mcp

## Documentation URL

https://www.klarefi.com/docs/guides/agent-intake

## Health Check URL

https://www.klarefi.com/api/live
