# Interface: AddInstructionParams

[api/procedures/addInstruction](../wiki/api.procedures.addInstruction).AddInstructionParams

## Hierarchy

- **`AddInstructionParams`**

  ↳ [`AddInstructionWithVenueIdParams`](../wiki/api.procedures.addInstruction.AddInstructionWithVenueIdParams)

## Table of contents

### Properties

- [endBlock](../wiki/api.procedures.addInstruction.AddInstructionParams#endblock)
- [legs](../wiki/api.procedures.addInstruction.AddInstructionParams#legs)
- [tradeDate](../wiki/api.procedures.addInstruction.AddInstructionParams#tradedate)
- [valueDate](../wiki/api.procedures.addInstruction.AddInstructionParams#valuedate)

## Properties

### endBlock

• `Optional` **endBlock**: `BigNumber`

block at which the Instruction will be executed automatically (optional, the Instruction will be executed when all participants have authorized it if not supplied)

#### Defined in

[api/procedures/addInstruction.ts:63](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/addInstruction.ts#L63)

___

### legs

• **legs**: { `amount`: `BigNumber` ; `asset`: `string` \| [`Asset`](../wiki/api.entities.Asset.Asset) ; `from`: [`PortfolioLike`](../wiki/types#portfoliolike) ; `to`: [`PortfolioLike`](../wiki/types#portfoliolike)  }[]

array of Asset movements (amount, from, to, asset)

#### Defined in

[api/procedures/addInstruction.ts:46](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/addInstruction.ts#L46)

___

### tradeDate

• `Optional` **tradeDate**: `Date`

date at which the trade was agreed upon (optional, for off chain trades)

#### Defined in

[api/procedures/addInstruction.ts:55](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/addInstruction.ts#L55)

___

### valueDate

• `Optional` **valueDate**: `Date`

date at which the trade was executed (optional, for off chain trades)

#### Defined in

[api/procedures/addInstruction.ts:59](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/addInstruction.ts#L59)
