# Tokenization Service

Asset onboarding, AI-driven evaluation, and token issuance on Taproot Assets.

## Responsibility

- Accept asset metadata, documents, and valuation inputs
- AI/ML model assessment of risk, projected ROI, market timing
- Interface with `tapd` to mint Taproot Assets on-chain
- Split a single asset token into N fractional units

## Flow

```
User submits asset → Ingestor validates → AI Evaluator scores →
  If approved → Token Issuer mints on Taproot Assets →
    Fractionalization Engine creates tradable units
```

## Technology

Python 3.11+ / FastAPI

## Port

`:8002`
