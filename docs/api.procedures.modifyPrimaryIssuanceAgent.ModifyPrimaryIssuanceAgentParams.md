# Interface: ModifyPrimaryIssuanceAgentParams

[api/procedures/modifyPrimaryIssuanceAgent](../wiki/api.procedures.modifyPrimaryIssuanceAgent).ModifyPrimaryIssuanceAgentParams

## Table of contents

### Properties

- [requestExpiry](../wiki/api.procedures.modifyPrimaryIssuanceAgent.ModifyPrimaryIssuanceAgentParams#requestexpiry)
- [target](../wiki/api.procedures.modifyPrimaryIssuanceAgent.ModifyPrimaryIssuanceAgentParams#target)

## Properties

### requestExpiry

• `Optional` **requestExpiry**: `Date`

date at which the authorization request to modify the primary issuance agent expires (optional, never expires if a date is not provided)

#### Defined in

[api/procedures/modifyPrimaryIssuanceAgent.ts:19](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/modifyPrimaryIssuanceAgent.ts#L19)

___

### target

• **target**: `string` \| [`Identity`](../wiki/api.entities.Identity.Identity)

Identity to be set as primary issuance agent

#### Defined in

[api/procedures/modifyPrimaryIssuanceAgent.ts:15](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/modifyPrimaryIssuanceAgent.ts#L15)
