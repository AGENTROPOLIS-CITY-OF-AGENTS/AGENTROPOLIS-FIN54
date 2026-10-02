# FIN54 Institutional Onchain Movement Index (IOMI)

## Role
FIN54 owns the canonical machine benchmark for regulated and institutional asset movement onchain.

## Canonical rule
Signals are evidence, not orders. Market movement may change agent posture, research depth, simulation priority, monitoring cadence, or a governed execution envelope. It MUST NOT directly authorize capital movement.

## Pipeline
Institutional / onchain data -> FIN54 -> MarketEvidence -> Ontology / Thesis -> ATG -> compiled risk -> Execution Envelope -> AEGIS / Fiscal gates -> execution adapter -> receipt -> audit / drift

## Required dimensions
- institution
- asset class
- network / rail
- jurisdiction
- event type
- notional value
- observed volume
- settlement velocity
- flow acceleration
- concentration
- provenance
- confidence
- timestamp
- regulatory state

## Canonical metrics
- OIV: Onchain Institutional Volume
- AMR: Asset Migration Rate
- IFV: Institutional Flow Velocity
- OPR: Onchain Penetration Ratio
- Network Concentration
- Asset-Class Concentration
- Counterparty Concentration
- Settlement Velocity
- Flow Acceleration

## Institutional regime states
R0 OFFCHAIN
R1 EXPERIMENTAL
R2 TOKENIZING
R3 SETTLING
R4 INTEROPERATING
R5 LIQUID
R6 SYSTEMIC

## Evidence source families
RLN / RSN, tokenized commercial bank deposits, tokenized Treasuries, bonds, funds, stablecoins, securities, public chains, permissioned ledgers, settlement networks, interoperable rails, market infrastructure providers, and verified institutional disclosures.

## Output contract
FIN54 emits normalized MarketEvidence objects and benchmark snapshots. It does not issue trading commands.

## Acceptance criteria
- no raw signal can invoke an execution adapter
- every metric has provenance and confidence
- issuance, transfer, settlement, collateral movement, and speculative trading are distinguishable
- benchmark calculations are reproducible
- all consequential downstream actions remain AEGIS-gated and receipted
