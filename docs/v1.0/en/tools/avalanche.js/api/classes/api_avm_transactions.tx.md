[avalanche](../README.md) › [API-AVM-Transactions](../modules/api_avm_transactions.md) › [Tx](api_avm_transactions.tx.md)

# Class: Tx

## Hierarchy

* [StandardTx](common_transactions.standardtx.md)‹[AVMKeyPair](api_avm_keychain.avmkeypair.md), [AVMKeyChain](api_avm_keychain.avmkeychain.md), [UnsignedTx](api_avm_transactions.unsignedtx.md)›

  ↳ **Tx**

## Index

### Constructors

* [constructor](api_avm_transactions.tx.md#constructor)

### Properties

* [credentials](api_avm_transactions.tx.md#protected-credentials)
* [unsignedTx](api_avm_transactions.tx.md#protected-unsignedtx)

### Methods

* [fromBuffer](api_avm_transactions.tx.md#frombuffer)
* [fromString](api_avm_transactions.tx.md#fromstring)
* [getUnsignedTx](api_avm_transactions.tx.md#getunsignedtx)
* [toBuffer](api_avm_transactions.tx.md#tobuffer)
* [toString](api_avm_transactions.tx.md#tostring)

## Constructors

###  constructor

\+ **new Tx**(`unsignedTx`: [UnsignedTx](api_avm_transactions.unsignedtx.md), `credentials`: Array‹[Credential](common_signature.credential.md)›): *[Tx](api_avm_transactions.tx.md)*

*Inherited from [StandardTx](common_transactions.standardtx.md).[constructor](common_transactions.standardtx.md#constructor)*

Defined in src/common/tx.ts:313

Class representing a signed transaction.

**Parameters:**

Name | Type | Default | Description |
------ | ------ | ------ | ------ |
`unsignedTx` | [UnsignedTx](api_avm_transactions.unsignedtx.md) | undefined | Optional [StandardUnsignedTx](common_transactions.standardunsignedtx.md) |
`credentials` | Array‹[Credential](common_signature.credential.md)› | undefined | - |

**Returns:** *[Tx](api_avm_transactions.tx.md)*

## Properties

### `Protected` credentials

• **credentials**: *Array‹[Credential](common_signature.credential.md)›* = []

*Inherited from [StandardTx](common_transactions.standardtx.md).[credentials](common_transactions.standardtx.md#protected-credentials)*

Defined in src/common/tx.ts:257

___

### `Protected` unsignedTx

• **unsignedTx**: *[UnsignedTx](api_avm_transactions.unsignedtx.md)* = undefined

*Inherited from [StandardTx](common_transactions.standardtx.md).[unsignedTx](common_transactions.standardtx.md#protected-unsignedtx)*

Defined in src/common/tx.ts:256

## Methods

###  fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): *number*

*Overrides [StandardTx](common_transactions.standardtx.md).[fromBuffer](common_transactions.standardtx.md#abstract-frombuffer)*

Defined in src/apis/avm/tx.ts:59

Takes a [Buffer](https://github.com/feross/buffer) containing an [Tx](api_avm_transactions.tx.md), parses it, populates the class, and returns the length of the Tx in bytes.

**Parameters:**

Name | Type | Default | Description |
------ | ------ | ------ | ------ |
`bytes` | Buffer | - | A [Buffer](https://github.com/feross/buffer) containing a raw [Tx](api_avm_transactions.tx.md) |
`offset` | number | 0 | A number representing the starting point of the bytes to begin parsing  |

**Returns:** *number*

The length of the raw [Tx](api_avm_transactions.tx.md)

___

###  fromString

▸ **fromString**(`serialized`: string): *number*

*Inherited from [StandardTx](common_transactions.standardtx.md).[fromString](common_transactions.standardtx.md#fromstring)*

Defined in src/common/tx.ts:301

Takes a base-58 string containing an [StandardTx](common_transactions.standardtx.md), parses it, populates the class, and returns the length of the Tx in bytes.

**`remarks`** 
unlike most fromStrings, it expects the string to be serialized in cb58 format

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`serialized` | string | A base-58 string containing a raw [StandardTx](common_transactions.standardtx.md)  |

**Returns:** *number*

The length of the raw [StandardTx](common_transactions.standardtx.md)

___

###  getUnsignedTx

▸ **getUnsignedTx**(): *[UnsignedTx](api_avm_transactions.unsignedtx.md)*

*Inherited from [StandardTx](common_transactions.standardtx.md).[getUnsignedTx](common_transactions.standardtx.md#getunsignedtx)*

Defined in src/common/tx.ts:262

Returns the [StandardUnsignedTx](common_transactions.standardunsignedtx.md)

**Returns:** *[UnsignedTx](api_avm_transactions.unsignedtx.md)*

___

###  toBuffer

▸ **toBuffer**(): *Buffer*

*Inherited from [StandardTx](common_transactions.standardtx.md).[toBuffer](common_transactions.standardtx.md#tobuffer)*

Defined in src/common/tx.ts:271

Returns a [Buffer](https://github.com/feross/buffer) representation of the [StandardTx](common_transactions.standardtx.md).

**Returns:** *Buffer*

___

###  toString

▸ **toString**(): *string*

*Inherited from [StandardTx](common_transactions.standardtx.md).[toString](common_transactions.standardtx.md#tostring)*

Defined in src/common/tx.ts:311

Returns a cb58 representation of the [StandardTx](common_transactions.standardtx.md).

**`remarks`** 
unlike most toStrings, this returns in cb58 serialization format

**Returns:** *string*
