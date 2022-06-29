# Interface: ThirdPartyFees

[types](../wiki/types).ThirdPartyFees

Breakdown of the fees that will be paid by a specific third party in a Transaction Queue

## Hierarchy

- [`PayingAccount`](../wiki/types.PayingAccount)

  ↳ **`ThirdPartyFees`**

## Table of contents

### Properties

- [account](../wiki/types.ThirdPartyFees#account)
- [allowance](../wiki/types.ThirdPartyFees#allowance)
- [balance](../wiki/types.ThirdPartyFees#balance)
- [fees](../wiki/types.ThirdPartyFees#fees)
- [type](../wiki/types.ThirdPartyFees#type)

## Properties

### account

• **account**: [`Account`](../wiki/api.entities.Account.Account)

Account that pays for the transaction

#### Inherited from

[PayingAccount](../wiki/types.PayingAccount).[account](../wiki/types.PayingAccount#account)

#### Defined in

[types/index.ts:738](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L738)

___

### allowance

• **allowance**: ``null`` \| `BigNumber`

total amount that will be paid for

#### Inherited from

[PayingAccount](../wiki/types.PayingAccount).[allowance](../wiki/types.PayingAccount#allowance)

#### Defined in

[types/index.ts:742](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L742)

___

### balance

• **balance**: `BigNumber`

free balance of the third party Account

#### Defined in

[types/index.ts:756](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L756)

___

### fees

• **fees**: [`Fees`](../wiki/types.Fees)

fees that will be paid by the third party Account

#### Defined in

[types/index.ts:752](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L752)

___

### type

• **type**: [`PayingAccountType`](../wiki/types.PayingAccountType)

#### Inherited from

[PayingAccount](../wiki/types.PayingAccount).[type](../wiki/types.PayingAccount#type)

#### Defined in

[types/index.ts:734](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L734)
