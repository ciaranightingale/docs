---
slug: /solana/react.usemintnft
title: useMintNFT() function
hide_title: true
displayed_sidebar: react
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

## useMintNFT() function

Mint NFTs on your NFT program

## Example

```jsx
import { useProgram, useMintNFT } from "@thirdweb-dev/react/solana";

export default function Component() {
  const program = useProgram("{{program_address}}");
  const { mutateAsync: mint, isLoading, error } = useMintNFT(program);

  function mintNFT() {
    const metadata = { name: "First NFT", description: "This is a cool NFT!" };
    mint({ to: "{{wallet_address}}", metadata });
  }

  return <button onClick={() => mintNFT()}>Mint</button>;
}
```

**Signature:**

```typescript
export declare function useMintNFT(
  program: RequiredParam<NFTCollection>,
): import("@tanstack/react-query").UseMutationResult<
  string,
  unknown,
  MintNFTParams,
  unknown
>;
```

## Parameters

| Parameter | Type                               | Description                     |
| --------- | ---------------------------------- | ------------------------------- |
| program   | RequiredParam&lt;NFTCollection&gt; | The NFT program to mint NFTs to |

**Returns:**

import("@tanstack/react-query").UseMutationResult&lt;string, unknown, MintNFTParams, unknown&gt;