# Interface: ExtrinsicDataWithFees

[types](../wiki/types).ExtrinsicDataWithFees

## Hierarchy

- [`ExtrinsicData`](../wiki/types.ExtrinsicData)

  ↳ **`ExtrinsicDataWithFees`**

## Table of contents

### Properties

- [address](../wiki/types.ExtrinsicDataWithFees#address)
- [blockHash](../wiki/types.ExtrinsicDataWithFees#blockhash)
- [blockNumber](../wiki/types.ExtrinsicDataWithFees#blocknumber)
- [extrinsicHash](../wiki/types.ExtrinsicDataWithFees#extrinsichash)
- [extrinsicIdx](../wiki/types.ExtrinsicDataWithFees#extrinsicidx)
- [fee](../wiki/types.ExtrinsicDataWithFees#fee)
- [nonce](../wiki/types.ExtrinsicDataWithFees#nonce)
- [params](../wiki/types.ExtrinsicDataWithFees#params)
- [specVersionId](../wiki/types.ExtrinsicDataWithFees#specversionid)
- [success](../wiki/types.ExtrinsicDataWithFees#success)
- [txTag](../wiki/types.ExtrinsicDataWithFees#txtag)

## Properties

### address

• **address**: ``null`` \| `string`

public key of the signer. Unsigned transactions have no signer, in which case this value is null (example: an enacted governance proposal)

#### Inherited from

[ExtrinsicData](../wiki/types.ExtrinsicData).[address](../wiki/types.ExtrinsicData#address)

#### Defined in

[types/index.ts:329](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L329)

___

### blockHash

• **blockHash**: `string`

#### Inherited from

[ExtrinsicData](../wiki/types.ExtrinsicData).[blockHash](../wiki/types.ExtrinsicData#blockhash)

#### Defined in

[types/index.ts:323](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L323)

___

### blockNumber

• **blockNumber**: `BigNumber`

#### Inherited from

[ExtrinsicData](../wiki/types.ExtrinsicData).[blockNumber](../wiki/types.ExtrinsicData#blocknumber)

#### Defined in

[types/index.ts:324](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L324)

___

### extrinsicHash

• **extrinsicHash**: `string`

#### Inherited from

[ExtrinsicData](../wiki/types.ExtrinsicData).[extrinsicHash](../wiki/types.ExtrinsicData#extrinsichash)

#### Defined in

[types/index.ts:338](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L338)

___

### extrinsicIdx

• **extrinsicIdx**: `BigNumber`

#### Inherited from

[ExtrinsicData](../wiki/types.ExtrinsicData).[extrinsicIdx](../wiki/types.ExtrinsicData#extrinsicidx)

#### Defined in

[types/index.ts:325](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L325)

___

### fee

• **fee**: [`Fees`](../wiki/types.Fees)

#### Defined in

[types/index.ts:342](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L342)

___

### nonce

• **nonce**: ``null`` \| `BigNumber`

nonce of the transaction. Null for unsigned transactions where address is null

#### Inherited from

[ExtrinsicData](../wiki/types.ExtrinsicData).[nonce](../wiki/types.ExtrinsicData#nonce)

#### Defined in

[types/index.ts:333](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L333)

___

### params

• **params**: `Record`<`string`, `unknown`\>[]

#### Inherited from

[ExtrinsicData](../wiki/types.ExtrinsicData).[params](../wiki/types.ExtrinsicData#params)

#### Defined in

[types/index.ts:335](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L335)

___

### specVersionId

• **specVersionId**: `BigNumber`

#### Inherited from

[ExtrinsicData](../wiki/types.ExtrinsicData).[specVersionId](../wiki/types.ExtrinsicData#specversionid)

#### Defined in

[types/index.ts:337](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L337)

___

### success

• **success**: `boolean`

#### Inherited from

[ExtrinsicData](../wiki/types.ExtrinsicData).[success](../wiki/types.ExtrinsicData#success)

#### Defined in

[types/index.ts:336](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L336)

___

### txTag

• **txTag**: `TxTag`

#### Inherited from

[ExtrinsicData](../wiki/types.ExtrinsicData).[txTag](../wiki/types.ExtrinsicData#txtag)

#### Defined in

[types/index.ts:334](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L334)
