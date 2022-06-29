# Module: api/entities/Asset/Checkpoints/types

## Table of contents

### Enumerations

- [CaCheckpointType](../wiki/api.entities.Asset.Checkpoints.types.CaCheckpointType)

### Type Aliases

- [InputCaCheckpoint](../wiki/api.entities.Asset.Checkpoints.types#inputcacheckpoint)

## Type Aliases

### InputCaCheckpoint

Ƭ **InputCaCheckpoint**: [`Checkpoint`](../wiki/api.entities.Checkpoint.Checkpoint) \| [`CheckpointSchedule`](../wiki/api.entities.CheckpointSchedule.CheckpointSchedule) \| `Date` \| { `id`: `BigNumber` ; `type`: [`Existing`](../wiki/api.entities.Asset.Checkpoints.types.CaCheckpointType#existing)  } \| { `id`: `BigNumber` ; `type`: [`Schedule`](../wiki/api.entities.Asset.Checkpoints.types.CaCheckpointType#schedule)  }

#### Defined in

[api/entities/Asset/Checkpoints/types.ts:10](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Asset/Checkpoints/types.ts#L10)
