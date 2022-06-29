[@polymeshassociation/polymesh-sdk](../README.md) / [Modules](../modules.md) / [api/entities/AuthorizationRequest](../modules/api_entities_AuthorizationRequest.md) / AuthorizationRequest

# Class: AuthorizationRequest

[api/entities/AuthorizationRequest](../modules/api_entities_AuthorizationRequest.md).AuthorizationRequest

Represents a request made by an Identity to another Identity (or Account) for some sort of authorization. This has multiple uses. For example, if Alice
  wants to transfer ownership of one of her Assets to Bob, this method emits an authorization request for Bob,
  who then has to accept it in order to complete the ownership transfer

## Hierarchy

- [`Entity`](api_entities_Entity.Entity.md)<[`UniqueIdentifiers`](../interfaces/api_entities_AuthorizationRequest.UniqueIdentifiers.md), `HumanReadable`\>

  ↳ **`AuthorizationRequest`**

## Table of contents

### Properties

- [authId](api_entities_AuthorizationRequest.AuthorizationRequest.md#authid)
- [data](api_entities_AuthorizationRequest.AuthorizationRequest.md#data)
- [expiry](api_entities_AuthorizationRequest.AuthorizationRequest.md#expiry)
- [issuer](api_entities_AuthorizationRequest.AuthorizationRequest.md#issuer)
- [target](api_entities_AuthorizationRequest.AuthorizationRequest.md#target)
- [uuid](api_entities_AuthorizationRequest.AuthorizationRequest.md#uuid)

### Methods

- [accept](api_entities_AuthorizationRequest.AuthorizationRequest.md#accept)
- [exists](api_entities_AuthorizationRequest.AuthorizationRequest.md#exists)
- [isEqual](api_entities_AuthorizationRequest.AuthorizationRequest.md#isequal)
- [isExpired](api_entities_AuthorizationRequest.AuthorizationRequest.md#isexpired)
- [remove](api_entities_AuthorizationRequest.AuthorizationRequest.md#remove)
- [toHuman](api_entities_AuthorizationRequest.AuthorizationRequest.md#tohuman)
- [generateUuid](api_entities_AuthorizationRequest.AuthorizationRequest.md#generateuuid)
- [unserialize](api_entities_AuthorizationRequest.AuthorizationRequest.md#unserialize)

## Properties

### authId

• **authId**: `BigNumber`

internal identifier for the Request (used to accept/reject/cancel)

#### Defined in

[api/entities/AuthorizationRequest.ts:99](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/AuthorizationRequest.ts#L99)

___

### data

• **data**: [`Authorization`](../modules/types.md#authorization)

Authorization Request data corresponding to type of Authorization

| Type                            | Data                            |
|---------------------------------|---------------------------------|
| Add Relayer Paying Key          | Beneficiary, Relayer, Allowance |
| Become Agent                    | Permission Group                |
| Attest Primary Key Rotation     | DID                             |
| Rotate Primary Key              | N/A                             |
| Rotate Primary Key to Secondary | Permissions                     |
| Transfer Ticker                 | Ticker                          |
| Add MultiSig Signer             | Account                         |
| Transfer Asset Ownership        | Ticker                          |
| Join Identity                   | Permissions                     |
| Portfolio Custody               | Portfolio                       |

#### Defined in

[api/entities/AuthorizationRequest.ts:88](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/AuthorizationRequest.ts#L88)

___

### expiry

• **expiry**: ``null`` \| `Date`

date at which the Authorization Request expires and can no longer be accepted.
  At this point, a new Authorization Request must be emitted. Null if the Request never expires

#### Defined in

[api/entities/AuthorizationRequest.ts:94](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/AuthorizationRequest.ts#L94)

___

### issuer

• **issuer**: [`Identity`](api_entities_Identity.Identity.md)

Identity that emitted the request

#### Defined in

[api/entities/AuthorizationRequest.ts:70](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/AuthorizationRequest.ts#L70)

___

### target

• **target**: [`Signer`](../modules/types.md#signer)

Identity or Account to which the request was emitted

#### Defined in

[api/entities/AuthorizationRequest.ts:65](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/AuthorizationRequest.ts#L65)

___

### uuid

• **uuid**: `string`

#### Inherited from

[Entity](api_entities_Entity.Entity.md).[uuid](api_entities_Entity.Entity.md#uuid)

#### Defined in

[api/entities/Entity.ts:46](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Entity.ts#L46)

## Methods

### accept

▸ **accept**(`opts?`): `Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

Accept the Authorization Request. You must be the target of the Request to be able to accept it

**`note`** this method is of type [NoArgsProcedureMethod](../interfaces/types.NoArgsProcedureMethod.md), which means you can call [accept.checkAuthorization](../interfaces/types.NoArgsProcedureMethod.md#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `opts?` | [`ProcedureOpts`](../interfaces/types.ProcedureOpts.md) |

#### Returns

`Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

#### Defined in

[api/entities/AuthorizationRequest.ts:183](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/AuthorizationRequest.ts#L183)

___

### exists

▸ **exists**(): `Promise`<`boolean`\>

Determine whether this Authorization Request exists on chain

#### Returns

`Promise`<`boolean`\>

#### Overrides

[Entity](api_entities_Entity.Entity.md).[exists](api_entities_Entity.Entity.md#exists)

#### Defined in

[api/entities/AuthorizationRequest.ts:212](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/AuthorizationRequest.ts#L212)

___

### isEqual

▸ **isEqual**(`entity`): `boolean`

Determine whether this Entity is the same as another one

#### Parameters

| Name | Type |
| :------ | :------ |
| `entity` | [`Entity`](api_entities_Entity.Entity.md)<`unknown`, `unknown`\> |

#### Returns

`boolean`

#### Inherited from

[Entity](api_entities_Entity.Entity.md).[isEqual](api_entities_Entity.Entity.md#isequal)

#### Defined in

[api/entities/Entity.ts:61](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Entity.ts#L61)

___

### isExpired

▸ **isExpired**(): `boolean`

Returns whether the Authorization Request has expired

#### Returns

`boolean`

#### Defined in

[api/entities/AuthorizationRequest.ts:203](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/AuthorizationRequest.ts#L203)

___

### remove

▸ **remove**(`opts?`): `Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

Remove the Authorization Request

- If you are the Request issuer, this will cancel the Authorization
- If you are the Request target, this will reject the Authorization

**`note`** this method is of type [NoArgsProcedureMethod](../interfaces/types.NoArgsProcedureMethod.md), which means you can call [remove.checkAuthorization](../interfaces/types.NoArgsProcedureMethod.md#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `opts?` | [`ProcedureOpts`](../interfaces/types.ProcedureOpts.md) |

#### Returns

`Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

#### Defined in

[api/entities/AuthorizationRequest.ts:196](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/AuthorizationRequest.ts#L196)

___

### toHuman

▸ **toHuman**(): `HumanReadable`

Return the Authorization's static data

#### Returns

`HumanReadable`

#### Overrides

[Entity](api_entities_Entity.Entity.md).[toHuman](api_entities_Entity.Entity.md#tohuman)

#### Defined in

[api/entities/AuthorizationRequest.ts:226](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/AuthorizationRequest.ts#L226)

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

[Entity](api_entities_Entity.Entity.md).[generateUuid](api_entities_Entity.Entity.md#generateuuid)

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

[Entity](api_entities_Entity.Entity.md).[unserialize](api_entities_Entity.Entity.md#unserialize)

#### Defined in

[api/entities/Entity.ts:23](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Entity.ts#L23)
