# Requirements

## Overview

Build a full-stack application for a problem domain of your choice. Start by identifying the target users, the problem they need solved, and the product experience that addresses it. The result should be a coherent product rather than a collection of unrelated screens or a shallow CRUD demo.

The application is full-stack React + Django (Python) with MongoDB persistence. Every capability you ship must work end to end: a usable UI surface, a real frontend API call, a backend handler, business logic, and stored data where data is involved.

Choose five to ten substantial capabilities from the patterns below, or propose equivalent capabilities of the same weight. Fewer than five is under scope. More than ten usually spreads the work too thin.

## Product definition

- Choose a product name and define its purpose in the README.
- Identify the primary user types and the main workflow the product supports.
- Define a coherent domain model with realistic seeded data and meaningful relationships.
- Select five to ten capabilities that demonstrate product depth across the UI, API, business logic, and MongoDB.

## Suggested capability patterns

- **Identity and access.** Sign in users, provide appropriate roles or profiles, and protect product actions with ownership or authorization rules.
- **Core domain management.** Create, view, edit, archive, restore, or otherwise manage the central records in the chosen domain.
- **Workflow and state.** Move records through meaningful states, enforce valid transitions, and show the resulting history or status clearly.
- **Relationships and assignment.** Connect related records, assign work or ownership, and make those relationships visible and editable.
- **Search and organization.** Provide useful search, filtering, sorting, grouping, or saved views for realistic data volumes.
- **Collaboration and permissions.** Support sharing, review, approval, comments, or role-specific actions when they fit the product.
- **Dashboard and reporting.** Summarize stored data with useful counts, trends, comparisons, or drill-down views.
- **History and auditability.** Record important changes and provide a readable timeline, activity feed, or restoration path.
- **Import, export, or configuration.** Support a useful data exchange or product configuration workflow using local, deterministic behavior.

## Acceptance criteria

- **Core features.** Build five to ten capabilities appropriate to the chosen product, such as core record management, workflows, search and filtering, authentication, dashboards, reporting, or activity history.
- **End-to-end functionality.** All core user flows must work seamlessly from start to finish.
- **Human judgment.** AI can help write the code, but feature selection, architectural decisions, and production readiness must reflect clear human judgment.
- **UI/UX.** The interface must be modern, sleek, and polished.
- **Clean build.** The app must install, build, and start without errors from a clean checkout.
- **Dependencies.** The technology stack and dependency versions must be current and at least as recent as those used in the reference repository.
- **Project structure.** The repository must follow the reference application structure precisely.
