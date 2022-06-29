# Interface: PercentageTransferRestrictionInput

[types](../wiki/types).PercentageTransferRestrictionInput

## Hierarchy

- `TransferRestrictionInputBase`

  ↳ **`PercentageTransferRestrictionInput`**

## Table of contents

### Properties

- [exemptedIdentities](../wiki/types.PercentageTransferRestrictionInput#exemptedidentities)
- [percentage](../wiki/types.PercentageTransferRestrictionInput#percentage)

## Properties

### exemptedIdentities

• `Optional` **exemptedIdentities**: (`string` \| [`Identity`](../wiki/api.entities.Identity.Identity))[]

array of Identities (or DIDs) that are exempted from the Restriction

#### Inherited from

TransferRestrictionInputBase.exemptedIdentities

#### Defined in

[types/index.ts:1249](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L1249)

___

### percentage

• **percentage**: `BigNumber`

maximum percentage (0-100) of the total supply of the Asset that can be held by a single investor at once

#### Defined in

[types/index.ts:1274](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L1274)
