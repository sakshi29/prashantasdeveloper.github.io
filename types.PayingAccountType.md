# Enumeration: PayingAccountType

[types](../wiki/types).PayingAccountType

Type of relationship between a paying account and a beneficiary

## Table of contents

### Enumeration Members

- [Other](../wiki/types.PayingAccountType#other)
- [Subsidy](../wiki/types.PayingAccountType#subsidy)

## Enumeration Members

### Other

• **Other**

the paying Account is paying for a specific transaction because of
  chain-specific constraints (i.e. the caller is accepting an invitation to an Identity
  and cannot have any funds to pay for it by definition)

#### Defined in

[types/index.ts:726](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L726)

___

### Subsidy

• **Subsidy**

the paying Account is currently subsidizing the caller

#### Defined in

[types/index.ts:720](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L720)
