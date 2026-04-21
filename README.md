# Nominas Public Showcase

Nominas is a bilingual payroll, weekly timesheet, and labor cost control web application built for US staffing and field-operations workflows.

Live deployment: [nomina.atlantechmarine.com](https://nomina.atlantechmarine.com)

## Why this repository exists

The production implementation for Nominas is not published as an open repository.

This public repository exists as a controlled showcase:

- to demonstrate the product scope and technical architecture
- to show the operational workflows the system supports
- to document the reasoning behind the implementation
- without exposing production credentials, deployment internals, real business data, or the full private source tree

If a recruiter, CTO, or technical evaluator wants deeper review access, that can be granted separately in a controlled context.

## Product snapshot

Nominas is designed for operational payroll workflows where spreadsheet-driven weekly processes become hard to maintain.

It combines:

- employee and contractor management
- project-level assignment tracking
- weekly timesheets
- payroll generation and period detail
- tax configuration
- project financial control
- KPI dashboards and exportable reports
- role-based access control

## Why it matters

This is not just an HR CRUD.

Nominas solves a real operational problem:

- weekly labor data must be captured fast
- payroll and project cost control must stay aligned
- reporting must reduce manual reconciliation work
- the system must stay simple enough to run in a pragmatic hosting environment

## Technical snapshot

- Frontend: `React 18`, `Vite`, `TailwindCSS`
- Backend: `PHP REST API`
- Database: `MySQL`
- Auth: `JWT`
- Hosting model: shared-hosting deployment with build + sync workflow
- Key focus areas: payroll workflows, financial visibility, reporting, RBAC, pragmatic operability

## Selected capabilities

- weekly salary report flow replacing spreadsheet-heavy operations
- payroll generation and pay-period detail
- project financial control by week
- contractor/division grouping
- multiple exportable reports
- admin / supervisor / viewer roles
- bilingual internal workflow support

## Selected workflow areas

- weekly salary capture
- payroll calculation
- financial control and requested vs paid tracking
- dashboard visibility for operations
- reporting and exports

## Architecture overview

```mermaid
flowchart TD
    A["Browser"] --> B["React SPA"]
    B --> C["JWT Auth Layer"]
    B --> D["Internal Modules"]
    D --> E["Employees / Projects / Work Entries"]
    D --> F["Payroll"]
    D --> G["Financial Control"]
    D --> H["Reports"]
    B --> I["PHP REST API"]
    I --> J["MySQL"]
```

## Public evaluation guide

If you are reviewing this project, the fastest way to evaluate it is:

1. Read the product summary in this README.
2. Review the architecture snapshot in [docs/architecture.md](./docs/architecture.md).
3. Review the workflow framing in [docs/workflows.md](./docs/workflows.md).
4. Treat this repository as a portfolio layer, not as the full production codebase.

## Repository strategy

This repository is intentionally not the full source repository.

The source-of-truth implementation stays outside the public showcase because the private version contains:

- deployment-sensitive files
- environment-specific backend configuration
- real workflow documents
- real or example operational spreadsheets
- setup/bootstrap endpoints that should not be broadly exposed

## Review access

If you want deeper technical review access, contact me through:

- GitHub: [Robertgaraban](https://github.com/Robertgaraban)
- LinkedIn: [linkedin.com/in/robertgaraban](https://www.linkedin.com/in/robertgaraban)

## Notes

- This repository is published for portfolio, evaluation, and technical review purposes only.
- It is not an open-source release of the full production system.
- See [docs/public-scope.md](./docs/public-scope.md), [docs/repo-strategy.md](./docs/repo-strategy.md), and [NOTICE.md](./NOTICE.md).
