# Interface: AddAssetRequirementParams

[api/procedures/addAssetRequirement](../wiki/api.procedures.addAssetRequirement).AddAssetRequirementParams

## Table of contents

### Properties

- [conditions](../wiki/api.procedures.addAssetRequirement.AddAssetRequirementParams#conditions)

## Properties

### conditions

• **conditions**: [`InputCondition`](../wiki/types#inputcondition)[]

array of conditions that form the requirement that must be added.
  Conditions within a requirement are *AND* between them. This means that in order
  for a transfer to comply with this requirement, it must fulfill *ALL* conditions

#### Defined in

[api/procedures/addAssetRequirement.ts:17](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/addAssetRequirement.ts#L17)
