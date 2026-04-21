# Live Tour

## Goal

This document makes the public showcase easier to evaluate by mapping the live application routes to the product areas they represent.

Verified against the live deployment on `2026-04-21`.

## Selected live routes

| Area | Live route | Access | What it represents |
|------|------------|--------|--------------------|
| App entry | [nomina.atlantechmarine.com](https://nomina.atlantechmarine.com) | public | Login shell and SPA entry point |
| Kiosk punch | [nomina.atlantechmarine.com/reloj](https://nomina.atlantechmarine.com/reloj) | public field route | GPS-aware punch flow for field users |
| Dashboard | [nomina.atlantechmarine.com/dashboard](https://nomina.atlantechmarine.com/dashboard) | authenticated | KPI cards, alerts, active projects, trends, quick actions |
| Employees | [nomina.atlantechmarine.com/employees](https://nomina.atlantechmarine.com/employees) | `admin` | Employee management and detail flows |
| Projects | [nomina.atlantechmarine.com/projects](https://nomina.atlantechmarine.com/projects) | `admin` | Project records, assignments, contractor linkage |
| Weekly timesheets | [nomina.atlantechmarine.com/timesheets](https://nomina.atlantechmarine.com/timesheets) | `admin`, `supervisor` | Weekly salary report, crew grouping, draft/approve flow |
| Time punches | [nomina.atlantechmarine.com/time-punches](https://nomina.atlantechmarine.com/time-punches) | `admin`, `supervisor` | Punch review and operational control |
| Payroll | [nomina.atlantechmarine.com/payroll](https://nomina.atlantechmarine.com/payroll) | `admin` | Payroll overview, generation, detail review |
| Financial control | [nomina.atlantechmarine.com/financials](https://nomina.atlantechmarine.com/financials) | `admin` | Requested vs paid tracking, adjustments, remaining balance |
| Reports hub | [nomina.atlantechmarine.com/reports](https://nomina.atlantechmarine.com/reports) | authenticated | Entry point into the report suite |
| Settings | [nomina.atlantechmarine.com/settings](https://nomina.atlantechmarine.com/settings) | `admin` | Controlled configuration areas |
| User manual | [nomina.atlantechmarine.com/manual](https://nomina.atlantechmarine.com/manual) | authenticated | Embedded operational guidance |

## Report inventory

The report layer is not a placeholder. The implemented report suite includes:

- [Project summary](https://nomina.atlantechmarine.com/reports/project-summary)
- [Project worker detail](https://nomina.atlantechmarine.com/reports/project-worker)
- [Contractor summary](https://nomina.atlantechmarine.com/reports/contractor-summary)
- [Worker report](https://nomina.atlantechmarine.com/reports/worker)
- [Payroll register](https://nomina.atlantechmarine.com/reports/register)
- [Paycheck print](https://nomina.atlantechmarine.com/reports/paychecks)

Most report routes are role-protected, but they are part of the live routed application structure.

## What this proves

This project should be evaluated as:

- a working internal product
- a route-complete SPA with multiple operational areas
- a workflow-heavy system, not a static admin panel
- a full-stack implementation that connects UI, API, payroll logic, reporting, and financial control

## Reading path

1. Open the live app entry point.
2. Review the route table above.
3. Read [README](../README.md).
4. Continue with [Architecture](./architecture.md), [Workflows](./workflows.md), and [Feature Map](./feature-map.md).
