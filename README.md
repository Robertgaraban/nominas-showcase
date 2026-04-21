# Nominas Public Showcase

Nominas is a bilingual payroll, weekly timesheet, and labor cost control web application built for US staffing and field-operations workflows.

Live deployment: [nomina.atlantechmarine.com](https://nomina.atlantechmarine.com)

## At a glance

- Status: `live in production`
- Product type: `internal payroll + labor operations system`
- Audience: `admin`, `supervisor`, `viewer`
- Stack: `React 18`, `Vite`, `TailwindCSS`, `PHP REST API`, `MySQL`, `JWT`
- Access model: `public showcase + private source review on request`

## Selected live entry points

- App entry / login shell: [nomina.atlantechmarine.com](https://nomina.atlantechmarine.com)
- Mobile kiosk punch: [nomina.atlantechmarine.com/reloj](https://nomina.atlantechmarine.com/reloj)
- Dashboard: [nomina.atlantechmarine.com/dashboard](https://nomina.atlantechmarine.com/dashboard) `auth required`
- Weekly timesheets: [nomina.atlantechmarine.com/timesheets](https://nomina.atlantechmarine.com/timesheets) `auth required`
- Payroll: [nomina.atlantechmarine.com/payroll](https://nomina.atlantechmarine.com/payroll) `auth required`
- Financial control: [nomina.atlantechmarine.com/financials](https://nomina.atlantechmarine.com/financials) `auth required`
- Reports hub: [nomina.atlantechmarine.com/reports](https://nomina.atlantechmarine.com/reports) `auth required`
- User manual: [nomina.atlantechmarine.com/manual](https://nomina.atlantechmarine.com/manual) `auth required`

The application is a SPA, so these routes resolve through the same frontend shell and then enforce access by role.

## What I built

Nominas is not a mock dashboard. It is an internal operations system built around real weekly payroll and labor-control workflows.

The implemented product scope includes:

- employee management
- project and contractor management
- weekly timesheet capture
- kiosk/mobile punch entry
- payroll generation
- payroll detail review
- project financial control
- reporting and exports
- role-based access control
- in-app manual and settings

## System tour

### 1. Login + dashboard

The authenticated shell opens on a dashboard built for operations, not vanity metrics.

It includes:

- KPI cards for labor, requested, paid, and remaining amounts
- quick actions into the main workflows
- active-project visibility
- multi-week trend charts for labor, requested, and paid amounts
- alerting around pending financial-control state

### 2. Weekly salary report

The timesheet module is based on the real Excel-driven weekly salary report process.

Key implemented behaviors include:

- project selector + week selector
- crew-group sections
- Mon-Sun hour capture per worker
- fixed weekly salary and hourly-rate support
- copy previous week
- save draft
- approve week
- markup-aware totals

### 3. Mobile kiosk punch

Nominas also includes a field-oriented punch flow instead of relying only on desktop data entry.

The kiosk route supports:

- mobile entry through `/reloj` and related aliases
- phone-based employee lookup
- 4-digit PIN confirmation
- GPS acquisition
- nearest-project detection
- geofenced punch in / punch out behavior

### 4. Payroll and period review

The payroll area is not just a single export button.

It includes:

- payroll overview
- payroll generation
- payroll detail review
- downstream register and paycheck reporting

### 5. Financial control

This is one of the strongest parts of the product because it connects labor capture to project money tracking.

The module supports:

- labor subtotal
- admin fee
- manual adjustments
- requested amount
- paid amount
- remaining balance
- weekly status progression from `draft` to `paid`

### 6. Reports hub

The reporting layer includes dedicated report flows for:

- project summary
- project worker detail
- contractor summary
- worker report
- payroll register
- paycheck print

## Live tour and route evidence

For a route-by-route overview of the implemented product, see [Live Tour](./docs/live-tour.md).

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

## Main modules

The private implementation currently includes dedicated modules for:

- `Dashboard`
- `Employees`
- `Projects`
- `Weekly Timesheets`
- `Kiosk Punch / Time Punches`
- `Payroll`
- `Financial Control`
- `Reports Hub`
- `Settings`
- `User Manual`

This is based on the actual routed application structure in the working product, not on a conceptual roadmap.

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
- GPS-aware kiosk punch flow
- contractor/division grouping
- multiple exportable reports
- admin / supervisor / viewer roles
- bilingual internal workflow support

## Route and module evidence

The implemented application shell currently exposes route groups for:

- `/dashboard`
- `/employees`
- `/projects`
- `/timesheets`
- `/time-punches`
- `/payroll`
- `/financials`
- `/reports`
- `/settings`
- `/manual`
- kiosk punch aliases such as `/reloj`, `/fichar`, and `/kiosk/punch`

These routes are backed by concrete frontend modules in the private implementation.

## Selected workflow areas

- weekly salary capture
- payroll calculation
- financial control and requested vs paid tracking
- dashboard visibility for operations
- reporting and exports

## Workflow evidence

The product is documented around real workflow areas, not generic admin abstractions:

- weekly salary report workflow
- financial control workflow
- live route and module tour
- deployment and bootstrap workflow
- API route surface
- database structure
- UI shell and layout system

See:

- [Live Tour](./docs/live-tour.md)
- [Architecture](./docs/architecture.md)
- [Workflow Map](./docs/workflows.md)
- [Feature Map](./docs/feature-map.md)
- [Documentation Map](./docs/documentation-map.md)

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
2. Open the live routes listed above and see the system entry points.
3. Review the route-by-route summary in [docs/live-tour.md](./docs/live-tour.md).
4. Review the architecture snapshot in [docs/architecture.md](./docs/architecture.md).
5. Review the workflow framing in [docs/workflows.md](./docs/workflows.md).
6. Review the module and feature summary in [docs/feature-map.md](./docs/feature-map.md).
7. Treat this repository as a portfolio layer, not as the full production codebase.

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
- See [docs/public-scope.md](./docs/public-scope.md), [docs/repo-strategy.md](./docs/repo-strategy.md), [docs/closeout.md](./docs/closeout.md), and [NOTICE.md](./NOTICE.md).
