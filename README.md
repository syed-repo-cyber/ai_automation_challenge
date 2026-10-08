# Automated Student Attendance & Academic Risk Management

A web application project scaffold for an attendance-monitoring and student-support system, based on the accompanying product brief.

## Project status

**This repository is currently a starter scaffold, not a completed attendance-management application.** It contains the TanStack Start, React, and TypeScript foundation and shared UI components. Student records, data imports, attendance calculations, risk scoring, notifications, appointment booking, and recurring reports from the brief have not yet been implemented. No real student data is included.

This distinction matters: the brief describes the intended product and capabilities; it does not mean those capabilities are already present in this snapshot.

## Intended product workflow

The planned system brings the following stages together into a single intervention process:

1. Import attendance, marks, and teacher availability from CSV or Excel files.
2. Preview, map, and validate columns and flag incomplete or invalid records before confirming an import.
3. Calculate attendance percentages and configurable attendance risk using explainable, deterministic rules.
4. Estimate consecutive classes needed to recover and forecast the effects of attending or missing upcoming classes.
5. Identify low, declining, and improving academic results.
6. Prioritize cases and prepare personalized student messages and staff recommendations.
7. Support follow-up through staff interventions and an appointment-availability workflow.
8. Provide an overview of intervention progress and weekly reporting.
9. Demonstrate below-threshold phone-call escalation with a clearly labeled demo or mock workflow unless a real calling service is configured.

These are goals from the product brief, **not features currently delivered by this scaffold**. The brief recommends an 85% default attendance threshold and an adjustable setting; calculations should use the formula `(classes attended / classes held) × 100`, with recovery determined by the minimum whole number of consecutively attended classes needed to meet the configured threshold. No such calculation is implemented yet.

## Technology in this repository

- React 19 and TypeScript
- TanStack Start and TanStack Router
- Tailwind CSS 4
- Reusable Radix-based UI components
- Vitest and Testing Library
- Bun lockfile for dependency management

The product brief mentions Next.js and FastAPI as possible choices. They are **not** the stack used in this repository. No API server, database, authentication, email provider, telephony integration, or persistent student data storage is configured.

## Run locally

Install [Bun](https://bun.sh/), then run:

```bash
bun install
bun run dev
```

Vite prints the local development URL when it starts.

Run the existing tests with:

```bash
bun run test
```

Create a production build with:

```bash
bun run build
```

## Repository layout

```text
src/
  components/ui/   Shared interface primitives
  hooks/           Shared React hooks
  lib/             Shared utilities and error reporting
  routes/          TanStack Start file-based routes
  test/            Test setup and routing tests
  router.tsx       Router and query-client setup
  server.ts        Server entry point
  start.ts         TanStack Start configuration
  styles.css       Tailwind imports and design tokens
public/            Public static assets
```

## Privacy and integrations

Do not upload real student information to an unconfigured demo. Before using real educational records, implement and review appropriate access controls, data-retention rules, institutional approvals, and applicable student-privacy requirements. Email, phone calls, and calendar synchronization are not enabled by this scaffold.