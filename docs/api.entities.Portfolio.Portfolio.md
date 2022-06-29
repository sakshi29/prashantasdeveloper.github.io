# Class: Portfolio

[api/entities/Portfolio](../wiki/api.entities.Portfolio).Portfolio

Represents a base Portfolio for a specific Identity in the Polymesh blockchain

## Hierarchy

- [`Entity`](../wiki/api.entities.Entity.Entity)<[`UniqueIdentifiers`](../wiki/api.entities.Portfolio.UniqueIdentifiers), `HumanReadable`\>

  ↳ **`Portfolio`**

  ↳↳ [`DefaultPortfolio`](../wiki/api.entities.DefaultPortfolio.DefaultPortfolio)

  ↳↳ [`NumberedPortfolio`](../wiki/api.entities.NumberedPortfolio.NumberedPortfolio)

## Table of contents

### Properties

- [owner](../wiki/api.entities.Portfolio.Portfolio#owner)
- [uuid](../wiki/api.entities.Portfolio.Portfolio#uuid)

### Methods

- [exists](../wiki/api.entities.Portfolio.Portfolio#exists)
- [getAssetBalances](../wiki/api.entities.Portfolio.Portfolio#getassetbalances)
- [getCustodian](../wiki/api.entities.Portfolio.Portfolio#getcustodian)
- [getTransactionHistory](../wiki/api.entities.Portfolio.Portfolio#gettransactionhistory)
- [isCustodiedBy](../wiki/api.entities.Portfolio.Portfolio#iscustodiedby)
- [isEqual](../wiki/api.entities.Portfolio.Portfolio#isequal)
- [isOwnedBy](../wiki/api.entities.Portfolio.Portfolio#isownedby)
- [moveFunds](../wiki/api.entities.Portfolio.Portfolio#movefunds)
- [quitCustody](../wiki/api.entities.Portfolio.Portfolio#quitcustody)
- [setCustodian](../wiki/api.entities.Portfolio.Portfolio#setcustodian)
- [toHuman](../wiki/api.entities.Portfolio.Portfolio#tohuman)
- [generateUuid](../wiki/api.entities.Portfolio.Portfolio#generateuuid)
- [unserialize](../wiki/api.entities.Portfolio.Portfolio#unserialize)

## Properties

### owner

• **owner**: [`Identity`](../wiki/api.entities.Identity.Identity)

Identity of the Portfolio's owner

#### Defined in

[api/entities/Portfolio/index.ts:75](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Portfolio/index.ts#L75)

___

### uuid

• **uuid**: `string`

#### Inherited from

[Entity](../wiki/api.entities.Entity.Entity).[uuid](../wiki/api.entities.Entity.Entity#uuid)

#### Defined in

[api/entities/Entity.ts:46](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Entity.ts#L46)

## Methods

### exists

▸ `Abstract` **exists**(): `Promise`<`boolean`\>

Determine whether this Entity exists on chain

#### Returns

`Promise`<`boolean`\>

#### Inherited from

[Entity](../wiki/api.entities.Entity.Entity).[exists](../wiki/api.entities.Entity.Entity#exists)

#### Defined in

[api/entities/Entity.ts:68](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Entity.ts#L68)

___

### getAssetBalances

▸ **getAssetBalances**(`args?`): `Promise`<[`PortfolioBalance`](../wiki/api.entities.Portfolio.types.PortfolioBalance)[]\>

Retrieve the balances of all Assets in this Portfolio

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `args?` | `Object` | - |
| `args.assets` | (`string` \| [`Asset`](../wiki/api.entities.Asset.Asset))[] | array of Assets (or tickers) for which to fetch balances (optional, all balances are retrieved if not passed) |

#### Returns

`Promise`<[`PortfolioBalance`](../wiki/api.entities.Portfolio.types.PortfolioBalance)[]\>

#### Defined in

[api/entities/Portfolio/index.ts:141](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Portfolio/index.ts#L141)

___

### getCustodian

▸ **getCustodian**(): `Promise`<[`Identity`](../wiki/api.entities.Identity.Identity)\>

Retrieve the custodian Identity of this Portfolio

**`note`** if no custodian is set, the owner Identity is returned

#### Returns

`Promise`<[`Identity`](../wiki/api.entities.Identity.Identity)\>

#### Defined in

[api/entities/Portfolio/index.ts:271](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Portfolio/index.ts#L271)

___

### getTransactionHistory

▸ **getTransactionHistory**(`filters?`): `Promise`<[`ResultSet`](../wiki/types.ResultSet)<[`HistoricSettlement`](../wiki/api.entities.Portfolio.types.HistoricSettlement)\>\>

Retrieve a list of transactions where this portfolio was involved. Can be filtered using parameters

**`note`** supports pagination

**`note`** uses the middleware

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `filters` | `Object` | - |
| `filters.account?` | `string` | Account involved in the settlement |
| `filters.size?` | `BigNumber` | page size |
| `filters.start?` | `BigNumber` | page offset |
| `filters.ticker?` | `string` | ticker involved in the transaction |

#### Returns

`Promise`<[`ResultSet`](../wiki/types.ResultSet)<[`HistoricSettlement`](../wiki/api.entities.Portfolio.types.HistoricSettlement)\>\>

#### Defined in

[api/entities/Portfolio/index.ts:316](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Portfolio/index.ts#L316)

___

### isCustodiedBy

▸ **isCustodiedBy**(`args?`): `Promise`<`boolean`\>

Return whether an Identity is the Portfolio custodian

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `args?` | `Object` | - |
| `args.identity` | `string` \| [`Identity`](../wiki/api.entities.Identity.Identity) | optional, defaults to the signing Identity |

#### Returns

`Promise`<`boolean`\>

#### Defined in

[api/entities/Portfolio/index.ts:125](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Portfolio/index.ts#L125)

___

### isEqual

▸ **isEqual**(`entity`): `boolean`

Determine whether this Entity is the same as another one

#### Parameters

| Name | Type |
| :------ | :------ |
| `entity` | [`Entity`](../wiki/api.entities.Entity.Entity)<`unknown`, `unknown`\> |

#### Returns

`boolean`

#### Inherited from

[Entity](../wiki/api.entities.Entity.Entity).[isEqual](../wiki/api.entities.Entity.Entity#isequal)

#### Defined in

[api/entities/Entity.ts:61](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Entity.ts#L61)

___

### isOwnedBy

▸ **isOwnedBy**(`args?`): `Promise`<`boolean`\>

Return whether an Identity is the Portfolio owner

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `args?` | `Object` | - |
| `args.identity` | `string` \| [`Identity`](../wiki/api.entities.Identity.Identity) | defaults to the signing Identity |

#### Returns

`Promise`<`boolean`\>

#### Defined in

[api/entities/Portfolio/index.ts:112](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Portfolio/index.ts#L112)

___

### moveFunds

▸ **moveFunds**(`args`, `opts?`): `Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

Moves funds from this Portfolio to another one owned by the same Identity

**`note`** required role:
  - Portfolio Custodian

**`note`** this method is of type [ProcedureMethod](../wiki/types.ProcedureMethod), which means you can call [moveFunds.checkAuthorization](../wiki/types.ProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `args` | [`MoveFundsParams`](../wiki/api.procedures.moveFunds.MoveFundsParams) |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

#### Defined in

[api/entities/Portfolio/index.ts:249](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Portfolio/index.ts#L249)

___

### quitCustody

▸ **quitCustody**(`opts?`): `Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

Returns the custody of the portfolio to the portfolio owner unilaterally

**`note`** required role:
  - Portfolio Custodian

**`note`** this method is of type [NoArgsProcedureMethod](../wiki/types.NoArgsProcedureMethod), which means you can call [quitCustody.checkAuthorization](../wiki/types.NoArgsProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

#### Defined in

[api/entities/Portfolio/index.ts:262](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Portfolio/index.ts#L262)

___

### setCustodian

▸ **setCustodian**(`args`, `opts?`): `Promise`<`TransactionQueue`<[`AuthorizationRequest`](../wiki/api.entities.AuthorizationRequest.AuthorizationRequest), [`AuthorizationRequest`](../wiki/api.entities.AuthorizationRequest.AuthorizationRequest), `unknown`[][]\>\>

Send an invitation to an Identity to assign it as custodian for this Portfolio

**`note`** this will create an [Authorization Request](../wiki/api.entities.AuthorizationRequest.AuthorizationRequest) which has to be accepted by the `targetIdentity`.
  An [Account](../wiki/api.entities.Account.Account) or [Identity](../wiki/api.entities.Identity.Identity) can fetch its pending Authorization Requests by calling [authorizations.getReceived](../wiki/api.entities.common.namespaces.Authorizations.Authorizations#getreceived).
  Also, an Account or Identity can directly fetch the details of an Authorization Request by calling [authorizations.getOne](../wiki/api.entities.common.namespaces.Authorizations.Authorizations#getone)

**`note`** required role:
  - Portfolio Custodian

**`note`** this method is of type [ProcedureMethod](../wiki/types.ProcedureMethod), which means you can call [setCustodian.checkAuthorization](../wiki/types.ProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `args` | [`SetCustodianParams`](../wiki/api.procedures.setCustodian.SetCustodianParams) |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<[`AuthorizationRequest`](../wiki/api.entities.AuthorizationRequest.AuthorizationRequest), [`AuthorizationRequest`](../wiki/api.entities.AuthorizationRequest.AuthorizationRequest), `unknown`[][]\>\>

#### Defined in

[api/entities/Portfolio/index.ts:236](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Portfolio/index.ts#L236)

___

### toHuman

▸ **toHuman**(): `HumanReadable`

Return the Portfolio ID and owner DID

#### Returns

`HumanReadable`

#### Overrides

[Entity](../wiki/api.entities.Entity.Entity).[toHuman](../wiki/api.entities.Entity.Entity#tohuman)

#### Defined in

[api/entities/Portfolio/index.ts:413](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Portfolio/index.ts#L413)

___

### generateUuid

▸ `Static` **generateUuid**<`Identifiers`\>(`identifiers`): `string`

Generate the Entity's UUID from its identifying properties

#### Type parameters

| Name |
| :------ |
| `Identifiers` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `identifiers` | `Identifiers` |

#### Returns

`string`

#### Inherited from

[Entity](../wiki/api.entities.Entity.Entity).[generateUuid](../wiki/api.entities.Entity.Entity#generateuuid)

#### Defined in

[api/entities/Entity.ts:14](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Entity.ts#L14)

___

### unserialize

▸ `Static` **unserialize**<`Identifiers`\>(`serialized`): `Identifiers`

Unserialize a UUID into its Unique Identifiers

#### Type parameters

| Name |
| :------ |
| `Identifiers` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `serialized` | `string` | UUID to unserialize |

#### Returns

`Identifiers`

#### Inherited from

[Entity](../wiki/api.entities.Entity.Entity).[unserialize](../wiki/api.entities.Entity.Entity#unserialize)

#### Defined in

[api/entities/Entity.ts:23](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Entity.ts#L23)
