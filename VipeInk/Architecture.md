---
config:
  layout: fixed
  theme: base
  look: neo
---

```mermaid
flowchart TB

%% ================= USERS =================
subgraph Users["Уровень Пользователей"]
    U1["Пользователь 1 (EUR)"]
    U2["Пользователь 2 (USD)"]
    U3["Пользователь N"]

    Wallet["Кошелёк Tonkeeper
    • Intent batching
    • Симуляция TX
    • TON DNS
    • MEV-защита"]

    TXBuilder["Transaction Builder / Intent API
    • Подпись
    • Replay protection
    • Fee check
    • SWIFT metadata"]
end

%% ================= CONVERTER =================
subgraph Converter["Converter Service (Centralized)"]
    AccountMapper["Account → Wallet Mapper
    • Bank → Wallet
    • AES-256"]

    FiatMint["Fiat Minting
    • EUR/USD → EUR@/USD@
    • Atomic batch"]

    ArakulaOracleRef["Arakula Oracle
    • FX rates
    • Proof-of-Reserves"]
end

%% ================= L2 =================
subgraph L2["ZK-Rollup Layer L2"]
    PM["MEV-защищённый mempool"]
    SC["Sequencer Committee"]
    A["Aggregator / Sequencer"]
    ZKP["ZK-Prover"]
    ProofMarket["Proof Marketplace"]
    SR["State Root Manager"]
    SS["Snapshot Service"]
    EX["Explorer"]

    Stablecoins["Стейблкоины (USD@, EUR@)"]
    RevertManager["Revert Manager"]
    DummyTX["SWIFT Dummy TX"]
    ZKBalanceCheck["ZK Balance Verifier"]
end

%% ================= L1 =================
subgraph L1["TON Base Layer L1"]
    subgraph MC["MasterChain"]
        ZKVC["ZK Verifier"]
        SRC["State Root Registry"]
        ARC["Aggregator Registry"]
        FO["Finality Oracle"]
        SWIFTL1["SWIFT Logger"]
    end

    subgraph WC["WorkChains"]
        WC1["Shard 1"]
        WC2["Shard 2"]
        WCN["Shard N"]
    end

    subgraph DS["Data Availability"]
        DS1["Shard 1"]
        DS2["Shard 2"]
        DSN["Shard N"]
    end
end

%% ================= SECURITY =================
subgraph Security["Безопасность"]
    PoS["PoS"]
    BFT["BFT"]
    Slashing["Slashing"]
    CP["CP"]
    EmergencyPause["Emergency Pause"]
    ComplianceLayer["Compliance (KYC/AML)"]
    MPCNetwork["MPC Network"]
end

%% ================= BRIDGE =================
subgraph Bridge["L1 ↔ L2 Bridge"]
    Deposit["Deposit"]
    WP["Withdraw"]
    Merkle["Merkle Proof"]
    MsgBridge["SWIFT Bridge"]
    Watcher["Watcher"]
end

%% ================= ATM =================
subgraph ATM["ATM / Fiat"]
    ATMUser["User"]
    ATMCash["ATM"]
    BankAPI["Bank API"]
    YourBank["Bank"]
    FiatAccount["Account"]
    ATMKYC["KYC Module"]
end

%% ================= ARAKULA =================
subgraph Arakula["Arakula Network"]
    ArakulaOracle["Oracle"]
    TWAP["TWAP"]
    MintRouter["Mint Router"]
    BurnRouter["Burn Router"]
    LiquidityHub["Liquidity Hub"]
    SettlementLayer["Settlement"]
    ReserveAuditor["Reserve Auditor"]
end

%% ================= FLOWS =================

U1 --> TXBuilder
U2 --> TXBuilder
U3 --> TXBuilder
Wallet --> TXBuilder

TXBuilder --> PM
PM --> A
A --> SR
SR --> SRC

A --> ZKP
ZKP --> ProofMarket
ProofMarket --> ZKVC

Deposit --> WC1
SRC --> Merkle
Merkle --> WP

WP --> U1
WP --> U2
WP --> U3

A --> Stablecoins
Stablecoins --> U2

%% SWAP FLOW
U1 --> Wallet
Wallet --> TXBuilder
PM --> SettlementLayer
SettlementLayer --> LiquidityHub
LiquidityHub --> Stablecoins

%% ATM FLOW
ATMUser --> ATMCash
ATMCash --> BankAPI
BankAPI --> WP
WP --> Stablecoins
BankAPI --> YourBank
YourBank --> FiatAccount
FiatAccount --> ATMUser

%% ORACLE
FiatMint --> MintRouter
MintRouter --> Stablecoins
BurnRouter --> Stablecoins

ReserveAuditor --> ArakulaOracle
TWAP --> LiquidityHub