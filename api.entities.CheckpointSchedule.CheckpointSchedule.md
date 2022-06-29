# Class: CheckpointSchedule

[api/entities/CheckpointSchedule](../wiki/api.entities.CheckpointSchedule).CheckpointSchedule

Represents a Checkpoint Schedule for an Asset. Schedules can be set up to create Checkpoints at regular intervals

## Hierarchy

- [`Entity`](../wiki/api.entities.Entity.Entity)<[`UniqueIdentifiers`](../wiki/api.entities.CheckpointSchedule.UniqueIdentifiers), `HumanReadable`\>

  ↳ **`CheckpointSchedule`**

## Table of contents

### Properties

- [asset](../wiki/api.entities.CheckpointSchedule.CheckpointSchedule#asset)
- [complexity](../wiki/api.entities.CheckpointSchedule.CheckpointSchedule#complexity)
- [expiryDate](../wiki/api.entities.CheckpointSchedule.CheckpointSchedule#expirydate)
- [id](../wiki/api.entities.CheckpointSchedule.CheckpointSchedule#id)
- [period](../wiki/api.entities.CheckpointSchedule.CheckpointSchedule#period)
- [start](../wiki/api.entities.CheckpointSchedule.CheckpointSchedule#start)
- [uuid](../wiki/api.entities.CheckpointSchedule.CheckpointSchedule#uuid)

### Methods

- [details](../wiki/api.entities.CheckpointSchedule.CheckpointSchedule#details)
- [exists](../wiki/api.entities.CheckpointSchedule.CheckpointSchedule#exists)
- [getCheckpoints](../wiki/api.entities.CheckpointSchedule.CheckpointSchedule#getcheckpoints)
- [isEqual](../wiki/api.entities.CheckpointSchedule.CheckpointSchedule#isequal)
- [toHuman](../wiki/api.entities.CheckpointSchedule.CheckpointSchedule#tohuman)
- [generateUuid](../wiki/api.entities.CheckpointSchedule.CheckpointSchedule#generateuuid)
- [unserialize](../wiki/api.entities.CheckpointSchedule.CheckpointSchedule#unserialize)

## Properties

### asset

• **asset**: [`Asset`](../wiki/api.entities.Asset.Asset)

Asset for which Checkpoints are scheduled

#### Defined in

[api/entities/CheckpointSchedule/index.ts:65](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/CheckpointSchedule/index.ts#L65)

___

### complexity

• **complexity**: `BigNumber`

abstract measure of the complexity of this Schedule. Shorter periods translate into more complexity

#### Defined in

[api/entities/CheckpointSchedule/index.ts:87](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/CheckpointSchedule/index.ts#L87)

___

### expiryDate

• **expiryDate**: ``null`` \| `Date`

date at which the last Checkpoint will be created with this Schedule.
  A null value means that this Schedule never expires

#### Defined in

[api/entities/CheckpointSchedule/index.ts:82](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/CheckpointSchedule/index.ts#L82)

___

### id

• **id**: `BigNumber`

schedule identifier number

#### Defined in

[api/entities/CheckpointSchedule/index.ts:60](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/CheckpointSchedule/index.ts#L60)

___

### period

• **period**: ``null`` \| [`CalendarPeriod`](../wiki/types.CalendarPeriod)

how often this Schedule creates a Checkpoint. A null value means this Schedule
  creates a single Checkpoint and then expires

#### Defined in

[api/entities/CheckpointSchedule/index.ts:71](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/CheckpointSchedule/index.ts#L71)

___

### start

• **start**: `Date`

first Checkpoint creation date

#### Defined in

[api/entities/CheckpointSchedule/index.ts:76](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/CheckpointSchedule/index.ts#L76)

___

### uuid

• **uuid**: `string`

#### Inherited from

[Entity](../wiki/api.entities.Entity.Entity).[uuid](../wiki/api.entities.Entity.Entity#uuid)

#### Defined in

[api/entities/Entity.ts:46](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Entity.ts#L46)

## Methods

### details

▸ **details**(): `Promise`<[`ScheduleDetails`](../wiki/api.entities.CheckpointSchedule.types.ScheduleDetails)\>

Retrieve information specific to this Schedule

#### Returns

`Promise`<[`ScheduleDetails`](../wiki/api.entities.CheckpointSchedule.types.ScheduleDetails)\>

#### Defined in

[api/entities/CheckpointSchedule/index.ts:123](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/CheckpointSchedule/index.ts#L123)

___

### exists

▸ **exists**(): `Promise`<`boolean`\>

Determine whether this Checkpoint Schedule exists on chain

#### Returns

`Promise`<`boolean`\>

#### Overrides

[Entity](../wiki/api.entities.Entity.Entity).[exists](../wiki/api.entities.Entity.Entity#exists)

#### Defined in

[api/entities/CheckpointSchedule/index.ts:189](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/CheckpointSchedule/index.ts#L189)

___

### getCheckpoints

▸ **getCheckpoints**(): `Promise`<[`Checkpoint`](../wiki/api.entities.Checkpoint.Checkpoint)[]\>

Retrieve all Checkpoints created by this Schedule

#### Returns

`Promise`<[`Checkpoint`](../wiki/api.entities.Checkpoint.Checkpoint)[]\>

#### Defined in

[api/entities/CheckpointSchedule/index.ts:157](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/CheckpointSchedule/index.ts#L157)

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

### toHuman

▸ **toHuman**(): `HumanReadable`

Return the Schedule's static data

#### Returns

`HumanReadable`

#### Overrides

[Entity](../wiki/api.entities.Entity.Entity).[toHuman](../wiki/api.entities.Entity.Entity#tohuman)

#### Defined in

[api/entities/CheckpointSchedule/index.ts:211](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/CheckpointSchedule/index.ts#L211)

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
