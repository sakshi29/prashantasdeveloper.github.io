# Interface: MoveFundsParams

[api/procedures/moveFunds](../wiki/api.procedures.moveFunds).MoveFundsParams

## Table of contents

### Properties

- [items](../wiki/api.procedures.moveFunds.MoveFundsParams#items)
- [to](../wiki/api.procedures.moveFunds.MoveFundsParams#to)

## Properties

### items

• **items**: [`PortfolioMovement`](../wiki/types.PortfolioMovement)[]

list of Assets (and the corresponding token amounts) that will be moved

#### Defined in

[api/procedures/moveFunds.ts:22](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/moveFunds.ts#L22)

___

### to

• `Optional` **to**: `BigNumber` \| [`NumberedPortfolio`](../wiki/api.entities.NumberedPortfolio.NumberedPortfolio) \| [`DefaultPortfolio`](../wiki/api.entities.DefaultPortfolio.DefaultPortfolio)

portfolio (or portfolio ID) that will receive the funds. Optional, if no value is passed, the funds will be moved to the default Portfolio of this Portfolio's owner

#### Defined in

[api/procedures/moveFunds.ts:18](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/moveFunds.ts#L18)
