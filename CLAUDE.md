# Advent Calendar — project rules for Claude

## What this is
A free, open-source community advent calendar. Each user gets one calendar per year from a pool,
never the same one two years in a row. Day N unlocks on December N. Anyone can propose a calendar;
accepted ones join the pool. Launch: December 1, 2027.

This is also my learning project: I'm moving from Flutter/Angular into TypeScript backend work.
Treat every session as teaching, not just delivery.

## Stack
- Backend: NestJS (TypeScript), PostgreSQL, ORM decided in milestone 1 (record it below)
- Frontend: Angular
- Later: Redis (milestone 6), pgvector (milestone 5), Docker + GitHub Actions (milestone 4)
- Not in scope before launch: Python, microservices, message queues, agent frameworks

## How to work with me
- I own: database schema, business rules (assignment, unlocking, moderation), and their tests.
  For these, ask me how I'd do it first, then review my attempt. Leave TODO(human) markers.
- You may write: config, boilerplate, Docker/CI files, repetitive UI.
- Use plan mode for anything touching more than one file. Wait for my approval.
- Explain backend concepts through Angular/Dart equivalents, then say where the analogy breaks.
- Point out over-engineering. Simple and correct beats clever.
- Don't add dependencies without telling me why and what the alternative is.

## Non-negotiable product rules
- Calendar content lives only in the database. Never commit real calendar content or seed data
  with real entries to this public repo.
- The API never returns a locked day. Unlock checks happen on the server.
- One assignment per (user, year), enforced by a database constraint, not only app code.

## Conventions
- Integration tests run against a real Postgres (Docker), not mocks, for anything touching the DB.
- Conventional commits (feat:, fix:, refactor:, test:, chore:).
- Progress and decisions are tracked in PROGRESS.md. Read it at the start of every session.

## Decisions log
(Short entries: date — decision — why. /wrap adds to this via PROGRESS.md.)
