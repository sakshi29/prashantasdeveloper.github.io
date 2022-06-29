# Class: CorporateActions

[api/entities/Asset/CorporateActions](../wiki/api.entities.Asset.CorporateActions).CorporateActions

Handles all Asset Corporate Actions related functionality

## Hierarchy

- `Namespace`<[`Asset`](../wiki/api.entities.Asset.Asset)\>

  ↳ **`CorporateActions`**

## Table of contents

### Properties

- [distributions](../wiki/api.entities.Asset.CorporateActions.CorporateActions#distributions)

### Methods

- [getAgents](../wiki/api.entities.Asset.CorporateActions.CorporateActions#getagents)
- [getDefaultConfig](../wiki/api.entities.Asset.CorporateActions.CorporateActions#getdefaultconfig)
- [remove](../wiki/api.entities.Asset.CorporateActions.CorporateActions#remove)
- [removeAgent](../wiki/api.entities.Asset.CorporateActions.CorporateActions#removeagent)
- [setAgent](../wiki/api.entities.Asset.CorporateActions.CorporateActions#setagent)
- [setDefaultConfig](../wiki/api.entities.Asset.CorporateActions.CorporateActions#setdefaultconfig)

## Properties

### distributions

• **distributions**: [`Distributions`](../wiki/api.entities.Asset.CorporateActions.Distributions.Distributions)

#### Defined in

[api/entities/Asset/CorporateActions/index.ts:35](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Asset/CorporateActions/index.ts#L35)

## Methods

### getAgents

▸ **getAgents**(): `Promise`<[`Identity`](../wiki/api.entities.Identity.Identity)[]\>

Retrieve a list of agent Identities

#### Returns

`Promise`<[`Identity`](../wiki/api.entities.Identity.Identity)[]\>

#### Defined in

[api/entities/Asset/CorporateActions/index.ts:125](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Asset/CorporateActions/index.ts#L125)

___

### getDefaultConfig

▸ **getDefaultConfig**(): `Promise`<[`CorporateActionDefaultConfig`](../wiki/api.entities.Asset.CorporateActions.types.CorporateActionDefaultConfig)\>

Retrieve default config comprising of targets, global tax withholding percentage and per-Identity tax withholding percentages.

**`note`** This config is applied to every Corporate Action that is created until they are modified. Modifying the default config
  does not impact existing Corporate Actions.
  When creating a Corporate Action, values passed explicitly will override this default config

#### Returns

`Promise`<[`CorporateActionDefaultConfig`](../wiki/api.entities.Asset.CorporateActions.types.CorporateActionDefaultConfig)\>

#### Defined in

[api/entities/Asset/CorporateActions/index.ts:160](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Asset/CorporateActions/index.ts#L160)

___

### remove

▸ **remove**(`args`, `opts?`): `Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

Remove a Corporate Action

**`note`** this method is of type [ProcedureMethod](../wiki/types.ProcedureMethod), which means you can call [remove.checkAuthorization](../wiki/types.ProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `args` | [`RemoveCorporateActionParams`](../wiki/api.procedures.removeCorporateAction.RemoveCorporateActionParams) |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

#### Defined in

[api/entities/Asset/CorporateActions/index.ts:118](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Asset/CorporateActions/index.ts#L118)

___

### removeAgent

▸ **removeAgent**(`opts?`): `Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

Remove the Corporate Actions Agent of the Asset

**`note`** this action will leave the Asset owner as the Corporate Actions Agent

**`deprecated`**

**`note`** this method is of type [NoArgsProcedureMethod](../wiki/types.NoArgsProcedureMethod), which means you can call [removeAgent.checkAuthorization](../wiki/types.NoArgsProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

#### Defined in

[api/entities/Asset/CorporateActions/index.ts:108](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Asset/CorporateActions/index.ts#L108)

___

### setAgent

▸ **setAgent**(`args`, `opts?`): `Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

Assign a new Corporate Actions Agent for the Asset

**`note`** this may create [Authorization Requests](../wiki/api.entities.AuthorizationRequest.AuthorizationRequest) which have to be accepted by the `target` Identity.
  An [Account](../wiki/api.entities.Account.Account) or [Identity](../wiki/api.entities.Identity.Identity) can fetch its pending Authorization Requests by calling [authorizations.getReceived](../wiki/api.entities.common.namespaces.Authorizations.Authorizations#getreceived).
  Also, an Account or Identity can directly fetch the details of an Authorization Request by calling [authorizations.getOne](../wiki/api.entities.common.namespaces.Authorizations.Authorizations#getone)

**`deprecated`** in favor of `inviteAgent`

**`note`** this method is of type [ProcedureMethod](../wiki/types.ProcedureMethod), which means you can call [setAgent.checkAuthorization](../wiki/types.ProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `args` | [`ModifyCorporateActionsAgentParams`](../wiki/api.procedures.modifyCorporateActionsAgent.ModifyCorporateActionsAgentParams) |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

#### Defined in

[api/entities/Asset/CorporateActions/index.ts:94](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Asset/CorporateActions/index.ts#L94)

___

### setDefaultConfig

▸ **setDefaultConfig**(`args`, `opts?`): `Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

Assign default config values(targets, global tax withholding percentage and per-Identity tax withholding percentages)

**`note`** These config values are applied to every Corporate Action that is created until they are modified. Modifying these values
  does not impact existing Corporate Actions.
  When creating a Corporate Action, values passed explicitly will override these default config values

**`note`** this method is of type [ProcedureMethod](../wiki/types.ProcedureMethod), which means you can call [setDefaultConfig.checkAuthorization](../wiki/types.ProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `args` | [`ModifyCaDefaultConfigParams`](../wiki/api.procedures.modifyCaDefaultConfig#modifycadefaultconfigparams) |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

#### Defined in

[api/entities/Asset/CorporateActions/index.ts:78](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Asset/CorporateActions/index.ts#L78)
