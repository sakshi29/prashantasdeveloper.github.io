# Interface: CheckRolesResult

[types](../wiki/types).CheckRolesResult

Result of a `checkRoles` call

## Table of contents

### Properties

- [message](../wiki/types.CheckRolesResult#message)
- [missingRoles](../wiki/types.CheckRolesResult#missingroles)
- [result](../wiki/types.CheckRolesResult#result)

## Properties

### message

• `Optional` **message**: `string`

optional message explaining the reason for failure in special cases

#### Defined in

[types/index.ts:988](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L988)

___

### missingRoles

• `Optional` **missingRoles**: [`Role`](../wiki/types#role)[]

required roles which the Identity *DOESN'T* have. Only present if `result` is `false`

#### Defined in

[types/index.ts:980](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L980)

___

### result

• **result**: `boolean`

whether the signer possesses all the required roles or not

#### Defined in

[types/index.ts:984](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L984)
