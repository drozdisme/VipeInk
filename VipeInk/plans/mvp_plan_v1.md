# MVP Plan v1
tags: #mvp #plan #roadmap

Version: 1
Date: 2026-04-14
Status: active

## Vision
Build the simplest usable TON-based stablecoin payment workflow that can be launched by one developer in 2-4 weeks with near-zero infrastructure cost.

Long-term vision from current vault materials points toward a larger programmable settlement system, potentially including fiat abstraction and advanced chain infrastructure. That is explicitly out of MVP scope.

## Core functionality (strict MVP scope)
1. Payment intent creation
- user can define a payment action inside a simple interface
- includes amount, asset, recipient, and memo/reference

2. Wallet handoff
- user signs through an existing TON wallet
- do not build a new wallet

3. Transaction preparation
- build or prefill a transaction request using existing TON wallet patterns
- basic fee visibility

4. Payment status tracking
- show pending / sent / confirmed / failed
- keep simple transaction log

5. Optional narrow feature
- stablecoin transfer first
- swaps only if they are required for launch use case and can be implemented cheaply

## Explicit non-goals for MVP
- custom L2 / ZK rollup
- custom prover / sequencer / bridge
- bank API integration
- ATM cash flow integration
- compliance automation stack
- new self-custodial wallet product
- institutional multi-rail settlement

## Tech stack
Preferred stack under $0 constraint:
- Frontend: simple web app or Telegram Mini App
- Wallet integration: existing TON wallet connection flow
- Backend: minimal Node.js service only if strictly required
- Storage: local file / lightweight SQLite / zero-cost managed free tier only if unavoidable
- Hosting: local-first or cheapest static hosting path
- Docs/planning: Obsidian vault markdown

## Architecture
### MVP architecture
- UI layer
- payment intent builder
- TON wallet connection/signing handoff
- transaction submission via existing TON ecosystem tooling
- transaction status checker
- simple activity log

### Deferred architecture
Keep [[Architecture]] as long-term vision, not implementation target for MVP v1.

## Development phases
### Phase 1: Prototype
Goal: prove a single user can prepare and send one successful payment

Tasks:
- define one concrete payment flow
- define supported asset for launch
- define target wallet integration
- implement payment intent screen
- implement signing handoff
- verify on test or low-risk environment

Exit criteria:
- 1 end-to-end payment flow works reliably

### Phase 2: MVP
Goal: make the flow usable by early testers

Tasks:
- add transaction status states
- add transaction history
- add basic error handling
- improve copy and UX clarity
- document setup and usage

Exit criteria:
- early tester can complete payment without manual developer intervention

### Phase 3: Testing
Goal: validate real user value

Tasks:
- run 5-10 real payment scenarios
- capture failures and confusion points
- measure completion rate and time-to-payment
- decide whether swap support is necessary

Exit criteria:
- validated narrow use case and clear next priority

## Risks
1. Scope inflation from long-term architecture
Mitigation: treat current architecture note as future-state only

2. Missing user segment definition
Mitigation: extract target user from WhitePaper / BusinessPlan before building secondary features

3. Wallet integration friction
Mitigation: design around existing TON wallet UX instead of replacing it

4. Stablecoin and liquidity assumptions may be wrong
Mitigation: start with one supported asset and one path only

5. Repo knowledge is too sparse
Mitigation: convert PDFs into structured notes and decisions

## Previous decisions
- Decision: do not build chain infrastructure in MVP
Reason: incompatible with 2-4 week, 1-developer, $0 constraints

- Decision: do not build a new wallet for MVP
Reason: existing TON wallets already solve the hardest trust and custody problems

- Decision: center MVP on payment workflow simplicity
Reason: likely strongest value with lowest implementation cost

## Rejected approaches
### Build custom ZK-rollup first
Rejected because:
- overengineered for MVP
- impossible within stated constraints
- delays user validation

### Build full fiat on/off ramp stack first
Rejected because:
- regulatory and integration heavy
- high dependency risk
- not needed to validate core product promise

## Next actions
1. Extract WhitePaper and BusinessPlan into markdown notes
2. Define exact user segment
3. Define exact payment scenario to validate first
4. Choose delivery surface: web app vs Telegram Mini App
5. Convert current Architecture note into future-state architecture and create separate MVP architecture note
