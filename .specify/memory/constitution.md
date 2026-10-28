<!--
Sync Impact Report
Version change: Unversioned scaffold -> 1.0.0
Defined principles:
- I. Secure by Default
- II. Scope and User Value
- III. Maintainable Simplicity
- IV. Verified Quality
- V. Clear, Accessible UX
Added sections: Project Constraints; Development Workflow and Quality Gates
Removed sections: None
Follow-up TODOs: None
-->
# RSS Feed Reader Constitution

## Core Principles

### I. Secure by Default
Treat URLs, feed metadata, and feed content as untrusted input. Validate inputs at system
boundaries, protect secrets from source control and logs, and use safe output encoding. Any
feature that fetches feeds MUST restrict requests to HTTP(S), prevent access to local or
private-network destinations (including after redirects), and enforce time and response-size
limits. Feed HTML MUST be sanitized before rendering. These controls prevent the reader from
becoming a path to server-side request forgery, secret exposure, or unsafe content execution.

### II. Scope and User Value
Every change MUST support a user need in the approved feature specification or be required for
security, reliability, accessibility, or maintainability. Keep delivery incremental and avoid
unrequested feed-reader features. Resolve conflicts between stakeholder notes through the
current approved specification and plan; do not treat older planning documents as authorization
to expand scope. This keeps the proof-of-concept focused while allowing deliberate evolution.

### III. Maintainable Simplicity
Prefer the simplest design that meets the approved requirements, with clear boundaries between
the ASP.NET Core API, Blazor UI, and persistence responsibilities. Reuse existing project
patterns and dependencies; add abstractions or packages only when they materially reduce
complexity or enable a required capability. Changes to the established .NET, ASP.NET Core,
Blazor, or SQLite technology choices MUST be justified in the plan before implementation.
Simple, consistent code reduces learning and maintenance costs.

### IV. Verified Quality
New behavior and bug fixes MUST have relevant automated tests. Changes to API behavior or
component interactions MUST include tests at the appropriate integration boundary. Before
completion, run the narrowest applicable tests and build or type-check, and report any
validation that could not be completed. Tests and explicit verification make regressions
visible and keep the application dependable.

### V. Clear, Accessible UX
User-facing flows MUST provide clear labels, understandable feedback for success and failure,
and keyboard-accessible controls. Keep presentation focused on the approved feature scope and
consistent with existing UI patterns. Verify affected flows at relevant viewport sizes when
layout changes. A simple, accessible interface supports the project's demonstration purpose
without requiring unnecessary polish.

## Project Constraints

The project is a locally run, single-user RSS/Atom reader developed to run on Windows, macOS,
and Linux. The established application stack is .NET, ASP.NET Core, Blazor, and SQLite. A
proposal to change these constraints MUST explain the user or engineering benefit and assess
migration impact in its plan. Specific feature scope and behavior are defined by the current
approved specifications, not by this summary.

## Development Workflow and Quality Gates

Feature work MUST proceed from an approved specification and plan to actionable tasks before
implementation. Plans MUST identify relevant security, compatibility, accessibility, and
testing implications. Reviews MUST check the change against this constitution, the approved
scope, and the affected tests. Do not mark work complete until applicable validation has passed
or its limitation and impact have been documented. At the end of each completed development
workflow, provide a suggested commit message summarizing the changes. Do not create a commit
unless the user explicitly requests one. This makes completion guidance consistent without
committing changes without authorization.

## Governance

This constitution governs project decisions and takes precedence over conflicting implementation
guidance. Amendments MUST be made in a reviewed change that states the rationale and updates
the version, amendment date, and sync impact report. Versioning follows semantic versioning:
MAJOR for incompatible principle or governance changes, MINOR for new principles or materially
expanded requirements, and PATCH for clarifications and non-semantic wording changes. Project
maintainers review compliance during specification, planning, and code review; deviations MUST
be justified in the relevant plan or review and must not weaken security safeguards.

**Version**: 1.0.0 | **Ratified**: 2026-10-28 | **Last Amended**: 2026-10-28
