[avalanche](../README.md) › [Common-NBytes](../modules/common_nbytes.md) › [NBytes](common_nbytes.nbytes.md)

# Class: NBytes

Abstract class that implements basic functionality for managing a
[Buffer](https://github.com/feross/buffer) of an exact length.

Create a class that extends this one and override bsize to make it validate for exactly
the correct length.

## Hierarchy

* **NBytes**

  ↳ [Address](common_output.address.md)

  ↳ [SigIdx](common_signature.sigidx.md)

  ↳ [Signature](common_signature.signature.md)

  ↳ [UTXOID](api_avm_operations.utxoid.md)

## Index

### Constructors

* [constructor](common_nbytes.nbytes.md#constructor)

### Properties

* [bsize](common_nbytes.nbytes.md#protected-bsize)
* [bytes](common_nbytes.nbytes.md#protected-bytes)

### Methods

* [fromBuffer](common_nbytes.nbytes.md#frombuffer)
* [fromString](common_nbytes.nbytes.md#fromstring)
* [getSize](common_nbytes.nbytes.md#getsize)
* [toBuffer](common_nbytes.nbytes.md#tobuffer)
* [toString](common_nbytes.nbytes.md#tostring)

## Constructors

###  constructor

\+ **new NBytes**(): *[NBytes](common_nbytes.nbytes.md)*

Defined in src/common/nbytes.ts:85

Returns instance of [NBytes](common_nbytes.nbytes.md).

**Returns:** *[NBytes](common_nbytes.nbytes.md)*

## Properties

### `Protected` bsize

• **bsize**: *number*

Defined in src/common/nbytes.ts:25

___

### `Protected` bytes

• **bytes**: *Buffer*

Defined in src/common/nbytes.ts:23

## Methods

###  fromBuffer

▸ **fromBuffer**(`buff`: Buffer, `offset`: number): *number*

Defined in src/common/nbytes.ts:56

Takes a [[Buffer]], verifies its length, and stores it.

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`buff` | Buffer | - |
`offset` | number | 0 |

**Returns:** *number*

The size of the [Buffer](https://github.com/feross/buffer)

___

###  fromString

▸ **fromString**(`b58str`: string): *number*

Defined in src/common/nbytes.ts:39

Takes a base-58 encoded string, verifies its length, and stores it.

**Parameters:**

Name | Type |
------ | ------ |
`b58str` | string |

**Returns:** *number*

The size of the [Buffer](https://github.com/feross/buffer)

___

###  getSize

▸ **getSize**(): *number*

Defined in src/common/nbytes.ts:32

Returns the length of the [Buffer](https://github.com/feross/buffer).

**Returns:** *number*

The exact length requirement of this class

___

###  toBuffer

▸ **toBuffer**(): *Buffer*

Defined in src/common/nbytes.ts:76

**Returns:** *Buffer*

A reference to the stored [Buffer](https://github.com/feross/buffer)

___

###  toString

▸ **toString**(): *string*

Defined in src/common/nbytes.ts:83

**Returns:** *string*

A base-58 string of the stored [Buffer](https://github.com/feross/buffer)
