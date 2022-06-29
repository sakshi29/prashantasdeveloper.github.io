# Interface: CreateAssetWithTickerParams

[api/procedures/createAsset](../wiki/api.procedures.createAsset).CreateAssetWithTickerParams

## Hierarchy

- [`CreateAssetParams`](../wiki/api.procedures.createAsset.CreateAssetParams)

  ↳ **`CreateAssetWithTickerParams`**

## Table of contents

### Properties

- [assetType](../wiki/api.procedures.createAsset.CreateAssetWithTickerParams#assettype)
- [documents](../wiki/api.procedures.createAsset.CreateAssetWithTickerParams#documents)
- [fundingRound](../wiki/api.procedures.createAsset.CreateAssetWithTickerParams#fundinground)
- [initialSupply](../wiki/api.procedures.createAsset.CreateAssetWithTickerParams#initialsupply)
- [isDivisible](../wiki/api.procedures.createAsset.CreateAssetWithTickerParams#isdivisible)
- [name](../wiki/api.procedures.createAsset.CreateAssetWithTickerParams#name)
- [requireInvestorUniqueness](../wiki/api.procedures.createAsset.CreateAssetWithTickerParams#requireinvestoruniqueness)
- [securityIdentifiers](../wiki/api.procedures.createAsset.CreateAssetWithTickerParams#securityidentifiers)
- [ticker](../wiki/api.procedures.createAsset.CreateAssetWithTickerParams#ticker)

## Properties

### assetType

• **assetType**: `string`

type of security that the Asset represents (i.e. Equity, Debt, Commodity, etc). Common values are included in the
  [KnownAssetType](../wiki/types.KnownAssetType) enum, but custom values can be used as well. Custom values must be registered on-chain the first time
  they're used, requiring an additional transaction. They aren't tied to a specific Asset

#### Inherited from

[CreateAssetParams](../wiki/api.procedures.createAsset.CreateAssetParams).[assetType](../wiki/api.procedures.createAsset.CreateAssetParams#assettype)

#### Defined in

[api/procedures/createAsset.ts:45](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/createAsset.ts#L45)

___

### documents

• `Optional` **documents**: [`AssetDocument`](../wiki/types.AssetDocument)[]

#### Inherited from

[CreateAssetParams](../wiki/api.procedures.createAsset.CreateAssetParams).[documents](../wiki/api.procedures.createAsset.CreateAssetParams#documents)

#### Defined in

[api/procedures/createAsset.ts:54](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/createAsset.ts#L54)

___

### fundingRound

• `Optional` **fundingRound**: `string`

(optional) funding round in which the Asset currently is (Series A, Series B, etc)

#### Inherited from

[CreateAssetParams](../wiki/api.procedures.createAsset.CreateAssetParams).[fundingRound](../wiki/api.procedures.createAsset.CreateAssetParams#fundinground)

#### Defined in

[api/procedures/createAsset.ts:53](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/createAsset.ts#L53)

___

### initialSupply

• `Optional` **initialSupply**: `BigNumber`

amount of Asset tokens that will be minted on creation (optional, default doesn't mint)

#### Inherited from

[CreateAssetParams](../wiki/api.procedures.createAsset.CreateAssetParams).[initialSupply](../wiki/api.procedures.createAsset.CreateAssetParams#initialsupply)

#### Defined in

[api/procedures/createAsset.ts:35](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/createAsset.ts#L35)

___

### isDivisible

• **isDivisible**: `boolean`

whether a single Asset token can be divided into decimal parts

#### Inherited from

[CreateAssetParams](../wiki/api.procedures.createAsset.CreateAssetParams).[isDivisible](../wiki/api.procedures.createAsset.CreateAssetParams#isdivisible)

#### Defined in

[api/procedures/createAsset.ts:39](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/createAsset.ts#L39)

___

### name

• **name**: `string`

#### Inherited from

[CreateAssetParams](../wiki/api.procedures.createAsset.CreateAssetParams).[name](../wiki/api.procedures.createAsset.CreateAssetParams#name)

#### Defined in

[api/procedures/createAsset.ts:31](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/createAsset.ts#L31)

___

### requireInvestorUniqueness

• **requireInvestorUniqueness**: `boolean`

whether this asset requires investors to have a Investor Uniqueness Claim in order
  to hold it. More information about Investor Uniqueness and PUIS [here](https://developers.polymesh.live/introduction/identity#polymesh-unique-identity-system-puis)

#### Inherited from

[CreateAssetParams](../wiki/api.procedures.createAsset.CreateAssetParams).[requireInvestorUniqueness](../wiki/api.procedures.createAsset.CreateAssetParams#requireinvestoruniqueness)

#### Defined in

[api/procedures/createAsset.ts:59](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/createAsset.ts#L59)

___

### securityIdentifiers

• `Optional` **securityIdentifiers**: [`SecurityIdentifier`](../wiki/types.SecurityIdentifier)[]

array of domestic or international alphanumeric security identifiers for the Asset (ISIN, CUSIP, FIGI, etc)

#### Inherited from

[CreateAssetParams](../wiki/api.procedures.createAsset.CreateAssetParams).[securityIdentifiers](../wiki/api.procedures.createAsset.CreateAssetParams#securityidentifiers)

#### Defined in

[api/procedures/createAsset.ts:49](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/createAsset.ts#L49)

___

### ticker

• **ticker**: `string`

#### Defined in

[api/procedures/createAsset.ts:63](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/createAsset.ts#L63)
