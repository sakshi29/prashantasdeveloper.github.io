# Class: Network

[api/client/Network](../wiki/api.client.Network).Network

Handles all Network related functionality, including querying for historical events from middleware

## Table of contents

### Methods

- [getEventByIndexedArgs](../wiki/api.client.Network.Network#geteventbyindexedargs)
- [getEventsByIndexedArgs](../wiki/api.client.Network.Network#geteventsbyindexedargs)
- [getLatestBlock](../wiki/api.client.Network.Network#getlatestblock)
- [getNetworkProperties](../wiki/api.client.Network.Network#getnetworkproperties)
- [getProtocolFees](../wiki/api.client.Network.Network#getprotocolfees)
- [getSs58Format](../wiki/api.client.Network.Network#getss58format)
- [getTransactionByHash](../wiki/api.client.Network.Network#gettransactionbyhash)
- [getTreasuryAccount](../wiki/api.client.Network.Network#gettreasuryaccount)
- [getTreasuryBalance](../wiki/api.client.Network.Network#gettreasurybalance)
- [getVersion](../wiki/api.client.Network.Network#getversion)
- [transferPolyx](../wiki/api.client.Network.Network#transferpolyx)

## Methods

### getEventByIndexedArgs

▸ **getEventByIndexedArgs**(`opts`): `Promise`<``null`` \| [`EventIdentifier`](../wiki/types.EventIdentifier)\>

Retrieve a single event by any of its indexed arguments. Can be filtered using parameters

**`note`** uses the middleware

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `opts` | `Object` | - |
| `opts.eventArg0?` | `string` | event parameter value to filter by in position 0 |
| `opts.eventArg1?` | `string` | event parameter value to filter by in position 1 |
| `opts.eventArg2?` | `string` | event parameter value to filter by in position 2 |
| `opts.eventId` | `EventIdEnum` | type of the event to fetch |
| `opts.moduleId` | `ModuleIdEnum` | type of the module to fetch |

#### Returns

`Promise`<``null`` \| [`EventIdentifier`](../wiki/types.EventIdentifier)\>

#### Defined in

[api/client/Network.ts:158](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/client/Network.ts#L158)

___

### getEventsByIndexedArgs

▸ **getEventsByIndexedArgs**(`opts`): `Promise`<``null`` \| [`EventIdentifier`](../wiki/types.EventIdentifier)[]\>

Retrieve a list of events. Can be filtered using parameters

**`note`** uses the middleware

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `opts` | `Object` | - |
| `opts.eventArg0?` | `string` | event parameter value to filter by in position 0 |
| `opts.eventArg1?` | `string` | event parameter value to filter by in position 1 |
| `opts.eventArg2?` | `string` | event parameter value to filter by in position 2 |
| `opts.eventId` | `EventIdEnum` | type of the event to fetch |
| `opts.moduleId` | `ModuleIdEnum` | type of the module to fetch |
| `opts.size?` | `BigNumber` | page size |
| `opts.start?` | `BigNumber` | page offset |

#### Returns

`Promise`<``null`` \| [`EventIdentifier`](../wiki/types.EventIdentifier)[]\>

#### Defined in

[api/client/Network.ts:197](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/client/Network.ts#L197)

___

### getLatestBlock

▸ **getLatestBlock**(): `Promise`<`BigNumber`\>

Retrieve the number of the latest block in the chain

#### Returns

`Promise`<`BigNumber`\>

#### Defined in

[api/client/Network.ts:52](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/client/Network.ts#L52)

___

### getNetworkProperties

▸ **getNetworkProperties**(): `Promise`<[`NetworkProperties`](../wiki/types.NetworkProperties)\>

Retrieve information for the current network

#### Returns

`Promise`<[`NetworkProperties`](../wiki/types.NetworkProperties)\>

#### Defined in

[api/client/Network.ts:73](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/client/Network.ts#L73)

___

### getProtocolFees

▸ **getProtocolFees**(`args`): `Promise`<[`ProtocolFees`](../wiki/types.ProtocolFees)[]\>

Retrieve the protocol fees associated with running specific transactions

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `args` | `Object` | - |
| `args.tags` | `TxTag`[] | list of transaction tags (i.e. [TxTags.asset.CreateAsset, TxTags.asset.RegisterTicker] or ["asset.createAsset", "asset.registerTicker"]) |

#### Returns

`Promise`<[`ProtocolFees`](../wiki/types.ProtocolFees)[]\>

#### Defined in

[api/client/Network.ts:97](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/client/Network.ts#L97)

___

### getSs58Format

▸ **getSs58Format**(): `BigNumber`

Retrieve the chain's SS58 format

#### Returns

`BigNumber`

#### Defined in

[api/client/Network.ts:66](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/client/Network.ts#L66)

___

### getTransactionByHash

▸ **getTransactionByHash**(`opts`): `Promise`<``null`` \| [`ExtrinsicDataWithFees`](../wiki/types.ExtrinsicDataWithFees)\>

Retrieve a transaction by hash

**`note`** uses the middleware

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `opts` | `Object` | - |
| `opts.txHash` | `string` | hash of the transaction |

#### Returns

`Promise`<``null`` \| [`ExtrinsicDataWithFees`](../wiki/types.ExtrinsicDataWithFees)\>

#### Defined in

[api/client/Network.ts:241](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/client/Network.ts#L241)

___

### getTreasuryAccount

▸ **getTreasuryAccount**(): [`Account`](../wiki/api.entities.Account.Account)

Get the treasury wallet address

#### Returns

[`Account`](../wiki/api.entities.Account.Account)

#### Defined in

[api/client/Network.ts:104](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/client/Network.ts#L104)

___

### getTreasuryBalance

▸ **getTreasuryBalance**(): `Promise`<`BigNumber`\>

Get the Treasury POLYX balance

**`note`** can be subscribed to

#### Returns

`Promise`<`BigNumber`\>

#### Defined in

[api/client/Network.ts:117](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/client/Network.ts#L117)

▸ **getTreasuryBalance**(`callback`): `Promise`<[`UnsubCallback`](../wiki/types#unsubcallback)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `callback` | [`SubCallback`](../wiki/types#subcallback)<`BigNumber`\> |

#### Returns

`Promise`<[`UnsubCallback`](../wiki/types#unsubcallback)\>

#### Defined in

[api/client/Network.ts:118](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/client/Network.ts#L118)

___

### getVersion

▸ **getVersion**(): `Promise`<`string`\>

Fetch the current network version (i.e. 3.1.0)

#### Returns

`Promise`<`string`\>

#### Defined in

[api/client/Network.ts:59](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/client/Network.ts#L59)

___

### transferPolyx

▸ **transferPolyx**(`args`, `opts?`): `Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

Transfer an amount of POLYX to a specified Account

**`note`** this method is of type [ProcedureMethod](../wiki/types.ProcedureMethod), which means you can call [transferPolyx.checkAuthorization](../wiki/types.ProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `args` | [`TransferPolyxParams`](../wiki/api.procedures.transferPolyx.TransferPolyxParams) |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

#### Defined in

[api/client/Network.ts:143](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/client/Network.ts#L143)
