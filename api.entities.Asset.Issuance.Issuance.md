# Class: Issuance

[api/entities/Asset/Issuance](../wiki/api.entities.Asset.Issuance).Issuance

Handles all Asset Issuance related functionality

## Hierarchy

- `Namespace`<[`Asset`](../wiki/api.entities.Asset.Asset)\>

  ↳ **`Issuance`**

## Table of contents

### Methods

- [issue](../wiki/api.entities.Asset.Issuance.Issuance#issue)

## Methods

### issue

▸ **issue**(`args`, `opts?`): `Promise`<`TransactionQueue`<[`Asset`](../wiki/api.entities.Asset.Asset), [`Asset`](../wiki/api.entities.Asset.Asset), `unknown`[][]\>\>

Issue a certain amount of Asset tokens to the caller's default portfolio

**`note`** this method is of type [ProcedureMethod](../wiki/types.ProcedureMethod), which means you can call [issue.checkAuthorization](../wiki/types.ProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `args` | `Object` | - |
| `args.amount` | `BigNumber` | amount of Asset tokens to be issued |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) | - |

#### Returns

`Promise`<`TransactionQueue`<[`Asset`](../wiki/api.entities.Asset.Asset), [`Asset`](../wiki/api.entities.Asset.Asset), `unknown`[][]\>\>

#### Defined in

[api/entities/Asset/Issuance.ts:35](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Asset/Issuance.ts#L35)
