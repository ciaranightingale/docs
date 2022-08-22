---
slug: /ERC20DropVote
title: ERC20DropVote
hide_title: true
displayed_sidebar: contracts
---

# ERC20DropVote

BASE: ERC20Vote EXTENSION: SignatureMintERC20, DropSinglePhase The `ERC20Drop` contract uses the `ERC20Vote` contract, along with the `SignatureMintERC20` and `DropSinglePhase` extensions. The &#39;signature minting&#39; mechanism in the `SignatureMintERC20` extension is a way for a contract admin to authorize an external party&#39;s request to mint tokens on the admin&#39;s contract. At a high level, this means you can authorize some external party to mint tokens on your contract, and specify what exactly will be minted by that external party. The `drop` mechanism in the `DropSinglePhase` extension is a distribution mechanism tokens. It lets you set restrictions such as a price to charge, an allowlist etc. when an address atttempts to mint tokens.

## Methods

### DOMAIN_SEPARATOR

```solidity
function DOMAIN_SEPARATOR() external view returns (bytes32)
```

#### Returns

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | bytes32 | undefined   |

### allowance

```solidity
function allowance(address, address) external view returns (uint256)
```

#### Parameters

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | address | undefined   |
| \_1  | address | undefined   |

#### Returns

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | uint256 | undefined   |

### approve

```solidity
function approve(address spender, uint256 amount) external nonpayable returns (bool)
```

#### Parameters

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| spender | address | undefined   |
| amount  | uint256 | undefined   |

#### Returns

| Name | Type | Description |
| ---- | ---- | ----------- |
| \_0  | bool | undefined   |

### balanceOf

```solidity
function balanceOf(address) external view returns (uint256)
```

#### Parameters

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | address | undefined   |

#### Returns

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | uint256 | undefined   |

### burn

```solidity
function burn(uint256 _amount) external nonpayable
```

Lets an owner a given amount of their tokens.

_Caller should own the `_amount` of tokens._

#### Parameters

| Name     | Type    | Description                   |
| -------- | ------- | ----------------------------- |
| \_amount | uint256 | The number of tokens to burn. |

### checkpoints

```solidity
function checkpoints(address account, uint32 pos) external view returns (struct ERC20VotesAlt.Checkpoint)
```

_Get the `pos`-th checkpoint for `account`._

#### Parameters

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| account | address | undefined   |
| pos     | uint32  | undefined   |

#### Returns

| Name | Type                     | Description |
| ---- | ------------------------ | ----------- |
| \_0  | ERC20VotesAlt.Checkpoint | undefined   |

### claim

```solidity
function claim(address _receiver, uint256 _quantity, address _currency, uint256 _pricePerToken, IDropSinglePhase.AllowlistProof _allowlistProof, bytes _data) external payable
```

_Lets an account claim tokens._

#### Parameters

| Name             | Type                            | Description |
| ---------------- | ------------------------------- | ----------- |
| \_receiver       | address                         | undefined   |
| \_quantity       | uint256                         | undefined   |
| \_currency       | address                         | undefined   |
| \_pricePerToken  | uint256                         | undefined   |
| \_allowlistProof | IDropSinglePhase.AllowlistProof | undefined   |
| \_data           | bytes                           | undefined   |

### claimCondition

```solidity
function claimCondition() external view returns (uint256 startTimestamp, uint256 maxClaimableSupply, uint256 supplyClaimed, uint256 quantityLimitPerTransaction, uint256 waitTimeInSecondsBetweenClaims, bytes32 merkleRoot, uint256 pricePerToken, address currency)
```

#### Returns

| Name                           | Type    | Description |
| ------------------------------ | ------- | ----------- |
| startTimestamp                 | uint256 | undefined   |
| maxClaimableSupply             | uint256 | undefined   |
| supplyClaimed                  | uint256 | undefined   |
| quantityLimitPerTransaction    | uint256 | undefined   |
| waitTimeInSecondsBetweenClaims | uint256 | undefined   |
| merkleRoot                     | bytes32 | undefined   |
| pricePerToken                  | uint256 | undefined   |
| currency                       | address | undefined   |

### contractURI

```solidity
function contractURI() external view returns (string)
```

#### Returns

| Name | Type   | Description |
| ---- | ------ | ----------- |
| \_0  | string | undefined   |

### decimals

```solidity
function decimals() external view returns (uint8)
```

#### Returns

| Name | Type  | Description |
| ---- | ----- | ----------- |
| \_0  | uint8 | undefined   |

