# MVP Plan v2
tags: #mvp #plan #roadmap

Version: 2
Date: 2026-04-14
Status: active
Supersedes: [[mvp_plan_v1]]

## Vision
Build a narrow, execution-ready TON stablecoin payment MVP that removes workflow friction, reuses existing wallet infrastructure, and can be shipped by one developer in 2-4 weeks.

## Core functionality (strict MVP scope)
- [[Payment Intent]]
- [[Wallet Handoff]]
- [[Transaction Status Tracking]]
- [[Activity Log]]

## Tech stack
Primary option:
- Telegram Mini App or simple web app
- existing TON wallet integration
- minimal Node.js backend only if required
- file-based storage or SQLite

Recommendation:
- choose the surface with the lowest wallet-friction after WhitePaper extraction

## Architecture
Working architecture is defined by [[mvp/Архитектура MVP]].
Long-term system ideas stay in [[reference/hubs/Future Architecture]] and must not expand MVP scope.

## Development phases
- [[mvp/phases/Этап 1 Прототип]]
- [[mvp/phases/Этап 2 MVP]]
- [[mvp/phases/Этап 3 Тестирование]]

## Risks
- [[mvp/Риски MVP]]
- unclear ICP
- unclear launch scenario
- missing extraction from source PDFs

## Next actions
- [[Следующие шаги]]
- parse source documents into notes
- define first payment scenario
- define ICP
- choose delivery surface

## Version delta
Changes from v1:
- converted plan into vault graph hubs
- separated source/reference materials from core graph
- established central nodes for roadmap, architecture, risks, stack, and phases
