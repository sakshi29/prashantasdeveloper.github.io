# Interface: Balance

[types](../wiki/types).Balance

## Hierarchy

- **`Balance`**

  ↳ [`PortfolioBalance`](../wiki/api.entities.Portfolio.types.PortfolioBalance)

## Table of contents

### Properties

- [free](../wiki/types.Balance#free)
- [locked](../wiki/types.Balance#locked)
- [total](../wiki/types.Balance#total)

## Properties

### free

• **free**: `BigNumber`

balance available for transferring and paying fees

#### Defined in

[types/index.ts:671](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L671)

___

### locked

• **locked**: `BigNumber`

unavailable balance, either bonded for staking or locked for some other purpose

#### Defined in

[types/index.ts:675](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L675)

___

### total

• **total**: `BigNumber`

free + locked

#### Defined in

[types/index.ts:679](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L679)
