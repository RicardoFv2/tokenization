# Marketplace Service

Order matching, Multisig escrow, and fee extraction.

## Responsibility

- Maintain buy/sell orders for each tokenized asset
- Pair compatible orders (price + quantity)
- Create 2-of-3 multisig (buyer, seller, platform) for each trade
- Deduct platform commission and route to Education Treasury
- Finalize token transfer upon escrow release

## Multisig Flow

```
1. Buyer places order → sats locked in 2-of-3 multisig address
2. Seller confirms availability → tokens held in escrow
3. Both parties sign → settlement executes atomically
4. Dispute? → Platform acts as arbiter (3rd key)
```

## Technology

Python 3.11+ / FastAPI

## Port

`:8003`
