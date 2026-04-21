# Repository Strategy

## Current reality

The working Nominas code currently lives inside the broader `Playground` git repository, not in an isolated project repository.

That means the first safe step is not to push anything directly from the current folder.

## Correct strategy

Use a two-repository model:

- private source repository for the real implementation
- public showcase repository for portfolio review

## Why this is necessary

The current working tree includes or references:

- deployment-sensitive files
- local and production environment files
- real spreadsheet artifacts
- bootstrap/setup routes
- historical material not suitable for public review

## Order of operations

1. Keep the current implementation private.
2. Use this showcase repository as the public portfolio layer.
3. Later, if needed, extract a clean private Nominas repo from the working tree.
4. Share private access only on request.

## What “done” looks like

Nominas is considered portfolio-ready when:

- the public showcase exists
- the private implementation remains private
- the product, workflows, and architecture are understandable without exposing the full codebase
