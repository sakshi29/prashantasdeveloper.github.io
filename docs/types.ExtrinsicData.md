# Interface: ExtrinsicData

[types](../wiki/types).ExtrinsicData

## Hierarchy

- **`ExtrinsicData`**

  ↳ [`ExtrinsicDataWithFees`](../wiki/types.ExtrinsicDataWithFees)

## Table of contents

### Properties

- [address](../wiki/types.ExtrinsicData#address)
- [blockHash](../wiki/types.ExtrinsicData#blockhash)
- [blockNumber](../wiki/types.ExtrinsicData#blocknumber)
- [extrinsicHash](../wiki/types.ExtrinsicData#extrinsichash)
- [extrinsicIdx](../wiki/types.ExtrinsicData#extrinsicidx)
- [nonce](../wiki/types.ExtrinsicData#nonce)
- [params](../wiki/types.ExtrinsicData#params)
- [specVersionId](../wiki/types.ExtrinsicData#specversionid)
- [success](../wiki/types.ExtrinsicData#success)
- [txTag](../wiki/types.ExtrinsicData#txtag)

## Properties

### address

• **address**: ``null`` \| `string`

public key of the signer. Unsigned transactions have no signer, in which case this value is null (example: an enacted governance proposal)

#### Defined in

[types/index.ts:329](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L329)

___

### blockHash

• **blockHash**: `string`

#### Defined in

[types/index.ts:323](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L323)

___

### blockNumber

• **blockNumber**: `BigNumber`

#### Defined in

[types/index.ts:324](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L324)

___

### extrinsicHash

• **extrinsicHash**: `string`

#### Defined in

[types/index.ts:338](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L338)

___

### extrinsicIdx

• **extrinsicIdx**: `BigNumber`

#### Defined in

[types/index.ts:325](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L325)

___

### nonce

• **nonce**: ``null`` \| `BigNumber`

nonce of the transaction. Null for unsigned transactions where address is null

#### Defined in

[types/index.ts:333](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L333)

___

### params

• **params**: `Record`<`string`, `unknown`\>[]

#### Defined in

[types/index.ts:335](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L335)

___

### specVersionId

• **specVersionId**: `BigNumber`

#### Defined in

[types/index.ts:337](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L337)

___

### success

• **success**: `boolean`

#### Defined in

[types/index.ts:336](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L336)

___

### txTag

• **txTag**: `TxTag`

#### Defined in

[types/index.ts:334](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L334)
