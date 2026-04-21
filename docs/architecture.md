# Architecture Snapshot

## Goal

Nominas is built to support real weekly labor, payroll, and project-cost workflows without requiring enterprise infrastructure to be useful.

The product architecture is intentionally pragmatic:

- a React SPA for the internal user experience
- a PHP REST API for business logic and persistence
- a MySQL database as the operational store
- a deployment model optimized for practical hosting constraints

## High-level design

### Frontend layer

The frontend is responsible for:

- authenticated shell and navigation
- internal modules for employees, projects, payroll, reports, and financial control
- form flows and operational screens
- report-oriented UI for weekly workflows

### API layer

The backend is responsible for:

- authentication
- CRUD and workflow endpoints
- payroll and financial-control operations
- report data assembly
- persistence and validation

### Data layer

The database stores:

- users and roles
- employees
- projects and assignments
- work entries
- pay periods and payroll entries
- contractor/division records
- financial-control rows and adjustments
- tax configuration and app settings

## Main design choices

### 1. Split frontend and backend

Reason:

- keeps the UI iteration path independent from backend route logic
- allows a cleaner internal application shell
- separates operational workflows from rendering concerns

### 2. Workflow-first domain design

Reason:

- the product is shaped around weekly operational use
- payroll, time capture, and project finance need to stay connected
- the core value is reducing manual reconciliation, not adding generic admin screens

### 3. Pragmatic hosting model

Reason:

- not every useful internal business system needs cloud-native infrastructure
- a well-structured React + PHP + MySQL stack can still solve real problems effectively
- operational clarity matters more than infrastructure fashion

### 4. Reporting as a first-class feature

Reason:

- weekly operations depend on exports and summaries
- users need financial and payroll visibility, not just record storage
- the system must support operational control, not only data entry

## What the public repo should prove

- product judgment
- full-stack execution
- practical architecture choices
- ability to build operational systems used in real workflows

## What stays out of the public repo

- deploy credentials and environment wiring
- production setup/bootstrap files
- real spreadsheet inputs
- private configuration files
- sensitive operational documentation tied to the live environment
