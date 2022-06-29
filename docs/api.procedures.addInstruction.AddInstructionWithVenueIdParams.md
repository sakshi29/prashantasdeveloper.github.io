# Interface: AddInstructionWithVenueIdParams

[api/procedures/addInstruction](../wiki/api.procedures.addInstruction).AddInstructionWithVenueIdParams

## Hierarchy

- [`AddInstructionParams`](../wiki/api.procedures.addInstruction.AddInstructionParams)

  ↳ **`AddInstructionWithVenueIdParams`**

## Table of contents

### Properties

- [endBlock](../wiki/api.procedures.addInstruction.AddInstructionWithVenueIdParams#endblock)
- [legs](../wiki/api.procedures.addInstruction.AddInstructionWithVenueIdParams#legs)
- [tradeDate](../wiki/api.procedures.addInstruction.AddInstructionWithVenueIdParams#tradedate)
- [valueDate](../wiki/api.procedures.addInstruction.AddInstructionWithVenueIdParams#valuedate)
- [venueId](../wiki/api.procedures.addInstruction.AddInstructionWithVenueIdParams#venueid)

## Properties

### endBlock

• `Optional` **endBlock**: `BigNumber`

block at which the Instruction will be executed automatically (optional, the Instruction will be executed when all participants have authorized it if not supplied)

#### Inherited from

[AddInstructionParams](../wiki/api.procedures.addInstruction.AddInstructionParams).[endBlock](../wiki/api.procedures.addInstruction.AddInstructionParams#endblock)

#### Defined in

[api/procedures/addInstruction.ts:63](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/addInstruction.ts#L63)

___

### legs

• **legs**: { `amount`: `BigNumber` ; `asset`: `string` \| [`Asset`](../wiki/api.entities.Asset.Asset) ; `from`: [`PortfolioLike`](../wiki/types#portfoliolike) ; `to`: [`PortfolioLike`](../wiki/types#portfoliolike)  }[]

array of Asset movements (amount, from, to, asset)

#### Inherited from

[AddInstructionParams](../wiki/api.procedures.addInstruction.AddInstructionParams).[legs](../wiki/api.procedures.addInstruction.AddInstructionParams#legs)

#### Defined in

[api/procedures/addInstruction.ts:46](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/addInstruction.ts#L46)

___

### tradeDate

• `Optional` **tradeDate**: `Date`

date at which the trade was agreed upon (optional, for off chain trades)

#### Inherited from

[AddInstructionParams](../wiki/api.procedures.addInstruction.AddInstructionParams).[tradeDate](../wiki/api.procedures.addInstruction.AddInstructionParams#tradedate)

#### Defined in

[api/procedures/addInstruction.ts:55](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/addInstruction.ts#L55)

___

### valueDate

• `Optional` **valueDate**: `Date`

date at which the trade was executed (optional, for off chain trades)

#### Inherited from

[AddInstructionParams](../wiki/api.procedures.addInstruction.AddInstructionParams).[valueDate](../wiki/api.procedures.addInstruction.AddInstructionParams#valuedate)

#### Defined in

[api/procedures/addInstruction.ts:59](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/addInstruction.ts#L59)

___

### venueId

• **venueId**: `BigNumber`

#### Defined in

[api/procedures/addInstruction.ts:74](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/addInstruction.ts#L74)
