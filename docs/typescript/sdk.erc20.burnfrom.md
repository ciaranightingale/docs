---
slug: /sdk.erc20.burnfrom
title: Erc20.burnFrom() method
hide_title: true
displayed_sidebar: typescript
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

## Erc20.burnFrom() method

Burn Tokens

## Example

```javascript
// Address of the wallet sending the tokens
const holderAddress = "{{wallet_address}}";

// The amount of this token you want to burn
const amount = 1.2;

await contract.erc20.burnFrom(holderAddress, amount);
```

**Signature:**

```typescript
burnFrom(holder: string, amount: Amount): Promise<TransactionResult>;
```

## Parameters

| Parameter | Type                      | Description |
| --------- | ------------------------- | ----------- |
| holder    | string                    |             |
| amount    | [Amount](./sdk.amount.md) |             |

**Returns:**

Promise&lt;[TransactionResult](./sdk.transactionresult.md)&gt;

## Remarks

Burn tokens held by the specified wallet