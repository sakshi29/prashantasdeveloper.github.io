# Interface: ProcedureMethod<MethodArgs, ProcedureReturnValue, ReturnValue\>

[types](../wiki/types).ProcedureMethod

## Type parameters

| Name | Type |
| :------ | :------ |
| `MethodArgs` | `MethodArgs` |
| `ProcedureReturnValue` | `ProcedureReturnValue` |
| `ReturnValue` | `ProcedureReturnValue` |

## Callable

### ProcedureMethod

▸ **ProcedureMethod**(`args`, `opts?`): `Promise`<`TransactionQueue`<`ProcedureReturnValue`, `ReturnValue`, `unknown`[][]\>\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `args` | `MethodArgs` |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<`ProcedureReturnValue`, `ReturnValue`, `unknown`[][]\>\>

#### Defined in

[types/index.ts:1349](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L1349)

## Table of contents

### Methods

- [checkAuthorization](../wiki/types.ProcedureMethod#checkauthorization)

## Methods

### checkAuthorization

▸ **checkAuthorization**(`args`, `opts?`): `Promise`<[`ProcedureAuthorizationStatus`](../wiki/types.ProcedureAuthorizationStatus)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `args` | `MethodArgs` |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<[`ProcedureAuthorizationStatus`](../wiki/types.ProcedureAuthorizationStatus)\>

#### Defined in

[types/index.ts:1352](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L1352)
