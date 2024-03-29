# Class: Documents

[api/entities/Asset/Documents](../wiki/api.entities.Asset.Documents).Documents

Handles all Asset Document related functionality

## Hierarchy

- `Namespace`<[`Asset`](../wiki/api.entities.Asset.Asset)\>

  ↳ **`Documents`**

## Table of contents

### Methods

- [get](../wiki/api.entities.Asset.Documents.Documents#get)
- [set](../wiki/api.entities.Asset.Documents.Documents#set)

## Methods

### get

▸ **get**(`paginationOpts?`): `Promise`<[`ResultSet`](../wiki/types.ResultSet)<[`AssetDocument`](../wiki/types.AssetDocument)\>\>

Retrieve all documents linked to the Asset

**`note`** supports pagination

#### Parameters

| Name | Type |
| :------ | :------ |
| `paginationOpts?` | [`PaginationOptions`](../wiki/types.PaginationOptions) |

#### Returns

`Promise`<[`ResultSet`](../wiki/types.ResultSet)<[`AssetDocument`](../wiki/types.AssetDocument)\>\>

#### Defined in

[api/entities/Asset/Documents.ts:43](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Asset/Documents.ts#L43)

___

### set

▸ **set**(`args`, `opts?`): `Promise`<`TransactionQueue`<[`Asset`](../wiki/api.entities.Asset.Asset), [`Asset`](../wiki/api.entities.Asset.Asset), `unknown`[][]\>\>

Assign a new list of documents to the Asset by replacing the existing list of documents with the ones passed in the parameters

This requires two transactions

**`note`** this method is of type [ProcedureMethod](../wiki/types.ProcedureMethod), which means you can call [set.checkAuthorization](../wiki/types.ProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `args` | [`SetAssetDocumentsParams`](../wiki/api.procedures.setAssetDocuments.SetAssetDocumentsParams) |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<[`Asset`](../wiki/api.entities.Asset.Asset), [`Asset`](../wiki/api.entities.Asset.Asset), `unknown`[][]\>\>

#### Defined in

[api/entities/Asset/Documents.ts:34](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Asset/Documents.ts#L34)
