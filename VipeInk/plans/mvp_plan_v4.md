# MVP Plan v4
tags: #mvp #plan #roadmap

Version: 4
Date: 2026-04-14
Status: active
Supersedes: [[mvp_plan_v3]]

## Vision
Build the fastest realistic wedge for Vipeink by framing it as a TON settlement / L2 abstraction layer that can later support bank middleware, while staying cheap, demoable, and grant-friendly.

## Core functionality (strict MVP scope)
- [[mvp/features/Settlement Request API]]
- lightweight sequencing / state transition abstraction
- transaction and settlement state tracking
- audit/proof-style record layer
- demo console
- optional vertical demo: bank middleware flow

## Product framing
Primary framing:
- TON settlement / L2 abstraction MVP

Secondary framing:
- bank-facing invisible middleware

Optional showcase framing:
- Telegram / TON app layer demo

## Tech stack
- API-first backend
- lightweight state store
- simple web console
- TON integration only where it strengthens the demo
- no production-grade rollup infra in MVP

## Architecture
Build the shell of an L2-style settlement system, not the full chain stack:
- request intake
- sequencing abstraction
- state machine
- audit/proof record
- operator/admin console

## Development phases
### Phase 1
- one settlement scenario
- one vertical narrative
- end-to-end console demo

### Phase 2
- second narrative on top of same core
- improved audit / record visibility
- clearer technical packaging for grants and pitch

### Phase 3
- grant applications / contest submissions / outreach package
- pilot conversations using working demo

## Risks
- trying to build real rollup too early
- overfitting to bank-only narrative
- overfitting to consumer-only narrative
- weak differentiation if demo is too shallow

## Next actions
1. define exact L2 abstraction MVP components
2. define what counts as the smallest convincing demo
3. create grant/contest opportunity notes
4. map one build path for 2 weeks and one for 4 weeks
5. clean remaining graph around new framing

## Version delta
Changes from v3:
- widened strategy beyond bank-only MVP
- reframed optimal wedge as TON settlement / L2 abstraction
- aligned roadmap with grants, contests, and faster entry paths
