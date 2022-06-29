# Class: NumberedPortfolio

[api/entities/NumberedPortfolio](../wiki/api.entities.NumberedPortfolio).NumberedPortfolio

Represents a numbered (non-default) Portfolio for an Identity

## Hierarchy

- [`Portfolio`](../wiki/api.entities.Portfolio.Portfolio)

  ↳ **`NumberedPortfolio`**

## Table of contents

### Properties

- [id](../wiki/api.entities.NumberedPortfolio.NumberedPortfolio#id)
- [owner](../wiki/api.entities.NumberedPortfolio.NumberedPortfolio#owner)
- [uuid](../wiki/api.entities.NumberedPortfolio.NumberedPortfolio#uuid)

### Methods

- [createdAt](../wiki/api.entities.NumberedPortfolio.NumberedPortfolio#createdat)
- [exists](../wiki/api.entities.NumberedPortfolio.NumberedPortfolio#exists)
- [getAssetBalances](../wiki/api.entities.NumberedPortfolio.NumberedPortfolio#getassetbalances)
- [getCustodian](../wiki/api.entities.NumberedPortfolio.NumberedPortfolio#getcustodian)
- [getName](../wiki/api.entities.NumberedPortfolio.NumberedPortfolio#getname)
- [getTransactionHistory](../wiki/api.entities.NumberedPortfolio.NumberedPortfolio#gettransactionhistory)
- [isCustodiedBy](../wiki/api.entities.NumberedPortfolio.NumberedPortfolio#iscustodiedby)
- [isEqual](../wiki/api.entities.NumberedPortfolio.NumberedPortfolio#isequal)
- [isOwnedBy](../wiki/api.entities.NumberedPortfolio.NumberedPortfolio#isownedby)
- [modifyName](../wiki/api.entities.NumberedPortfolio.NumberedPortfolio#modifyname)
- [moveFunds](../wiki/api.entities.NumberedPortfolio.NumberedPortfolio#movefunds)
- [quitCustody](../wiki/api.entities.NumberedPortfolio.NumberedPortfolio#quitcustody)
- [setCustodian](../wiki/api.entities.NumberedPortfolio.NumberedPortfolio#setcustodian)
- [toHuman](../wiki/api.entities.NumberedPortfolio.NumberedPortfolio#tohuman)
- [generateUuid](../wiki/api.entities.NumberedPortfolio.NumberedPortfolio#generateuuid)
- [unserialize](../wiki/api.entities.NumberedPortfolio.NumberedPortfolio#unserialize)

## Properties

### id

• **id**: `BigNumber`

Portfolio identifier number

#### Defined in

[api/entities/NumberedPortfolio.ts:46](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/NumberedPortfolio.ts#L46)

___

### owner

• **owner**: [`Identity`](../wiki/api.entities.Identity.Identity)

Identity of the Portfolio's owner

#### Inherited from

[Portfolio](../wiki/api.entities.Portfolio.Portfolio).[owner](../wiki/api.entities.Portfolio.Portfolio#owner)

#### Defined in

[api/entities/Portfolio/index.ts:75](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Portfolio/index.ts#L75)

___

### uuid

• **uuid**: `string`

#### Inherited from

[Portfolio](../wiki/api.entities.Portfolio.Portfolio).[uuid](../wiki/api.entities.Portfolio.Portfolio#uuid)

#### Defined in

[api/entities/Entity.ts:46](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Entity.ts#L46)

## Methods

### createdAt

▸ **createdAt**(): `Promise`<``null`` \| [`EventIdentifier`](../wiki/types.EventIdentifier)\>

Retrieve the identifier data (block number, date and event index) of the event that was emitted when this Portfolio was created

**`note`** uses the middleware

**`note`** there is a possibility that the data is not ready by the time it is requested. In that case, `null` is returned

#### Returns

`Promise`<``null`` \| [`EventIdentifier`](../wiki/types.EventIdentifier)\>

#### Defined in

[api/entities/NumberedPortfolio.ts:112](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/NumberedPortfolio.ts#L112)

___

### exists

▸ **exists**(): `Promise`<`boolean`\>

Return whether this Portfolio exists

#### Returns

`Promise`<`boolean`\>

#### Overrides

[Portfolio](../wiki/api.entities.Portfolio.Portfolio).[exists](../wiki/api.entities.Portfolio.Portfolio#exists)

#### Defined in

[api/entities/NumberedPortfolio.ts:136](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/NumberedPortfolio.ts#L136)

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

#### Inherited from

[Portfolio](../wiki/api.entities.Portfolio.Portfolio).[getAssetBalances](../wiki/api.entities.Portfolio.Portfolio#getassetbalances)

#### Defined in

[api/entities/Portfolio/index.ts:141](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Portfolio/index.ts#L141)

___

### getCustodian

▸ **getCustodian**(): `Promise`<[`Identity`](../wiki/api.entities.Identity.Identity)\>

Retrieve the custodian Identity of this Portfolio

**`note`** if no custodian is set, the owner Identity is returned

#### Returns

`Promise`<[`Identity`](../wiki/api.entities.Identity.Identity)\>

#### Inherited from

[Portfolio](../wiki/api.entities.Portfolio.Portfolio).[getCustodian](../wiki/api.entities.Portfolio.Portfolio#getcustodian)

#### Defined in

[api/entities/Portfolio/index.ts:271](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Portfolio/index.ts#L271)

___

### getName

▸ **getName**(): `Promise`<`string`\>

Return the Portfolio name

#### Returns

`Promise`<`string`\>

#### Defined in

[api/entities/NumberedPortfolio.ts:80](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/NumberedPortfolio.ts#L80)

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

#### Inherited from

[Portfolio](../wiki/api.entities.Portfolio.Portfolio).[getTransactionHistory](../wiki/api.entities.Portfolio.Portfolio#gettransactionhistory)

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

#### Inherited from

[Portfolio](../wiki/api.entities.Portfolio.Portfolio).[isCustodiedBy](../wiki/api.entities.Portfolio.Portfolio#iscustodiedby)

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

[Portfolio](../wiki/api.entities.Portfolio.Portfolio).[isEqual](../wiki/api.entities.Portfolio.Portfolio#isequal)

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

#### Inherited from

[Portfolio](../wiki/api.entities.Portfolio.Portfolio).[isOwnedBy](../wiki/api.entities.Portfolio.Portfolio#isownedby)

#### Defined in

[api/entities/Portfolio/index.ts:112](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Portfolio/index.ts#L112)

___

### modifyName

▸ **modifyName**(`args`, `opts?`): `Promise`<`TransactionQueue`<[`NumberedPortfolio`](../wiki/api.entities.NumberedPortfolio.NumberedPortfolio), [`NumberedPortfolio`](../wiki/api.entities.NumberedPortfolio.NumberedPortfolio), `unknown`[][]\>\>

Rename portfolio

**`note`** required role:
  - Portfolio Custodian

**`note`** this method is of type [ProcedureMethod](../wiki/types.ProcedureMethod), which means you can call [modifyName.checkAuthorization](../wiki/types.ProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `args` | [`RenamePortfolioParams`](../wiki/api.procedures.renamePortfolio.RenamePortfolioParams) |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<[`NumberedPortfolio`](../wiki/api.entities.NumberedPortfolio.NumberedPortfolio), [`NumberedPortfolio`](../wiki/api.entities.NumberedPortfolio.NumberedPortfolio), `unknown`[][]\>\>

#### Defined in

[api/entities/NumberedPortfolio.ts:73](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/NumberedPortfolio.ts#L73)

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

#### Inherited from

[Portfolio](../wiki/api.entities.Portfolio.Portfolio).[moveFunds](../wiki/api.entities.Portfolio.Portfolio#movefunds)

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

#### Inherited from

[Portfolio](../wiki/api.entities.Portfolio.Portfolio).[quitCustody](../wiki/api.entities.Portfolio.Portfolio#quitcustody)

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

#### Inherited from

[Portfolio](../wiki/api.entities.Portfolio.Portfolio).[setCustodian](../wiki/api.entities.Portfolio.Portfolio#setcustodian)

#### Defined in

[api/entities/Portfolio/index.ts:236](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Portfolio/index.ts#L236)

___

### toHuman

▸ **toHuman**(): `HumanReadable`

Return the Portfolio ID and owner DID

#### Returns

`HumanReadable`

#### Inherited from

[Portfolio](../wiki/api.entities.Portfolio.Portfolio).[toHuman](../wiki/api.entities.Portfolio.Portfolio#tohuman)

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

[Portfolio](../wiki/api.entities.Portfolio.Portfolio).[generateUuid](../wiki/api.entities.Portfolio.Portfolio#generateuuid)

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

[Portfolio](../wiki/api.entities.Portfolio.Portfolio).[unserialize](../wiki/api.entities.Portfolio.Portfolio#unserialize)

#### Defined in

[api/entities/Entity.ts:23](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Entity.ts#L23)
