# Module: api/procedures/modifyComplianceRequirement

## Table of contents

### Type Aliases

- [ModifyComplianceRequirementParams](../wiki/api.procedures.modifyComplianceRequirement#modifycompliancerequirementparams)

## Type Aliases

### ModifyComplianceRequirementParams

Ƭ **ModifyComplianceRequirementParams**: `Object`

#### Type declaration

| Name | Type | Description |
| :------ | :------ | :------ |
| `conditions` | [`InputCondition`](../wiki/types#inputcondition)[] | array of conditions to replace the existing array of conditions for the requirement (identified by `id`).   Conditions within a requirement are *AND* between them. This means that in order   for a transfer to comply with this requirement, it must fulfill *ALL* conditions |
| `id` | `BigNumber` | ID of the Compliance Requirement |

#### Defined in

[api/procedures/modifyComplianceRequirement.ts:11](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/modifyComplianceRequirement.ts#L11)
