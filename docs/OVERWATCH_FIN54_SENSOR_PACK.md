# Overwatch -> FIN54 Sensor Pack

FIN54 may consume governed observations from Omarchy Overwatch after Dock/Ingest normalization.

## Principle

**Signals are evidence, not orders.**

Overwatch expands FIN54 situational awareness. It does not gain trading authority and FIN54 does not become an execution engine.

## Initial sensor domains

### Markets
- equities
- FX
- crypto
- commodities
- rates
- credit

### Onchain
- Base
- Ethereum
- Solana
- XRPL
- Hedera
- approved L2s

### Macro
- Federal Reserve
- U.S. Treasury
- BLS
- BEA
- FRED

### Entity intelligence
- SEC / EDGAR
- public company filings
- public corporate registries
- public market/news feeds

## Input contract

FIN54 accepts an `EvidenceEnvelope` with:

- source/provenance
- observation and retrieval timestamps
- LIVE/STALE/ERR/OFF state
- evidence payload
- optional geographic context
- authority.class = OBSERVATION
- authority.executable = false

FIN54 MAY enrich, correlate, summarize, or classify evidence.

FIN54 MUST NOT:

- silently convert model summaries to source facts
- erase provenance
- convert correlation into causation
- route a trade directly from an observation
- inject credentials
- bypass AEGIS or the Execution Envelope

## Corridor

```text
Overwatch
  -> Dock / Ingest
  -> EvidenceEnvelope
  -> FIN54 MarketEvidence
  -> Ontology / thesis
  -> ATG
  -> compiled risk
  -> Execution Envelope
  -> AEGIS / fiscal gates
  -> approved execution adapter
  -> receipt
  -> audit / drift
```
