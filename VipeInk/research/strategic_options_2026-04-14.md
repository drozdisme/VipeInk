# Strategic Options 2026-04-14
tags: #strategy #mvp #l2 #ton

Связано:
- [[MVP]]
- [[Future Architecture]]
- [[Следующие шаги]]

## Новая рамка
Vipeink не должен застревать только в bank middleware narrative.

Нужно смотреть шире: как быстрее и дешевле пробиться к реальному запуску, traction и капиталу, используя идею TON-based L2 / settlement layer.

## Критерии выбора пути
- 1 developer friendly
- 2-4 weeks for meaningful prototype
- near $0 cash burn
- возможность податься в grants / contests / ecosystem support
- понятный demo
- не требовать full regulated rollout на старте

## Вариант A — Bank middleware MVP
### Плюсы
- ближе всего к WhitePaper и BusinessPlan narrative
- сильная enterprise value proposition
- хорош для investor story

### Минусы
- длинный sales cycle
- тяжёлый compliance narrative
- сложно быстро показать traction

### Вывод
Хорош как strategic north star, но слаб как fastest wedge.

## Вариант B — TON L2 / settlement demo infrastructure
### Что это
Показать Vipeink как упрощённый L2 execution / settlement layer на TON:
- intent-based settlement requests
- state tracking
- proof / audit record
- minimal rollup-like sequencing abstraction
- API + demo UI

### Плюсы
- ближе к core tech identity
- хорошо ложится на grants / infra narrative
- можно показать техническую уникальность без банковского go-live

### Минусы
- есть риск сделать слишком research-heavy демо
- нужен очень жёсткий scope, чтобы не утонуть

### Вывод
Один из лучших путей для короткого старта, если не строить real rollup, а строить convincing L2 MVP shell.

## Вариант C — Telegram / TON app wedge on top of settlement layer
### Что это
Сделать user-facing demo app или mini app, использующий Vipeink как backend settlement abstraction.

### Плюсы
- проще показать пользователям и grant reviewers
- быстрее получить demo traction
- использует Telegram distribution angle

### Минусы
- может размыть B2B positioning
- может выглядеть как ещё один app без infra moat

### Вывод
Хорош как оболочка для demo, но не как весь продукт.

## Рекомендуемый путь сейчас
### Best current path
Собирать MVP как:
- Vipeink = TON settlement / L2 abstraction layer
- bank middleware = один из strongest narratives / verticals
- demo surface = lightweight console or mini app

То есть не выбирать только один угол, а собрать один core, который можно подавать в 3 нарративах:
1. TON L2 infrastructure
2. settlement middleware for banks
3. payment abstraction layer for TON apps

## Что строить в ближайшие 2-4 недели
1. Settlement Request API
2. minimal sequencer / state tracker abstraction
3. audit / proof record layer
4. demo console
5. one or two vertical demos:
   - bank settlement demo
   - TON app / mini app demo

## Grants / contests / support paths
### TON ecosystem
- TON Champion Grants: high-impact projects in payments / infra / AI
- TON Builders Portal partner offers: infra credits, TON API credits, audit discounts, marketing support
- TON Hub / hackathon routes for visibility and early traction

### Useful support found
- TON Foundation support ecosystem via Builders Portal
- AWS credits / Yandex credits / TON API credits / TonBit discounts
- Fluence compute grants for infra-heavy TON projects

## Tactical implication
Нужно готовить не только product graph, но и:
- grant-ready one pager
- contest-ready pitch angle
- technical demo scope with short build horizon

## Decision
Short-term product framing:
- primary build framing: TON settlement / L2 abstraction MVP
- secondary framing: bank-facing middleware
- optional showcase framing: Telegram-facing demo experience