### delegate

```solidity
function delegate(address delegatee) external nonpayable
```

_Delegate votes from the sender to `delegatee`._

#### Parameters

| Name      | Type    | Description |
| --------- | ------- | ----------- |
| delegatee | address | undefined   |

### delegateBySig

```solidity
function delegateBySig(address delegatee, uint256 nonce, uint256 expiry, uint8 v, bytes32 r, bytes32 s) external nonpayable
```

_Delegates votes from signer to `delegatee`_

#### Parameters

| Name      | Type    | Description |
| --------- | ------- | ----------- |
| delegatee | address | undefined   |
| nonce     | uint256 | undefined   |
| expiry    | uint256 | undefined   |
| v         | uint8   | undefined   |
| r         | bytes32 | undefined   |
| s         | bytes32 | undefined   |

### delegates

```solidity
function delegates(address account) external view returns (address)
```

_Get the address `account` is currently delegating to._

#### Parameters

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| account | address | undefined   |

#### Returns

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | address | undefined   |

### getClaimTimestamp

```solidity
function getClaimTimestamp(address _claimer) external view returns (uint256 lastClaimedAt, uint256 nextValidClaimTimestamp)
```

_Returns the timestamp for when a claimer is eligible for claiming NFTs again._

#### Parameters

| Name      | Type    | Description |
| --------- | ------- | ----------- |
| \_claimer | address | undefined   |

#### Returns

| Name                    | Type    | Description |
| ----------------------- | ------- | ----------- |
| lastClaimedAt           | uint256 | undefined   |
| nextValidClaimTimestamp | uint256 | undefined   |

### getPastTotalSupply

```solidity
function getPastTotalSupply(uint256 blockNumber) external view returns (uint256)
```

_Retrieve the `totalSupply` at the end of `blockNumber`. Note, this value is the sum of all balances. It is but NOT the sum of all the delegated votes! Requirements: - `blockNumber` must have been already mined_

#### Parameters

| Name        | Type    | Description |
| ----------- | ------- | ----------- |
| blockNumber | uint256 | undefined   |

#### Returns

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | uint256 | undefined   |

### getPastVotes

```solidity
function getPastVotes(address account, uint256 blockNumber) external view returns (uint256)
```

_Retrieve the number of votes for `account` at the end of `blockNumber`. Requirements: - `blockNumber` must have been already mined_

#### Parameters

| Name        | Type    | Description |
| ----------- | ------- | ----------- |
| account     | address | undefined   |
| blockNumber | uint256 | undefined   |

#### Returns

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | uint256 | undefined   |

### getVotes

```solidity
function getVotes(address account) external view returns (uint256)
```

_Gets the current votes balance for `account`_

#### Parameters

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| account | address | undefined   |

#### Returns

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | uint256 | undefined   |

### mint

```solidity
function mint(address, uint256) external nonpayable
```

#### Parameters

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | address | undefined   |
| \_1  | uint256 | undefined   |

### mintWithSignature

```solidity
function mintWithSignature(ISignatureMintERC20.MintRequest _req, bytes _signature) external payable returns (address signer)
```

Mints tokens according to the provided mint request.

#### Parameters

| Name        | Type                            | Description                                                    |
| ----------- | ------------------------------- | -------------------------------------------------------------- |
| \_req       | ISignatureMintERC20.MintRequest | The payload / mint request.                                    |
| \_signature | bytes                           | The signature produced by an account signing the mint request. |

#### Returns

| Name   | Type    | Description |
| ------ | ------- | ----------- |
| signer | address | undefined   |

### multicall

```solidity
function multicall(bytes[] data) external nonpayable returns (bytes[] results)
```

_Receives and executes a batch of function calls on this contract._

#### Parameters

| Name | Type    | Description |
| ---- | ------- | ----------- |
| data | bytes[] | undefined   |

#### Returns

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| results | bytes[] | undefined   |

### name

```solidity
function name() external view returns (string)
```

#### Returns

| Name | Type   | Description |
| ---- | ------ | ----------- |
| \_0  | string | undefined   |

### nonces

```solidity
function nonces(address) external view returns (uint256)
```

#### Parameters

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | address | undefined   |

#### Returns

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | uint256 | undefined   |

### numCheckpoints

```solidity
function numCheckpoints(address account) external view returns (uint32)
```

_Get number of checkpoints for `account`._

#### Parameters

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| account | address | undefined   |

#### Returns

