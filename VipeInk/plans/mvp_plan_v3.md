# MVP Plan v3
tags: #mvp #plan #roadmap

Version: 3
Date: 2026-04-14
Status: active
Supersedes: [[mvp_plan_v2]]

## Vision
Build a pilot-ready, bank-facing invisible settlement middleware product on TON for Tier-2/3 EEA banks, proving that cross-border settlement can be faster, more traceable, and easier to integrate without forcing banks to replace their existing client-facing systems.

## Core functionality (strict MVP scope)
- [[Bank Middleware MVP]]
- [[Settlement Request API]]
- [[Pilot Bank Integration]]
- [[Audit Trail Console]]
- [[Compliance Visibility Layer]]

## Tech stack
Recommended current direction:
- API-first backend
- lightweight demo console / dashboard
- simulated or pilot bank integration
- minimal storage for transaction records and audit trail
- TON-connected settlement representation only where needed for demo/proof

## Architecture
Working architecture is defined by [[Архитектура MVP]].
Long-term system ideas stay in [[Future Architecture]].

## Development phases
- [[Этап 1 Прототип]]: one settlement scenario, one corridor, one request-to-status flow
- [[Этап 2 MVP]]: pilot-ready API surface and audit visibility
- [[Этап 3 Тестирование]]: bank-facing validation through conversations, demos, and PoC preparation

## Risks
- product drift toward consumer crypto app
- ICP mismatch
- overbuilding chain infrastructure before pilot validation
- unclear compliance story in MVP narrative
- long bank sales cycle

## Next actions
- extract bank pipeline and licensing milestones into graph notes
- define first pilot settlement scenario
- define bank demo flow end to end
- define what is mocked vs real in MVP
- align roadmap with one-developer 2-4 week constraint

## Version delta
Changes from v2:
- corrected product direction after reading WhitePaper and BusinessPlan
- shifted MVP from consumer payment workflow to bank-facing invisible middleware
- introduced bank ICP, pilot integration, audit console, and compliance visibility as primary nodes
