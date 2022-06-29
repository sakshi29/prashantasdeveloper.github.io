# Module: api/procedures/inviteExternalAgent

## Table of contents

### Interfaces

- [InviteExternalAgentParams](../wiki/api.procedures.inviteExternalAgent.InviteExternalAgentParams)

### Functions

- [createGroupAndAuthorizationResolver](../wiki/api.procedures.inviteExternalAgent#creategroupandauthorizationresolver)

## Functions

### createGroupAndAuthorizationResolver

▸ **createGroupAndAuthorizationResolver**(`target`): (`receipt`: `ISubmittableResult`) => `Promise`<[`AuthorizationRequest`](../wiki/api.entities.AuthorizationRequest.AuthorizationRequest)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `target` | [`Identity`](../wiki/api.entities.Identity.Identity) |

#### Returns

`fn`

▸ (`receipt`): `Promise`<[`AuthorizationRequest`](../wiki/api.entities.AuthorizationRequest.AuthorizationRequest)\>

##### Parameters

| Name | Type |
| :------ | :------ |
| `receipt` | `ISubmittableResult` |

##### Returns

`Promise`<[`AuthorizationRequest`](../wiki/api.entities.AuthorizationRequest.AuthorizationRequest)\>

#### Defined in

[api/procedures/inviteExternalAgent.ts:36](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/inviteExternalAgent.ts#L36)