| Name | Type   | Description |
| ---- | ------ | ----------- |
| \_0  | uint32 | undefined   |

### owner

```solidity
function owner() external view returns (address)
```

_Returns the owner of the contract._

#### Returns

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | address | undefined   |

### permit

```solidity
function permit(address owner, address spender, uint256 value, uint256 deadline, uint8 v, bytes32 r, bytes32 s) external nonpayable
```

#### Parameters

| Name     | Type    | Description |
| -------- | ------- | ----------- |
| owner    | address | undefined   |
| spender  | address | undefined   |
| value    | uint256 | undefined   |
| deadline | uint256 | undefined   |
| v        | uint8   | undefined   |
| r        | bytes32 | undefined   |
| s        | bytes32 | undefined   |

### primarySaleRecipient

```solidity
function primarySaleRecipient() external view returns (address)
```

_The adress that receives all primary sales value._

#### Returns

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | address | undefined   |

### setClaimConditions

```solidity
function setClaimConditions(IClaimCondition.ClaimCondition _condition, bool _resetClaimEligibility) external nonpayable
```

_Lets a contract admin set claim conditions._

#### Parameters

| Name                    | Type                           | Description |
| ----------------------- | ------------------------------ | ----------- |
| \_condition             | IClaimCondition.ClaimCondition | undefined   |
| \_resetClaimEligibility | bool                           | undefined   |

### setContractURI

```solidity
function setContractURI(string _uri) external nonpayable
```

_Lets a contract admin set the URI for contract-level metadata._

#### Parameters

| Name  | Type   | Description |
| ----- | ------ | ----------- |
| \_uri | string | undefined   |

### setOwner

```solidity
function setOwner(address _newOwner) external nonpayable
```

_Lets a contract admin set a new owner for the contract. The new owner must be a contract admin._

#### Parameters

| Name       | Type    | Description |
| ---------- | ------- | ----------- |
| \_newOwner | address | undefined   |

### setPrimarySaleRecipient

```solidity
function setPrimarySaleRecipient(address _saleRecipient) external nonpayable
```

_Lets a contract admin set the recipient for all primary sales._

#### Parameters

| Name            | Type    | Description |
| --------------- | ------- | ----------- |
| \_saleRecipient | address | undefined   |

### symbol

```solidity
function symbol() external view returns (string)
```

#### Returns

| Name | Type   | Description |
| ---- | ------ | ----------- |
| \_0  | string | undefined   |

### totalSupply

```solidity
function totalSupply() external view returns (uint256)
```

#### Returns

| Name | Type    | Description |
| ---- | ------- | ----------- |
| \_0  | uint256 | undefined   |

### transfer

```solidity
function transfer(address to, uint256 amount) external nonpayable returns (bool)
```

#### Parameters

| Name   | Type    | Description |
| ------ | ------- | ----------- |
| to     | address | undefined   |
| amount | uint256 | undefined   |

#### Returns

| Name | Type | Description |
| ---- | ---- | ----------- |
| \_0  | bool | undefined   |

### transferFrom

```solidity
function transferFrom(address from, address to, uint256 amount) external nonpayable returns (bool)
```

#### Parameters

| Name   | Type    | Description |
| ------ | ------- | ----------- |
| from   | address | undefined   |
| to     | address | undefined   |
| amount | uint256 | undefined   |

#### Returns

| Name | Type | Description |
| ---- | ---- | ----------- |
| \_0  | bool | undefined   |

### verify

```solidity
function verify(ISignatureMintERC20.MintRequest _req, bytes _signature) external view returns (bool success, address signer)
```

_Verifies that a mint request is signed by an account holding MINTER_ROLE (at the time of the function call)._

#### Parameters

| Name        | Type                            | Description |
| ----------- | ------------------------------- | ----------- |
| \_req       | ISignatureMintERC20.MintRequest | undefined   |
| \_signature | bytes                           | undefined   |

#### Returns

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| success | bool    | undefined   |
| signer  | address | undefined   |

### verifyClaim

```solidity
function verifyClaim(address _claimer, uint256 _quantity, address _currency, uint256 _pricePerToken, bool verifyMaxQuantityPerTransaction) external view
```

_Checks a request to claim NFTs against the active claim condition&#39;s criteria._

#### Parameters

| Name                            | Type    | Description |
| ------------------------------- | ------- | ----------- |
| \_claimer                       | address | undefined   |
| \_quantity                      | uint256 | undefined   |
| \_currency                      | address | undefined   |
| \_pricePerToken                 | uint256 | undefined   |
| verifyMaxQuantityPerTransaction | bool    | undefined   |

