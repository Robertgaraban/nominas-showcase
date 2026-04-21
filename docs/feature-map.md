# Feature Map

## Goal

This document makes the public showcase more concrete by listing the actual product areas implemented in Nominas.

## Core product areas

### 1. Dashboard

Purpose:

- surface KPIs
- show operational summaries
- provide quick visibility into payroll and financial-control state

### 2. Employees

Purpose:

- create and manage employee records
- review employee detail
- support assignment and payroll-related workflows downstream

### 3. Projects

Purpose:

- manage projects
- connect projects to contractors/divisions
- support worker assignment and financial visibility

### 4. Weekly Timesheets

Purpose:

- replace spreadsheet-heavy weekly salary reporting
- capture work by employee, project, and week
- support approval flow and downstream payroll operations

### 5. Kiosk Punch / Time Punches

Purpose:

- support simplified operational punch workflows
- allow field-oriented time capture entry paths

### 6. Payroll

Purpose:

- generate payroll
- review payroll detail
- connect work capture to pay-period outputs

### 7. Financial Control

Purpose:

- track labor subtotal
- track admin fee
- register manual adjustments
- track requested, paid, and remaining balances

### 8. Reports

Purpose:

- provide operational exports and summary views
- reduce repeated manual reconciliation work

Known report areas include:

- project summary
- project worker report
- contractor summary
- worker report
- payroll register
- paycheck print

Representative routed paths:

- `/reports`
- `/reports/project-summary`
- `/reports/project-worker`
- `/reports/contractor-summary`
- `/reports/worker`
- `/reports/register`
- `/reports/paychecks`

### 9. Settings

Purpose:

- support controlled configuration areas for the application

### 10. User Manual

Purpose:

- keep operational guidance close to the product
- reduce onboarding friction for real users

## Access model

The working product uses role-based access control with role distinctions such as:

- `admin`
- `supervisor`
- `viewer`

Representative route access:

- `admin`: employees, projects, payroll, financials, settings
- `admin` + `supervisor`: timesheets, time punches, some reports
- authenticated users: reports hub, manual, dashboard

## Portfolio interpretation

Nominas should be evaluated as:

- a workflow-heavy internal business system
- a full-stack product
- an operations tool designed around weekly use, not only static CRUD
