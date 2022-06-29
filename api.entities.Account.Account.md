# Class: Account

[api/entities/Account](../wiki/api.entities.Account).Account

Represents an Account in the Polymesh blockchain. Accounts can hold POLYX, control Identities and vote on proposals (among other things)

## Hierarchy

- [`Entity`](../wiki/api.entities.Entity.Entity)<[`UniqueIdentifiers`](../wiki/api.entities.Account.UniqueIdentifiers), `string`\>

  ↳ **`Account`**

## Table of contents

### Properties

- [address](../wiki/api.entities.Account.Account#address)
- [authorizations](../wiki/api.entities.Account.Account#authorizations)
- [key](../wiki/api.entities.Account.Account#key)
- [uuid](../wiki/api.entities.Account.Account#uuid)

### Methods

- [checkPermissions](../wiki/api.entities.Account.Account#checkpermissions)
- [exists](../wiki/api.entities.Account.Account#exists)
- [getBalance](../wiki/api.entities.Account.Account#getbalance)
- [getIdentity](../wiki/api.entities.Account.Account#getidentity)
- [getPermissions](../wiki/api.entities.Account.Account#getpermissions)
- [getSubsidy](../wiki/api.entities.Account.Account#getsubsidy)
- [getTransactionHistory](../wiki/api.entities.Account.Account#gettransactionhistory)
- [hasPermissions](../wiki/api.entities.Account.Account#haspermissions)
- [isEqual](../wiki/api.entities.Account.Account#isequal)
- [isFrozen](../wiki/api.entities.Account.Account#isfrozen)
- [toHuman](../wiki/api.entities.Account.Account#tohuman)
- [generateUuid](../wiki/api.entities.Account.Account#generateuuid)
- [unserialize](../wiki/api.entities.Account.Account#unserialize)

## Properties

### address

• **address**: `string`

Polymesh-specific address of the Account. Serves as an identifier

#### Defined in

[api/entities/Account.ts:251](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Account.ts#L251)

___

### authorizations

• **authorizations**: [`Authorizations`](../wiki/api.entities.common.namespaces.Authorizations.Authorizations)<[`Account`](../wiki/api.entities.Account.Account)\>

#### Defined in

[api/entities/Account.ts:260](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Account.ts#L260)

___

### key

• **key**: `string`

A hex representation of the cryptographic public key of the Account. This is consistent across
Substrate chains, while the address depends on the chain as well.

#### Defined in

[api/entities/Account.ts:257](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Account.ts#L257)

___

### uuid

• **uuid**: `string`

#### Inherited from

[Entity](../wiki/api.entities.Entity.Entity).[uuid](../wiki/api.entities.Entity.Entity#uuid)

#### Defined in

[api/entities/Entity.ts:46](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Entity.ts#L46)

## Methods

### checkPermissions

▸ **checkPermissions**(`permissions`): `Promise`<[`CheckPermissionsResult`](../wiki/types.CheckPermissionsResult)<[`Account`](../wiki/types.SignerType#account)\>\>

Check if this Account possesses certain Permissions to act on behalf of its corresponding Identity

#### Parameters

| Name | Type |
| :------ | :------ |
| `permissions` | [`SimplePermissions`](../wiki/types.SimplePermissions) |

#### Returns

`Promise`<[`CheckPermissionsResult`](../wiki/types.CheckPermissionsResult)<[`Account`](../wiki/types.SignerType#account)\>\>

which permissions the Account is missing (if any) and the final result

#### Defined in

[api/entities/Account.ts:531](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Account.ts#L531)

___

### exists

▸ **exists**(): `Promise`<`boolean`\>

Determine whether this Account exists on chain

#### Returns

`Promise`<`boolean`\>

#### Overrides

[Entity](../wiki/api.entities.Entity.Entity).[exists](../wiki/api.entities.Entity.Entity#exists)

#### Defined in

[api/entities/Account.ts:597](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Account.ts#L597)

___

### getBalance

▸ **getBalance**(): `Promise`<[`Balance`](../wiki/types.Balance)\>

Get the free/locked POLYX balance of the Account

**`note`** can be subscribed to

#### Returns

`Promise`<[`Balance`](../wiki/types.Balance)\>

#### Defined in

[api/entities/Account.ts:282](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Account.ts#L282)

▸ **getBalance**(`callback`): `Promise`<[`UnsubCallback`](../wiki/types#unsubcallback)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `callback` | [`SubCallback`](../wiki/types#subcallback)<[`Balance`](../wiki/types.Balance)\> |

#### Returns

`Promise`<[`UnsubCallback`](../wiki/types#unsubcallback)\>

#### Defined in

[api/entities/Account.ts:283](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Account.ts#L283)

___

### getIdentity

▸ **getIdentity**(): `Promise`<``null`` \| [`Identity`](../wiki/api.entities.Identity.Identity)\>

Retrieve the Identity associated to this Account (null if there is none)

#### Returns

`Promise`<``null`` \| [`Identity`](../wiki/api.entities.Identity.Identity)\>

#### Defined in

[api/entities/Account.ts:323](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Account.ts#L323)

___

### getPermissions

▸ **getPermissions**(): `Promise`<[`Permissions`](../wiki/types.Permissions)\>

Retrieve the Permissions this Account has as a Permissioned Account for its corresponding Identity

**`throws`** if there is no Identity associated with the Account

#### Returns

`Promise`<[`Permissions`](../wiki/types.Permissions)\>

#### Defined in

[api/entities/Account.ts:490](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Account.ts#L490)

___

### getSubsidy

▸ **getSubsidy**(): `Promise`<``null`` \| [`SubsidyWithAllowance`](../wiki/api.entities.Subsidy.types.SubsidyWithAllowance)\>

Get the subsidized balance of this Account and the subsidizer Account. If
  this Account isn't being subsidized, return null

**`note`** can be subscribed to

#### Returns

`Promise`<``null`` \| [`SubsidyWithAllowance`](../wiki/api.entities.Subsidy.types.SubsidyWithAllowance)\>

#### Defined in

[api/entities/Account.ts:304](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Account.ts#L304)

▸ **getSubsidy**(`callback`): `Promise`<[`UnsubCallback`](../wiki/types#unsubcallback)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `callback` | [`SubCallback`](../wiki/types#subcallback)<``null`` \| [`SubsidyWithAllowance`](../wiki/api.entities.Subsidy.types.SubsidyWithAllowance)\> |

#### Returns

`Promise`<[`UnsubCallback`](../wiki/types#unsubcallback)\>

#### Defined in

[api/entities/Account.ts:305](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Account.ts#L305)

___

### getTransactionHistory

▸ **getTransactionHistory**(`filters?`): `Promise`<[`ResultSet`](../wiki/types.ResultSet)<[`ExtrinsicData`](../wiki/types.ExtrinsicData)\>\>

Retrieve a list of transactions signed by this Account. Can be filtered using parameters

**`note`** if both `blockNumber` and `blockHash` are passed, only `blockNumber` is taken into account

**`note`** uses the middleware

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `filters` | `Object` | - |
| `filters.blockHash?` | `string` | - |
| `filters.blockNumber?` | `BigNumber` | - |
| `filters.orderBy?` | `TransactionOrderByInput` | - |
| `filters.size?` | `BigNumber` | page size |
| `filters.start?` | `BigNumber` | page offset |
| `filters.success?` | `boolean` | whether the transaction was successful or not |
| `filters.tag?` | `TxTag` | tag associated with the transaction |

#### Returns

`Promise`<[`ResultSet`](../wiki/types.ResultSet)<[`ExtrinsicData`](../wiki/types.ExtrinsicData)\>\>

#### Defined in

[api/entities/Account.ts:368](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Account.ts#L368)

___

### hasPermissions

▸ **hasPermissions**(`permissions`): `Promise`<`boolean`\>

Check if this Account possesses certain Permissions to act on behalf of its corresponding Identity

**`deprecated`** in favor of `checkPermissions`

#### Parameters

| Name | Type |
| :------ | :------ |
| `permissions` | [`SimplePermissions`](../wiki/types.SimplePermissions) |

#### Returns

`Promise`<`boolean`\>

#### Defined in

[api/entities/Account.ts:588](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Account.ts#L588)

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

### isFrozen

▸ **isFrozen**(): `Promise`<`boolean`\>

Check whether this Account is frozen. If frozen, it cannot perform any Identity related action until the primary Account of the Identity unfreezes all secondary Accounts

**`note`** returns false if the Account isn't associated to any Identity

#### Returns

`Promise`<`boolean`\>

#### Defined in

[api/entities/Account.ts:469](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Account.ts#L469)

___

### toHuman

▸ **toHuman**(): `string`

Return the Account's address

#### Returns

`string`

#### Overrides

[Entity](../wiki/api.entities.Entity.Entity).[toHuman](../wiki/api.entities.Entity.Entity#tohuman)

#### Defined in

[api/entities/Account.ts:604](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Account.ts#L604)

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
