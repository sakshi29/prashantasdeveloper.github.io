# Interface: CountTransferRestrictionInput

[types](../wiki/types).CountTransferRestrictionInput

## Hierarchy

- `TransferRestrictionInputBase`

  ↳ **`CountTransferRestrictionInput`**

## Table of contents

### Properties

- [count](../wiki/types.CountTransferRestrictionInput#count)
- [exemptedIdentities](../wiki/types.CountTransferRestrictionInput#exemptedidentities)

## Properties

### count

• **count**: `BigNumber`

limit on the amount of different (unique) investors that can hold the Asset at once

#### Defined in

[types/index.ts:1267](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L1267)

___

### exemptedIdentities

• `Optional` **exemptedIdentities**: (`string` \| [`Identity`](../wiki/api.entities.Identity.Identity))[]

array of Identities (or DIDs) that are exempted from the Restriction

#### Inherited from

TransferRestrictionInputBase.exemptedIdentities

#### Defined in

[types/index.ts:1249](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L1249)
