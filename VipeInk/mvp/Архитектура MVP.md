# Архитектура MVP
tags: #mvp #architecture

Связано:
- [[MVP]]
- [[mvp/Техстек MVP]]
- [[mvp/Ключевые функции]]
- [[mvp/Риски MVP]]
- [[reference/hubs/Референсы]]
- [[mvp/features/Bank Middleware MVP]]
- [[mvp/features/Invisible Middleware]]

## MVP-архитектура
- Bank-facing API layer
- Settlement Request API
- orchestration/service layer
- transaction state machine
- audit trail console
- compliance visibility layer
- mock or pilot bank integration

## Границы
Это не [[reference/hubs/Future Architecture]].

## Зависит от
- [[mvp/Целевая аудитория]]
- [[mvp/Ключевые функции]]
- [[mvp/Ценность продукта]]

## Не входит
- production ZK-rollup with full decentralization
- proof marketplace
- ATM flows
- full reserve auditor network
- full multicurrency infrastructure
- consumer wallet product