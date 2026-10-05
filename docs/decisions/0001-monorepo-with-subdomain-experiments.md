# 0001: Monorepo with one folder per subdomain

- **Date:** 2026-10-05
- **Status:** accepted

## Context

This repo has to hold a personal site (thoughts, photos, videos, portfolio) and an open-ended number of experiments, each on its own subdomain, such as `26daysoftype.domain.com`.

## Decision

- Use a single repo with `apps/` (permanent sites), `experiments/` (one folder per subdomain), `packages/` (shared code), and `content/` (writing and media).
- Each experiment's folder name is its subdomain, and each one deploys independently.
- Content stays separate from presentation code.

## Consequences

- An experiment can use any stack and be deleted without side effects.
- The design language lives in `packages/tokens`, so it stays consistent across subdomains.
- Every new experiment needs its own deploy project and DNS record. That one-time setup is worth the isolation.
