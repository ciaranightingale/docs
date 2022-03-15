---
slug: /sdk.marketplace.getactivelistings
title: Marketplace.getActiveListings() method
hide_title: true
---
<!-- Do not edit this file. It is automatically generated by API Documenter. -->


## Marketplace.getActiveListings() method

Get all active listings

**Signature:**

```typescript
getActiveListings(): Promise<(AuctionListing | DirectListing)[]>;
```
**Returns:**

Promise&lt;([AuctionListing](./sdk.auctionlisting.md) \| [DirectListing](./sdk.directlisting.md))\[\]&gt;

## Remarks

Fetch all the active listings from this marketplace contract.

## Example


```javascript
const listings = await contract.getActiveListings();
const priceOfFirstActiveListing = listings[0].price;
```