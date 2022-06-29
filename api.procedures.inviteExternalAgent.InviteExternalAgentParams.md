# Interface: InviteExternalAgentParams

[api/procedures/inviteExternalAgent](../wiki/api.procedures.inviteExternalAgent).InviteExternalAgentParams

## Table of contents

### Properties

- [expiry](../wiki/api.procedures.inviteExternalAgent.InviteExternalAgentParams#expiry)
- [permissions](../wiki/api.procedures.inviteExternalAgent.InviteExternalAgentParams#permissions)
- [target](../wiki/api.procedures.inviteExternalAgent.InviteExternalAgentParams#target)

## Properties

### expiry

• `Optional` **expiry**: `Date`

date at which the authorization request for invitation expires (optional)

**`note`** if expiry date is not set, the invitation will never expire

**`note`** due to chain limitations, the expiry will be ignored if the passed `permissions` don't correspond to an existing Permission Group

#### Defined in

[api/procedures/inviteExternalAgent.ts:63](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/inviteExternalAgent.ts#L63)

___

### permissions

• **permissions**: [`CustomPermissionGroup`](../wiki/api.entities.CustomPermissionGroup.CustomPermissionGroup) \| [`KnownPermissionGroup`](../wiki/api.entities.KnownPermissionGroup.KnownPermissionGroup) \| { `transactions`: ``null`` \| [`TransactionPermissions`](../wiki/types.TransactionPermissions)  } \| { `transactionGroups`: [`TxGroup`](../wiki/types.TxGroup)[]  }

#### Defined in

[api/procedures/inviteExternalAgent.ts:48](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/inviteExternalAgent.ts#L48)

___

### target

• **target**: `string` \| [`Identity`](../wiki/api.entities.Identity.Identity)

#### Defined in

[api/procedures/inviteExternalAgent.ts:47](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/inviteExternalAgent.ts#L47)
