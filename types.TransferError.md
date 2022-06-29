# Enumeration: TransferError

[types](../wiki/types).TransferError

Akin to TransferStatus, these are a bit more granular and specific. Every TransferError translates to
  a [TransferStatus](../wiki/types.TransferStatus), but two or more TransferErrors can represent the same TransferStatus, and
  not all Transfer Statuses are represented by a TransferError

## Table of contents

### Enumeration Members

- [InsufficientBalance](../wiki/types.TransferError#insufficientbalance)
- [InsufficientPortfolioBalance](../wiki/types.TransferError#insufficientportfoliobalance)
- [InvalidGranularity](../wiki/types.TransferError#invalidgranularity)
- [InvalidReceiverCdd](../wiki/types.TransferError#invalidreceivercdd)
- [InvalidReceiverPortfolio](../wiki/types.TransferError#invalidreceiverportfolio)
- [InvalidSenderCdd](../wiki/types.TransferError#invalidsendercdd)
- [InvalidSenderPortfolio](../wiki/types.TransferError#invalidsenderportfolio)
- [ScopeClaimMissing](../wiki/types.TransferError#scopeclaimmissing)
- [SelfTransfer](../wiki/types.TransferError#selftransfer)
- [TransfersFrozen](../wiki/types.TransferError#transfersfrozen)

## Enumeration Members

### InsufficientBalance

• **InsufficientBalance**

translates to TransferStatus.InsufficientBalance

occurs if the sender Identity does not have enough balance to cover the amount

#### Defined in

[types/index.ts:618](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L618)

___

### InsufficientPortfolioBalance

• **InsufficientPortfolioBalance**

translates to TransferStatus.PortfolioFailure

occurs if the sender Portfolio does not have enough balance to cover the amount

#### Defined in

[types/index.ts:642](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L642)

___

### InvalidGranularity

• **InvalidGranularity**

translates to TransferStatus.InvalidGranularity

occurs if attempting to transfer decimal amounts of a non-divisible token

#### Defined in

[types/index.ts:587](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L587)

___

### InvalidReceiverCdd

• **InvalidReceiverCdd**

translates to TransferStatus.InvalidReceiverIdentity

occurs if the receiver Identity doesn't have a valid CDD claim

#### Defined in

[types/index.ts:599](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L599)

___

### InvalidReceiverPortfolio

• **InvalidReceiverPortfolio**

translates to TransferStatus.PortfolioFailure

occurs if the receiver Portfolio doesn't exist

#### Defined in

[types/index.ts:636](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L636)

___

### InvalidSenderCdd

• **InvalidSenderCdd**

translates to TransferStatus.InvalidSenderIdentity

occurs if the receiver Identity doesn't have a valid CDD claim

#### Defined in

[types/index.ts:605](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L605)

___

### InvalidSenderPortfolio

• **InvalidSenderPortfolio**

translates to TransferStatus.PortfolioFailure

occurs if the sender Portfolio doesn't exist

#### Defined in

[types/index.ts:630](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L630)

___

### ScopeClaimMissing

• **ScopeClaimMissing**

translates to TransferStatus.ScopeClaimMissing

occurs if one of the participants doesn't have a valid Investor Uniqueness Claim for
  the Asset

#### Defined in

[types/index.ts:612](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L612)

___

### SelfTransfer

• **SelfTransfer**

translates to TransferStatus.InvalidReceiverIdentity

occurs if the origin and destination Identities are the same

#### Defined in

[types/index.ts:593](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L593)

___

### TransfersFrozen

• **TransfersFrozen**

translates to TransferStatus.TransfersHalted

occurs if the Asset's transfers are frozen

#### Defined in

[types/index.ts:624](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L624)
