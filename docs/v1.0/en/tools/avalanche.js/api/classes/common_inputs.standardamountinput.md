[avalanche](../README.md) › [Common-Inputs](../modules/common_inputs.md) › [StandardAmountInput](common_inputs.standardamountinput.md)

# Class: StandardAmountInput

An [Input](common_inputs.input.md) class which specifies a token amount .

## Hierarchy

* [Input](common_inputs.input.md)

  ↳ **StandardAmountInput**

  ↳ [AmountInput](api_avm_inputs.amountinput.md)

  ↳ [SecpInput](api_avm_inputs.secpinput.md)

  ↳ [AmountInput](api_platformvm_inputs.amountinput.md)

  ↳ [SecpInput](api_platformvm_inputs.secpinput.md)

## Index

### Constructors

* [constructor](common_inputs.standardamountinput.md#constructor)

### Properties

* [amount](common_inputs.standardamountinput.md#protected-amount)
* [amountValue](common_inputs.standardamountinput.md#protected-amountvalue)
* [sigCount](common_inputs.standardamountinput.md#protected-sigcount)
* [sigIdxs](common_inputs.standardamountinput.md#protected-sigidxs)

### Methods

* [addSignatureIdx](common_inputs.standardamountinput.md#addsignatureidx)
* [fromBuffer](common_inputs.standardamountinput.md#frombuffer)
* [getAmount](common_inputs.standardamountinput.md#getamount)
* [getCredentialID](common_inputs.standardamountinput.md#abstract-getcredentialid)
* [getInputID](common_inputs.standardamountinput.md#abstract-getinputid)
* [getSigIdxs](common_inputs.standardamountinput.md#getsigidxs)
* [toBuffer](common_inputs.standardamountinput.md#tobuffer)
* [toString](common_inputs.standardamountinput.md#tostring)
* [comparator](common_inputs.standardamountinput.md#static-comparator)

## Constructors

###  constructor

\+ **new StandardAmountInput**(`amount`: BN): *[StandardAmountInput](common_inputs.standardamountinput.md)*

*Overrides [Input](common_inputs.input.md).[constructor](common_inputs.input.md#constructor)*

Defined in src/common/input.ts:217

An [AmountInput](api_avm_inputs.amountinput.md) class which issues a payment on an assetID.

**Parameters:**

Name | Type | Default | Description |
------ | ------ | ------ | ------ |
`amount` | BN | undefined | A [BN](https://github.com/indutny/bn.js/) representing the amount in the input  |

**Returns:** *[StandardAmountInput](common_inputs.standardamountinput.md)*

## Properties

### `Protected` amount

• **amount**: *Buffer* = Buffer.alloc(8)

Defined in src/common/input.ts:190

___

### `Protected` amountValue

• **amountValue**: *BN* = new BN(0)

Defined in src/common/input.ts:192

___

### `Protected` sigCount

• **sigCount**: *Buffer* = Buffer.alloc(4)

*Inherited from [Input](common_inputs.input.md).[sigCount](common_inputs.input.md#protected-sigcount)*

Defined in src/common/input.ts:17

___

### `Protected` sigIdxs

• **sigIdxs**: *Array‹[SigIdx](common_signature.sigidx.md)›* = []

*Inherited from [Input](common_inputs.input.md).[sigIdxs](common_inputs.input.md#protected-sigidxs)*

Defined in src/common/input.ts:19

## Methods

###  addSignatureIdx

▸ **addSignatureIdx**(`addressIdx`: number, `address`: Buffer): *void*

*Inherited from [Input](common_inputs.input.md).[addSignatureIdx](common_inputs.input.md#addsignatureidx)*

Defined in src/common/input.ts:36

Creates and adds a [SigIdx](common_signature.sigidx.md) to the [Input](common_inputs.input.md).

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`addressIdx` | number | The index of the address to reference in the signatures |
`address` | Buffer | The address of the source of the signature  |

**Returns:** *void*

___

###  fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): *number*

*Overrides [Input](common_inputs.input.md).[fromBuffer](common_inputs.input.md#frombuffer)*

Defined in src/common/input.ts:202

Popuates the instance from a [Buffer](https://github.com/feross/buffer) representing the [AmountInput](api_avm_inputs.amountinput.md) and returns the size of the output.

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`bytes` | Buffer | - |
`offset` | number | 0 |

**Returns:** *number*

___

###  getAmount

▸ **getAmount**(): *BN*

Defined in src/common/input.ts:197

Returns the amount as a [BN](https://github.com/indutny/bn.js/).

**Returns:** *BN*

___

### `Abstract` getCredentialID

▸ **getCredentialID**(): *number*

*Inherited from [Input](common_inputs.input.md).[getCredentialID](common_inputs.input.md#abstract-getcredentialid)*

Defined in src/common/input.ts:28

**Returns:** *number*

___

### `Abstract` getInputID

▸ **getInputID**(): *number*

*Inherited from [Input](common_inputs.input.md).[getInputID](common_inputs.input.md#abstract-getinputid)*

Defined in src/common/input.ts:21

**Returns:** *number*

___

###  getSigIdxs

▸ **getSigIdxs**(): *Array‹[SigIdx](common_signature.sigidx.md)›*

*Inherited from [Input](common_inputs.input.md).[getSigIdxs](common_inputs.input.md#getsigidxs)*

Defined in src/common/input.ts:26

Returns the array of [SigIdx](common_signature.sigidx.md) for this [Input](common_inputs.input.md)

**Returns:** *Array‹[SigIdx](common_signature.sigidx.md)›*

___

###  toBuffer

▸ **toBuffer**(): *Buffer*

*Overrides [Input](common_inputs.input.md).[toBuffer](common_inputs.input.md#tobuffer)*

Defined in src/common/input.ts:212

Returns the buffer representing the [AmountInput](api_avm_inputs.amountinput.md) instance.

**Returns:** *Buffer*

___

###  toString

▸ **toString**(): *string*

*Inherited from [Input](common_inputs.input.md).[toString](common_inputs.input.md#tostring)*

Defined in src/common/input.ts:76

Returns a base-58 representation of the [Input](common_inputs.input.md).

**Returns:** *string*

___

### `Static` comparator

▸ **comparator**(): *function*

*Inherited from [Input](common_inputs.input.md).[comparator](common_inputs.input.md#static-comparator)*

Defined in src/common/input.ts:80

**Returns:** *function*

▸ (`a`: [Input](common_inputs.input.md), `b`: [Input](common_inputs.input.md)): *0 | 1 | -1*

**Parameters:**

Name | Type |
------ | ------ |
`a` | [Input](common_inputs.input.md) |
`b` | [Input](common_inputs.input.md) |
