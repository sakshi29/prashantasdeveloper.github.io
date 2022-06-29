# Interface: CountTransferRestriction

[types](../wiki/types).CountTransferRestriction

## Hierarchy

- `TransferRestrictionBase`

  ↳ **`CountTransferRestriction`**

## Table of contents

### Properties

- [count](../wiki/types.CountTransferRestriction#count)
- [exemptedIds](../wiki/types.CountTransferRestriction#exemptedids)

## Properties

### count

• **count**: `BigNumber`

#### Defined in

[types/index.ts:1253](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L1253)

___

### exemptedIds

• `Optional` **exemptedIds**: `string`[]

array of Scope/Identity IDs that are exempted from the Restriction

**`note`** if the Asset requires investor uniqueness, Scope IDs are used. Otherwise, we use Identity IDs. More on Scope IDs and investor uniqueness
  [here](https://developers.polymesh.network/introduction/identity#polymesh-unique-identity-system-puis) and
  [here](https://developers.polymesh.network/polymesh-docs/primitives/confidential-identity)

#### Inherited from

TransferRestrictionBase.exemptedIds

#### Defined in

[types/index.ts:1242](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L1242)
