# Техстек MVP
tags: #mvp #stack

Связано:
- [[MVP]]
- [[mvp/Архитектура MVP]]
- [[mvp/План разработки MVP]]

## Принципы выбора
- $0 бюджет
- open-source first
- minimal infrastructure
- один разработчик

## Предпочтительный стек
- Frontend: simple web app или Telegram Mini App
- Wallet integration: существующий TON wallet connect/sign flow
- Backend: Node.js только если без него нельзя
- Storage: file-based или SQLite
- Hosting: static / cheapest possible

## Что избегаем
- сложный DevOps
- ранний микросервисный зоопарк
- своя wallet-инфраструктура
- своя chain-инфраструктура
