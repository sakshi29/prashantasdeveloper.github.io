# Class: Settlements

[api/client/Settlements](../wiki/api.client.Settlements).Settlements

Handles all Settlement related functionality

## Table of contents

### Methods

- [addInstruction](../wiki/api.client.Settlements.Settlements#addinstruction)
- [affirmInstruction](../wiki/api.client.Settlements.Settlements#affirminstruction)
- [createVenue](../wiki/api.client.Settlements.Settlements#createvenue)
- [getInstruction](../wiki/api.client.Settlements.Settlements#getinstruction)
- [getVenue](../wiki/api.client.Settlements.Settlements#getvenue)

## Methods

### addInstruction

▸ **addInstruction**(`args`, `opts?`): `Promise`<`TransactionQueue`<[`Instruction`](../wiki/api.entities.Instruction.Instruction)[], [`Instruction`](../wiki/api.entities.Instruction.Instruction), `unknown`[][]\>\>

Create an Instruction to exchange Assets

**`note`** this method is of type [ProcedureMethod](../wiki/types.ProcedureMethod), which means you can call [addInstruction.checkAuthorization](../wiki/types.ProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `args` | [`AddInstructionWithVenueIdParams`](../wiki/api.procedures.addInstruction.AddInstructionWithVenueIdParams) |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<[`Instruction`](../wiki/api.entities.Instruction.Instruction)[], [`Instruction`](../wiki/api.entities.Instruction.Instruction), `unknown`[][]\>\>

#### Defined in

[api/client/Settlements.ts:118](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/client/Settlements.ts#L118)

___

### affirmInstruction

▸ **affirmInstruction**(`args`, `opts?`): `Promise`<`TransactionQueue`<[`Instruction`](../wiki/api.entities.Instruction.Instruction), [`Instruction`](../wiki/api.entities.Instruction.Instruction), `unknown`[][]\>\>

Affirm an Instruction (authorize)

**`note`** this method is of type [ProcedureMethod](../wiki/types.ProcedureMethod), which means you can call [affirmInstruction.checkAuthorization](../wiki/types.ProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `args` | [`AffirmInstructionParams`](../wiki/api.procedures.modifyInstructionAffirmation.AffirmInstructionParams) |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<[`Instruction`](../wiki/api.entities.Instruction.Instruction), [`Instruction`](../wiki/api.entities.Instruction.Instruction), `unknown`[][]\>\>

#### Defined in

[api/client/Settlements.ts:128](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/client/Settlements.ts#L128)

___

### createVenue

▸ **createVenue**(`args`, `opts?`): `Promise`<`TransactionQueue`<[`Venue`](../wiki/api.entities.Venue.Venue), [`Venue`](../wiki/api.entities.Venue.Venue), `unknown`[][]\>\>

Create a Venue under the ownership of the signing Identity

**`note`** this method is of type [ProcedureMethod](../wiki/types.ProcedureMethod), which means you can call [createVenue.checkAuthorization](../wiki/types.ProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `args` | [`CreateVenueParams`](../wiki/api.procedures.createVenue.CreateVenueParams) |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<[`Venue`](../wiki/api.entities.Venue.Venue), [`Venue`](../wiki/api.entities.Venue.Venue), `unknown`[][]\>\>

#### Defined in

[api/client/Settlements.ts:108](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/client/Settlements.ts#L108)

___

### getInstruction

▸ **getInstruction**(`args`): `Promise`<[`Instruction`](../wiki/api.entities.Instruction.Instruction)\>

Retrieve an Instruction by its ID

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `args` | `Object` | - |
| `args.id` | `BigNumber` | identifier number of the Instruction |

#### Returns

`Promise`<[`Instruction`](../wiki/api.entities.Instruction.Instruction)\>

#### Defined in

[api/client/Settlements.ts:86](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/client/Settlements.ts#L86)

___

### getVenue

▸ **getVenue**(`args`): `Promise`<[`Venue`](../wiki/api.entities.Venue.Venue)\>

Retrieve a Venue by its ID

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `args` | `Object` | - |
| `args.id` | `BigNumber` | identifier number of the Venue |

#### Returns

`Promise`<[`Venue`](../wiki/api.entities.Venue.Venue)\>

#### Defined in

[api/client/Settlements.ts:65](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/client/Settlements.ts#L65)
