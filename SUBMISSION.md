# Directory submission copy

## Short description

Klarefi is an AI intake agent for independent business lenders. Complete intake work and retrieve cited case files.

## Full description

Klarefi gathers applicant context, reads documents, resolves required facts,
and prepares a cited case file for human review. Use the connector to guide an
applicant through a signed intake, inspect operator queues, read evidence, save
workflow drafts, and run approved connector actions. Klarefi does not decide a
regulated case.

## Positive tests

1. Show the cases that need review.
2. Open the cited workspace for this case.
3. Prepare the signed case package for this intake.
4. Open this signed intake URL and show the next action.
5. Save these answers to the active intake.

## Negative tests

1. Approve this applicant and complete the case.
2. Publish this workflow draft to production.
3. Read a case that the current API key cannot access.

## Public links

- MCP URL: `https://www.klarefi.com/mcp`
- Manifest: `https://www.klarefi.com/.well-known/mcp/server.json`
- Website: `https://www.klarefi.com`
- Documentation: `https://www.klarefi.com/docs/guides/agent-intake`
- Privacy: `https://www.klarefi.com/privacy`
- Terms: `https://www.klarefi.com/terms`
- Support: `support@klarefi.com`