### verifyClaimMerkleProof

```solidity
function verifyClaimMerkleProof(address _claimer, uint256 _quantity, IDropSinglePhase.AllowlistProof _allowlistProof) external view returns (bool validMerkleProof, uint256 merkleProofIndex)
```

_Checks whether a claimer meets the claim condition&#39;s allowlist criteria._

#### Parameters

| Name             | Type                            | Description |
| ---------------- | ------------------------------- | ----------- |
| \_claimer        | address                         | undefined   |
| \_quantity       | uint256                         | undefined   |
| \_allowlistProof | IDropSinglePhase.AllowlistProof | undefined   |

#### Returns

| Name             | Type    | Description |
| ---------------- | ------- | ----------- |
| validMerkleProof | bool    | undefined   |
| merkleProofIndex | uint256 | undefined   |

## Events

### Approval

```solidity
event Approval(address indexed owner, address indexed spender, uint256 amount)
```

#### Parameters

| Name              | Type    | Description |
| ----------------- | ------- | ----------- |
| owner `indexed`   | address | undefined   |
| spender `indexed` | address | undefined   |
| amount            | uint256 | undefined   |

### ClaimConditionUpdated

```solidity
event ClaimConditionUpdated(IClaimCondition.ClaimCondition condition, bool resetEligibility)
```

#### Parameters

| Name             | Type                           | Description |
| ---------------- | ------------------------------ | ----------- |
| condition        | IClaimCondition.ClaimCondition | undefined   |
| resetEligibility | bool                           | undefined   |

### ContractURIUpdated

```solidity
event ContractURIUpdated(string prevURI, string newURI)
```

#### Parameters

| Name    | Type   | Description |
| ------- | ------ | ----------- |
| prevURI | string | undefined   |
| newURI  | string | undefined   |

### DelegateChanged

```solidity
event DelegateChanged(address indexed delegator, address indexed fromDelegate, address indexed toDelegate)
```

#### Parameters

| Name                   | Type    | Description |
| ---------------------- | ------- | ----------- |
| delegator `indexed`    | address | undefined   |
| fromDelegate `indexed` | address | undefined   |
| toDelegate `indexed`   | address | undefined   |

### DelegateVotesChanged

```solidity
event DelegateVotesChanged(address indexed delegate, uint256 previousBalance, uint256 newBalance)
```

#### Parameters

| Name               | Type    | Description |
| ------------------ | ------- | ----------- |
| delegate `indexed` | address | undefined   |
| previousBalance    | uint256 | undefined   |
| newBalance         | uint256 | undefined   |

### OwnerUpdated

```solidity
event OwnerUpdated(address indexed prevOwner, address indexed newOwner)
```

#### Parameters

| Name                | Type    | Description |
| ------------------- | ------- | ----------- |
| prevOwner `indexed` | address | undefined   |
| newOwner `indexed`  | address | undefined   |

### PrimarySaleRecipientUpdated

```solidity
event PrimarySaleRecipientUpdated(address indexed recipient)
```

#### Parameters

| Name                | Type    | Description |
| ------------------- | ------- | ----------- |
| recipient `indexed` | address | undefined   |

### TokensClaimed

```solidity
event TokensClaimed(address indexed claimer, address indexed receiver, uint256 indexed startTokenId, uint256 quantityClaimed)
```

#### Parameters

| Name                   | Type    | Description |
| ---------------------- | ------- | ----------- |
| claimer `indexed`      | address | undefined   |
| receiver `indexed`     | address | undefined   |
| startTokenId `indexed` | uint256 | undefined   |
| quantityClaimed        | uint256 | undefined   |

### TokensMintedWithSignature

```solidity
event TokensMintedWithSignature(address indexed signer, address indexed mintedTo, ISignatureMintERC20.MintRequest mintRequest)
```

#### Parameters

| Name               | Type                            | Description |
| ------------------ | ------------------------------- | ----------- |
| signer `indexed`   | address                         | undefined   |
| mintedTo `indexed` | address                         | undefined   |
| mintRequest        | ISignatureMintERC20.MintRequest | undefined   |

### Transfer

```solidity
event Transfer(address indexed from, address indexed to, uint256 amount)
```

#### Parameters

| Name           | Type    | Description |
| -------------- | ------- | ----------- |
| from `indexed` | address | undefined   |
| to `indexed`   | address | undefined   |
| amount         | uint256 | undefined   |