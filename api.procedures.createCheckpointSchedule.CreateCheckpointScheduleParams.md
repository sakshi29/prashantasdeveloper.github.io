# Interface: CreateCheckpointScheduleParams

[api/procedures/createCheckpointSchedule](../wiki/api.procedures.createCheckpointSchedule).CreateCheckpointScheduleParams

## Table of contents

### Properties

- [period](../wiki/api.procedures.createCheckpointSchedule.CreateCheckpointScheduleParams#period)
- [repetitions](../wiki/api.procedures.createCheckpointSchedule.CreateCheckpointScheduleParams#repetitions)
- [start](../wiki/api.procedures.createCheckpointSchedule.CreateCheckpointScheduleParams#start)

## Properties

### period

• **period**: ``null`` \| [`CalendarPeriod`](../wiki/types.CalendarPeriod)

The cadence with which to make Checkpoints.

**`note`** A null value indicates to create only one Checkpoint, regardless of repetitions specified. This can be used to schedule the creation of a Checkpoint in the future

#### Defined in

[api/procedures/createCheckpointSchedule.ts:30](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/createCheckpointSchedule.ts#L30)

___

### repetitions

• **repetitions**: ``null`` \| `BigNumber`

The number of snapshots to take. A null value indicates snapshots should be made indefinitely

#### Defined in

[api/procedures/createCheckpointSchedule.ts:34](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/createCheckpointSchedule.ts#L34)

___

### start

• **start**: ``null`` \| `Date`

The date from which to begin creating snapshots. A null value indicates immediately

#### Defined in

[api/procedures/createCheckpointSchedule.ts:25](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/createCheckpointSchedule.ts#L25)
