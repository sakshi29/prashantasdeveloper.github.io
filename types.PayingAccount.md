# Interface: PayingAccount

[types](../wiki/types).PayingAccount

Represents a relationship in which a third party Account
  is paying for a transaction on behalf of the caller

## Hierarchy

- **`PayingAccount`**

  ↳ [`ThirdPartyFees`](../wiki/types.ThirdPartyFees)

## Table of contents

### Properties

- [account](../wiki/types.PayingAccount#account)
- [allowance](../wiki/types.PayingAccount#allowance)
- [type](../wiki/types.PayingAccount#type)

## Properties

### account

• **account**: [`Account`](../wiki/api.entities.Account.Account)

Account that pays for the transaction

#### Defined in

[types/index.ts:738](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L738)

___

### allowance

• **allowance**: ``null`` \| `BigNumber`

total amount that will be paid for

#### Defined in

[types/index.ts:742](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L742)

___

### type

• **type**: [`PayingAccountType`](../wiki/types.PayingAccountType)

#### Defined in

[types/index.ts:734](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L734)
