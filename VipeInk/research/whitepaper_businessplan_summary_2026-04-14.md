# WhitePaper + BusinessPlan Summary 2026-04-14
tags: #research #source #strategy

Связано:
- [[MVP]]
- [[reference/hubs/Source Documents]]
- [[mvp/Ценность продукта]]
- [[mvp/Целевая аудитория]]
- [[mvp/План разработки MVP]]

## Что это за проект на самом деле
Vipeink по текущим source documents это не consumer wallet и не generic TON payment app.

Это regulated payment middleware на TON для межбанковских и cross-border B2B расчетов, ориентированное прежде всего на Tier-2/3 банки в EEA.

Ключевой тезис:
- invisible middleware для банка
- банк сохраняет свой UI, клиента и лицензионный контур
- Vipeink работает как settlement rail под капотом

## Проблема из документов
Основные боли:
- SWIFT settlement 1-4 дня
- дорогой correspondent banking
- дублирование KYC/AML на каждом звене
- Tier-2/3 банки платят disproportionately high costs и хуже конкурируют

## Обещание продукта
- settlement около 5.2 секунд
- API-first интеграция для банков
- ZK-backed compliance / auditability
- bridge между blockchain settlement и существующими банковскими процессами

## Целевая аудитория по документам
Primary ICP:
- Tier-2/3 банки в EEA
- особенно банки с cross-border SME / trade-finance / treasury pain

Не primary ICP:
- retail users
- обычные криптопользователи
- broad consumer payments

## Настоящая продуктовая форма
На уровне продукта Vipeink должен выглядеть как:
- invisible middleware
- bank API integration layer
- settlement orchestration layer
- audit/compliance-capable transaction rail

А не как:
- новый конечный wallet
- пользовательский superapp
- общий DeFi frontend

## Что из long-term architecture реально важно
Документы описывают большую future-state system:
- ZK-Rollup
- SWIFT bridge
- compliance layer
- oracle/liquidity layer
- ATM / fiat / reserve systems
- proof marketplace

Но для MVP не нужно всё это строить целиком.

## Что должно стать реальным MVP после чтения документов
Правильный MVP должен проверять не consumer UX, а bank adoption thesis:

### MVP hypothesis
Банк или банкоподобный pilot partner готов тестировать invisible settlement middleware, если:
- интеграция простая
- API понятный
- audit trail прозрачен
- compliance story понятна
- нет необходимости менять core UX для банка

### Реалистичный MVP scope
1. API-first payment intent / settlement request
2. bank-facing dashboard или demo console
3. transaction status and audit trail
4. simple proof / record model for compliance visibility
5. mock or simulated SWIFT/bank side instead of full real bank integration on day 1

## Что не нужно делать в ближайшем MVP
- полноценный ZK-rollup production stack
- full proof marketplace
- ATM flows
- full reserve auditor network
- broad multicurrency system
- собственный consumer wallet

## Сильные сигналы из Business Plan
- product positioning: B2B infrastructure
- bank pipeline already described
- value proposition: speed + lower cost + compliance + invisible integration
- licensing and audits are a major part of strategy
- first commercial motion depends on regulated trust, not viral adoption

## Главный стратегический вывод
Нужно перестроить основной MVP graph так, чтобы центром был не просто TON payment flow, а:
- bank settlement middleware MVP
- invisible integration
- pilot-ready API product
- demoable compliance/audit layer

## Следствия для плана
Нужно обновить:
- [[mvp/Ценность продукта]]
- [[mvp/Целевая аудитория]]
- [[mvp/Ключевые функции]]
- [[mvp/Архитектура MVP]]
- [[mvp/План разработки MVP]]
- latest MVP plan

## Что ещё стоит извлечь позже
Из документов ещё можно отдельно вынести:
- competitor map
- licensing milestones
- bank pipeline
- revenue model
- phased rollout
