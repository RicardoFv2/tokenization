# Wallet Service

Bitcoin custody, Lightning Network payments, and balance management.

## Responsibility

- HD wallet derivation (BIP-84/86), encrypted seed storage
- gRPC connection to LND for invoice creation, payment, and routing
- Aggregates on-chain + Lightning + token balances per user
- Persists every inbound/outbound movement with blockchain proof

## Technology

Python 3.11+ / FastAPI

## Port

`:8001`

## External Dependencies

Bitcoin Core (RPC), LND (gRPC), Taproot Assets daemon.

## Security

- Private keys never leave the Key Manager module.
- All seed material encrypted with AES-256-GCM at rest.
- Wallet operations require JWT + optional 2FA.
