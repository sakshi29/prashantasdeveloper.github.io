# Class: DefaultTrustedClaimIssuer

[api/entities/DefaultTrustedClaimIssuer](../wiki/api.entities.DefaultTrustedClaimIssuer).DefaultTrustedClaimIssuer

Represents a default trusted claim issuer for a specific Asset in the Polymesh blockchain

## Hierarchy

- [`Identity`](../wiki/api.entities.Identity.Identity)

  ↳ **`DefaultTrustedClaimIssuer`**

## Table of contents

### Properties

- [asset](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#asset)
- [assetPermissions](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#assetpermissions)
- [authorizations](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#authorizations)
- [did](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#did)
- [portfolios](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#portfolios)
- [uuid](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#uuid)

### Methods

- [addedAt](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#addedat)
- [areSecondaryAccountsFrozen](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#aresecondaryaccountsfrozen)
- [checkRoles](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#checkroles)
- [exists](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#exists)
- [getAssetBalance](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#getassetbalance)
- [getHeldAssets](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#getheldassets)
- [getInstructions](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#getinstructions)
- [getPendingDistributions](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#getpendingdistributions)
- [getPendingInstructions](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#getpendinginstructions)
- [getPrimaryAccount](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#getprimaryaccount)
- [getScopeId](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#getscopeid)
- [getSecondaryAccounts](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#getsecondaryaccounts)
- [getTrustingAssets](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#gettrustingassets)
- [getVenues](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#getvenues)
- [hasRole](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#hasrole)
- [hasRoles](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#hasroles)
- [hasValidCdd](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#hasvalidcdd)
- [isCddProvider](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#iscddprovider)
- [isEqual](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#isequal)
- [isGcMember](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#isgcmember)
- [toHuman](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#tohuman)
- [trustedFor](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#trustedfor)
- [generateUuid](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#generateuuid)
- [unserialize](../wiki/api.entities.DefaultTrustedClaimIssuer.DefaultTrustedClaimIssuer#unserialize)

## Properties

### asset

• **asset**: [`Asset`](../wiki/api.entities.Asset.Asset)

Asset for which this Identity is a Default Trusted Claim Issuer

#### Defined in

[api/entities/DefaultTrustedClaimIssuer.ts:36](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/DefaultTrustedClaimIssuer.ts#L36)

___

### assetPermissions

• **assetPermissions**: [`AssetPermissions`](../wiki/api.entities.Identity.AssetPermissions.AssetPermissions)

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[assetPermissions](../wiki/api.entities.Identity.Identity#assetpermissions)

#### Defined in

[api/entities/Identity/index.ts:99](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L99)

___

### authorizations

• **authorizations**: [`IdentityAuthorizations`](../wiki/api.entities.Identity.IdentityAuthorizations.IdentityAuthorizations)

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[authorizations](../wiki/api.entities.Identity.Identity#authorizations)

#### Defined in

[api/entities/Identity/index.ts:97](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L97)

___

### did

• **did**: `string`

Identity ID as stored in the blockchain

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[did](../wiki/api.entities.Identity.Identity#did)

#### Defined in

[api/entities/Identity/index.ts:94](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L94)

___

### portfolios

• **portfolios**: [`Portfolios`](../wiki/api.entities.Identity.Portfolios.Portfolios)

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[portfolios](../wiki/api.entities.Identity.Identity#portfolios)

#### Defined in

[api/entities/Identity/index.ts:98](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L98)

___

### uuid

• **uuid**: `string`

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[uuid](../wiki/api.entities.Identity.Identity#uuid)

#### Defined in

[api/entities/Entity.ts:46](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Entity.ts#L46)

## Methods

### addedAt

▸ **addedAt**(): `Promise`<``null`` \| [`EventIdentifier`](../wiki/types.EventIdentifier)\>

Retrieve the identifier data (block number, date and event index) of the event that was emitted when the trusted claim issuer was added

**`note`** uses the middleware

**`note`** there is a possibility that the data is not ready by the time it is requested. In that case, `null` is returned

#### Returns

`Promise`<``null`` \| [`EventIdentifier`](../wiki/types.EventIdentifier)\>

#### Defined in

[api/entities/DefaultTrustedClaimIssuer.ts:55](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/DefaultTrustedClaimIssuer.ts#L55)

___

### areSecondaryAccountsFrozen

▸ **areSecondaryAccountsFrozen**(): `Promise`<`boolean`\>

Check whether secondary Accounts are frozen

**`note`** can be subscribed to

#### Returns

`Promise`<`boolean`\>

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[areSecondaryAccountsFrozen](../wiki/api.entities.Identity.Identity#aresecondaryaccountsfrozen)

#### Defined in

[api/entities/Identity/index.ts:594](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L594)

▸ **areSecondaryAccountsFrozen**(`callback`): `Promise`<[`UnsubCallback`](../wiki/types#unsubcallback)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `callback` | [`SubCallback`](../wiki/types#subcallback)<`boolean`\> |

#### Returns

`Promise`<[`UnsubCallback`](../wiki/types#unsubcallback)\>

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[areSecondaryAccountsFrozen](../wiki/api.entities.Identity.Identity#aresecondaryaccountsfrozen)

#### Defined in

[api/entities/Identity/index.ts:595](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L595)

___

### checkRoles

▸ **checkRoles**(`roles`): `Promise`<[`CheckRolesResult`](../wiki/types.CheckRolesResult)\>

Check whether this Identity possesses all specified roles

#### Parameters

| Name | Type |
| :------ | :------ |
| `roles` | [`Role`](../wiki/types#role)[] |

#### Returns

`Promise`<[`CheckRolesResult`](../wiki/types.CheckRolesResult)\>

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[checkRoles](../wiki/api.entities.Identity.Identity#checkroles)

#### Defined in

[api/entities/Identity/index.ts:362](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L362)

___

### exists

▸ **exists**(): `Promise`<`boolean`\>

Determine whether this Identity exists on chain

**`note`** asset Identities aren't considered to exist for the

#### Returns

`Promise`<`boolean`\>

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[exists](../wiki/api.entities.Identity.Identity#exists)

#### Defined in

[api/entities/Identity/index.ts:751](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L751)

___

### getAssetBalance

▸ **getAssetBalance**(`args`): `Promise`<`BigNumber`\>

Retrieve the balance of a particular Asset

**`note`** can be subscribed to

#### Parameters

| Name | Type |
| :------ | :------ |
| `args` | `Object` |
| `args.ticker` | `string` |

#### Returns

`Promise`<`BigNumber`\>

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[getAssetBalance](../wiki/api.entities.Identity.Identity#getassetbalance)

#### Defined in

[api/entities/Identity/index.ts:166](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L166)

▸ **getAssetBalance**(`args`, `callback`): `Promise`<[`UnsubCallback`](../wiki/types#unsubcallback)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `args` | `Object` |
| `args.ticker` | `string` |
| `callback` | [`SubCallback`](../wiki/types#subcallback)<`BigNumber`\> |

#### Returns

`Promise`<[`UnsubCallback`](../wiki/types#unsubcallback)\>

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[getAssetBalance](../wiki/api.entities.Identity.Identity#getassetbalance)

#### Defined in

[api/entities/Identity/index.ts:167](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L167)

___

### getHeldAssets

▸ **getHeldAssets**(`opts?`): `Promise`<[`ResultSet`](../wiki/types.ResultSet)<[`Asset`](../wiki/api.entities.Asset.Asset)\>\>

Retrieve a list of all Assets which were held at one point by this Identity

**`note`** uses the middleware

**`note`** supports pagination

#### Parameters

| Name | Type |
| :------ | :------ |
| `opts` | `Object` |
| `opts.order?` | `Order` |
| `opts.size?` | `BigNumber` |
| `opts.start?` | `BigNumber` |

#### Returns

`Promise`<[`ResultSet`](../wiki/types.ResultSet)<[`Asset`](../wiki/api.entities.Asset.Asset)\>\>

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[getHeldAssets](../wiki/api.entities.Identity.Identity#getheldassets)

#### Defined in

[api/entities/Identity/index.ts:320](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L320)

___

### getInstructions

▸ **getInstructions**(): `Promise`<[`GroupedInstructions`](../wiki/types.GroupedInstructions)\>

Retrieve all Instructions where this Identity is a participant,
  grouped by status

#### Returns

`Promise`<[`GroupedInstructions`](../wiki/types.GroupedInstructions)\>

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[getInstructions](../wiki/api.entities.Identity.Identity#getinstructions)

#### Defined in

[api/entities/Identity/index.ts:472](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L472)

___

### getPendingDistributions

▸ **getPendingDistributions**(): `Promise`<[`DistributionWithDetails`](../wiki/types.DistributionWithDetails)[]\>

Retrieve every Dividend Distribution for which this Identity is eligible and hasn't been paid

**`note`** uses the middleware

**`note`** this query can be potentially **SLOW** depending on which Assets this Identity has held

#### Returns

`Promise`<[`DistributionWithDetails`](../wiki/types.DistributionWithDetails)[]\>

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[getPendingDistributions](../wiki/api.entities.Identity.Identity#getpendingdistributions)

#### Defined in

[api/entities/Identity/index.ts:631](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L631)

___

### getPendingInstructions

▸ **getPendingInstructions**(): `Promise`<[`Instruction`](../wiki/api.entities.Instruction.Instruction)[]\>

Retrieve all pending Instructions involving this Identity

**`deprecated`** in favor of `getInstructions`

#### Returns

`Promise`<[`Instruction`](../wiki/api.entities.Instruction.Instruction)[]\>

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[getPendingInstructions](../wiki/api.entities.Identity.Identity#getpendinginstructions)

#### Defined in

[api/entities/Identity/index.ts:541](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L541)

___

### getPrimaryAccount

▸ **getPrimaryAccount**(): `Promise`<[`PermissionedAccount`](../wiki/types.PermissionedAccount)\>

Retrieve the primary Account associated with the Identity

**`note`** can be subscribed to

#### Returns

`Promise`<[`PermissionedAccount`](../wiki/types.PermissionedAccount)\>

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[getPrimaryAccount](../wiki/api.entities.Identity.Identity#getprimaryaccount)

#### Defined in

[api/entities/Identity/index.ts:267](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L267)

▸ **getPrimaryAccount**(`callback`): `Promise`<[`UnsubCallback`](../wiki/types#unsubcallback)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `callback` | [`SubCallback`](../wiki/types#subcallback)<[`PermissionedAccount`](../wiki/types.PermissionedAccount)\> |

#### Returns

`Promise`<[`UnsubCallback`](../wiki/types#unsubcallback)\>

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[getPrimaryAccount](../wiki/api.entities.Identity.Identity#getprimaryaccount)

#### Defined in

[api/entities/Identity/index.ts:268](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L268)

___

### getScopeId

▸ **getScopeId**(`args`): `Promise`<``null`` \| `string`\>

Retrieve the Scope ID associated to this Identity's Investor Uniqueness Claim for a specific Asset, or null
  if there is none

**`note`** more on Investor Uniqueness [here](https://developers.polymesh.network/introduction/identity#polymesh-unique-identity-system-puis) and
  [here](https://developers.polymesh.network/polymesh-docs/primitives/confidential-identity)

#### Parameters

| Name | Type |
| :------ | :------ |
| `args` | `Object` |
| `args.asset` | `string` \| [`Asset`](../wiki/api.entities.Asset.Asset) |

#### Returns

`Promise`<``null`` \| `string`\>

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[getScopeId](../wiki/api.entities.Identity.Identity#getscopeid)

#### Defined in

[api/entities/Identity/index.ts:450](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L450)

___

### getSecondaryAccounts

▸ **getSecondaryAccounts**(): `Promise`<[`PermissionedAccount`](../wiki/types.PermissionedAccount)[]\>

Get the list of secondary Accounts related to the Identity

**`note`** can be subscribed to

**`note`** This method currently lacks pagination and may be slow for identities with many thousands of keys

#### Returns

`Promise`<[`PermissionedAccount`](../wiki/types.PermissionedAccount)[]\>

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[getSecondaryAccounts](../wiki/api.entities.Identity.Identity#getsecondaryaccounts)

#### Defined in

[api/entities/Identity/index.ts:686](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L686)

▸ **getSecondaryAccounts**(`callback`): `Promise`<[`UnsubCallback`](../wiki/types#unsubcallback)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `callback` | [`SubCallback`](../wiki/types#subcallback)<[`PermissionedAccount`](../wiki/types.PermissionedAccount)[]\> |

#### Returns

`Promise`<[`UnsubCallback`](../wiki/types#unsubcallback)\>

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[getSecondaryAccounts](../wiki/api.entities.Identity.Identity#getsecondaryaccounts)

#### Defined in

[api/entities/Identity/index.ts:687](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L687)

___

### getTrustingAssets

▸ **getTrustingAssets**(): `Promise`<[`Asset`](../wiki/api.entities.Asset.Asset)[]\>

Get the list of Assets for which this Identity is a trusted claim issuer

**`note`** uses the middleware

#### Returns

`Promise`<[`Asset`](../wiki/api.entities.Asset.Asset)[]\>

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[getTrustingAssets](../wiki/api.entities.Identity.Identity#gettrustingassets)

#### Defined in

[api/entities/Identity/index.ts:397](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L397)

___

### getVenues

▸ **getVenues**(): `Promise`<[`Venue`](../wiki/api.entities.Venue.Venue)[]\>

Retrieve all Venues created by this Identity

**`note`** can be subscribed to

#### Returns

`Promise`<[`Venue`](../wiki/api.entities.Venue.Venue)[]\>

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[getVenues](../wiki/api.entities.Identity.Identity#getvenues)

#### Defined in

[api/entities/Identity/index.ts:414](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L414)

▸ **getVenues**(`callback`): `Promise`<[`UnsubCallback`](../wiki/types#unsubcallback)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `callback` | [`SubCallback`](../wiki/types#subcallback)<[`Venue`](../wiki/api.entities.Venue.Venue)[]\> |

#### Returns

`Promise`<[`UnsubCallback`](../wiki/types#unsubcallback)\>

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[getVenues](../wiki/api.entities.Identity.Identity#getvenues)

#### Defined in

[api/entities/Identity/index.ts:415](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L415)

___

### hasRole

▸ **hasRole**(`role`): `Promise`<`boolean`\>

Check whether this Identity possesses the specified Role

#### Parameters

| Name | Type |
| :------ | :------ |
| `role` | [`Role`](../wiki/types#role) |

#### Returns

`Promise`<`boolean`\>

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[hasRole](../wiki/api.entities.Identity.Identity#hasrole)

#### Defined in

[api/entities/Identity/index.ts:118](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L118)

___

### hasRoles

▸ **hasRoles**(`roles`): `Promise`<`boolean`\>

Check whether this Identity possesses all specified roles

**`deprecated`** in favor of `checkRoles`

#### Parameters

| Name | Type |
| :------ | :------ |
| `roles` | [`Role`](../wiki/types#role)[] |

#### Returns

`Promise`<`boolean`\>

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[hasRoles](../wiki/api.entities.Identity.Identity#hasroles)

#### Defined in

[api/entities/Identity/index.ts:386](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L386)

___

### hasValidCdd

▸ **hasValidCdd**(): `Promise`<`boolean`\>

Check whether this Identity has a valid CDD claim

#### Returns

`Promise`<`boolean`\>

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[hasValidCdd](../wiki/api.entities.Identity.Identity#hasvalidcdd)

#### Defined in

[api/entities/Identity/index.ts:215](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L215)

___

### isCddProvider

▸ **isCddProvider**(): `Promise`<`boolean`\>

Check whether this Identity is a CDD provider

#### Returns

`Promise`<`boolean`\>

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[isCddProvider](../wiki/api.entities.Identity.Identity#iscddprovider)

#### Defined in

[api/entities/Identity/index.ts:248](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L248)

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

[Identity](../wiki/api.entities.Identity.Identity).[isEqual](../wiki/api.entities.Identity.Identity#isequal)

#### Defined in

[api/entities/Entity.ts:61](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Entity.ts#L61)

___

### isGcMember

▸ **isGcMember**(): `Promise`<`boolean`\>

Check whether this Identity is Governance Committee member

#### Returns

`Promise`<`boolean`\>

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[isGcMember](../wiki/api.entities.Identity.Identity#isgcmember)

#### Defined in

[api/entities/Identity/index.ts:231](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L231)

___

### toHuman

▸ **toHuman**(): `string`

Return the Identity's DID

#### Returns

`string`

#### Inherited from

[Identity](../wiki/api.entities.Identity.Identity).[toHuman](../wiki/api.entities.Identity.Identity#tohuman)

#### Defined in

[api/entities/Identity/index.ts:774](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Identity/index.ts#L774)

___

### trustedFor

▸ **trustedFor**(): `Promise`<``null`` \| [`ClaimType`](../wiki/types.ClaimType)[]\>

Retrieve claim types for which this Claim Issuer is trusted. A null value means that the issuer is trusted for all claim types

#### Returns

`Promise`<``null`` \| [`ClaimType`](../wiki/types.ClaimType)[]\>

#### Defined in

[api/entities/DefaultTrustedClaimIssuer.ts:77](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/DefaultTrustedClaimIssuer.ts#L77)

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

[Identity](../wiki/api.entities.Identity.Identity).[generateUuid](../wiki/api.entities.Identity.Identity#generateuuid)

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

[Identity](../wiki/api.entities.Identity.Identity).[unserialize](../wiki/api.entities.Identity.Identity#unserialize)

#### Defined in

[api/entities/Entity.ts:23](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Entity.ts#L23)
