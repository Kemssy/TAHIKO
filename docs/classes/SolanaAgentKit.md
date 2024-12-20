[**solana-agent-kit v1.1.1**](../README.md)

***

[solana-agent-kit](../README.md) / SolanaAgentKit

# Class: SolanaAgentKit

Main class for interacting with Solana blockchain
Provides a unified interface for token operations, NFT management, and trading

 SolanaAgentKit

## Constructors

### new SolanaAgentKit()

> **new SolanaAgentKit**(`private_key`, `rpc_url`, `openai_api_key`): [`SolanaAgentKit`](SolanaAgentKit.md)

#### Parameters

##### private\_key

`string`

##### rpc\_url

`string` = `"https://api.mainnet-beta.solana.com"`

##### openai\_api\_key

`string`

#### Returns

[`SolanaAgentKit`](SolanaAgentKit.md)

#### Defined in

[agent/index.ts:39](https://github.com/scriptscrypt/solana-agent-kit/blob/4c8fad738fa9f59b8988f2e035ba86e7943593b8/src/agent/index.ts#L39)

## Methods

### requestFaucetFunds()

> **requestFaucetFunds**(): `Promise`\<`string`\>

#### Returns

`Promise`\<`string`\>

#### Defined in

[agent/index.ts:51](https://github.com/scriptscrypt/solana-agent-kit/blob/4c8fad738fa9f59b8988f2e035ba86e7943593b8/src/agent/index.ts#L51)

***

### deployToken()

> **deployToken**(`name`, `uri`, `symbol`, `decimals`, `initialSupply`?): `Promise`\<\{ `mint`: `PublicKey`; \}\>

#### Parameters

##### name

`string`

##### uri

`string`

##### symbol

`string`

##### decimals

`number` = `DEFAULT_OPTIONS.TOKEN_DECIMALS`

##### initialSupply?

`number`

#### Returns

`Promise`\<\{ `mint`: `PublicKey`; \}\>

#### Defined in

[agent/index.ts:55](https://github.com/scriptscrypt/solana-agent-kit/blob/4c8fad738fa9f59b8988f2e035ba86e7943593b8/src/agent/index.ts#L55)

***

### deployCollection()

> **deployCollection**(`options`): `Promise`\<[`CollectionDeployment`](../interfaces/CollectionDeployment.md)\>

#### Parameters

##### options

[`CollectionOptions`](../interfaces/CollectionOptions.md)

#### Returns

`Promise`\<[`CollectionDeployment`](../interfaces/CollectionDeployment.md)\>

#### Defined in

[agent/index.ts:65](https://github.com/scriptscrypt/solana-agent-kit/blob/4c8fad738fa9f59b8988f2e035ba86e7943593b8/src/agent/index.ts#L65)

***

### getBalance()

> **getBalance**(`token_address`?): `Promise`\<`null` \| `number`\>

#### Parameters

##### token\_address?

`PublicKey`

#### Returns

`Promise`\<`null` \| `number`\>

#### Defined in

[agent/index.ts:69](https://github.com/scriptscrypt/solana-agent-kit/blob/4c8fad738fa9f59b8988f2e035ba86e7943593b8/src/agent/index.ts#L69)

***

### mintNFT()

> **mintNFT**(`collectionMint`, `metadata`, `recipient`?): `Promise`\<[`MintCollectionNFTResponse`](../interfaces/MintCollectionNFTResponse.md)\>

#### Parameters

##### collectionMint

`PublicKey`

##### metadata

###### name

`string`

###### uri

`string`

###### sellerFeeBasisPoints

`number`

###### creators

`object`[]

##### recipient?

`PublicKey`

#### Returns

`Promise`\<[`MintCollectionNFTResponse`](../interfaces/MintCollectionNFTResponse.md)\>

#### Defined in

[agent/index.ts:73](https://github.com/scriptscrypt/solana-agent-kit/blob/4c8fad738fa9f59b8988f2e035ba86e7943593b8/src/agent/index.ts#L73)

***

### transfer()

> **transfer**(`to`, `amount`, `mint`?): `Promise`\<`string`\>

#### Parameters

##### to

`PublicKey`

##### amount

`number`

##### mint?

`PublicKey`

#### Returns

`Promise`\<`string`\>

#### Defined in

[agent/index.ts:81](https://github.com/scriptscrypt/solana-agent-kit/blob/4c8fad738fa9f59b8988f2e035ba86e7943593b8/src/agent/index.ts#L81)

***

### registerDomain()

> **registerDomain**(`name`, `spaceKB`?): `Promise`\<`string`\>

#### Parameters

##### name

`string`

##### spaceKB?

`number`

#### Returns

`Promise`\<`string`\>

#### Defined in

[agent/index.ts:85](https://github.com/scriptscrypt/solana-agent-kit/blob/4c8fad738fa9f59b8988f2e035ba86e7943593b8/src/agent/index.ts#L85)

***

### resolveSolDomain()

> **resolveSolDomain**(`domain`): `Promise`\<`PublicKey`\>

#### Parameters

##### domain

`string`

#### Returns

`Promise`\<`PublicKey`\>

#### Defined in

[agent/index.ts:89](https://github.com/scriptscrypt/solana-agent-kit/blob/4c8fad738fa9f59b8988f2e035ba86e7943593b8/src/agent/index.ts#L89)

***

### getPrimaryDomain()

> **getPrimaryDomain**(`account`): `Promise`\<`string`\>

#### Parameters

##### account

`PublicKey`

#### Returns

`Promise`\<`string`\>

#### Defined in

[agent/index.ts:93](https://github.com/scriptscrypt/solana-agent-kit/blob/4c8fad738fa9f59b8988f2e035ba86e7943593b8/src/agent/index.ts#L93)

***

### trade()

> **trade**(`outputMint`, `inputAmount`, `inputMint`?, `slippageBps`?): `Promise`\<`string`\>

#### Parameters

##### outputMint

`PublicKey`

##### inputAmount

`number`

##### inputMint?

`PublicKey`

##### slippageBps?

`number` = `DEFAULT_OPTIONS.SLIPPAGE_BPS`

#### Returns

`Promise`\<`string`\>

#### Defined in

[agent/index.ts:97](https://github.com/scriptscrypt/solana-agent-kit/blob/4c8fad738fa9f59b8988f2e035ba86e7943593b8/src/agent/index.ts#L97)

***

### lendAssets()

> **lendAssets**(`amount`): `Promise`\<`string`\>

#### Parameters

##### amount

`number`

#### Returns

`Promise`\<`string`\>

#### Defined in

[agent/index.ts:106](https://github.com/scriptscrypt/solana-agent-kit/blob/4c8fad738fa9f59b8988f2e035ba86e7943593b8/src/agent/index.ts#L106)

***

### getTPS()

> **getTPS**(): `Promise`\<`number`\>

#### Returns

`Promise`\<`number`\>

#### Defined in

[agent/index.ts:110](https://github.com/scriptscrypt/solana-agent-kit/blob/4c8fad738fa9f59b8988f2e035ba86e7943593b8/src/agent/index.ts#L110)

***

### getTokenDataByAddress()

> **getTokenDataByAddress**(`mint`): `Promise`\<`undefined` \| [`JupiterTokenData`](../interfaces/JupiterTokenData.md)\>

#### Parameters

##### mint

`string`

#### Returns

`Promise`\<`undefined` \| [`JupiterTokenData`](../interfaces/JupiterTokenData.md)\>

#### Defined in

[agent/index.ts:114](https://github.com/scriptscrypt/solana-agent-kit/blob/4c8fad738fa9f59b8988f2e035ba86e7943593b8/src/agent/index.ts#L114)

***

### getTokenDataByTicker()

> **getTokenDataByTicker**(`ticker`): `Promise`\<`undefined` \| [`JupiterTokenData`](../interfaces/JupiterTokenData.md)\>

#### Parameters

##### ticker

`string`

#### Returns

`Promise`\<`undefined` \| [`JupiterTokenData`](../interfaces/JupiterTokenData.md)\>

#### Defined in

[agent/index.ts:118](https://github.com/scriptscrypt/solana-agent-kit/blob/4c8fad738fa9f59b8988f2e035ba86e7943593b8/src/agent/index.ts#L118)

***

### launchPumpFunToken()

> **launchPumpFunToken**(`tokenName`, `tokenTicker`, `description`, `imageUrl`, `options`?): `Promise`\<\{ `signature`: `string`; `mint`: `string`; `metadataUri`: `any`; \}\>

#### Parameters

##### tokenName

`string`

##### tokenTicker

`string`

##### description

`string`

##### imageUrl

`string`

##### options?

[`PumpFunTokenOptions`](../interfaces/PumpFunTokenOptions.md)

#### Returns

`Promise`\<\{ `signature`: `string`; `mint`: `string`; `metadataUri`: `any`; \}\>

#### Defined in

[agent/index.ts:122](https://github.com/scriptscrypt/solana-agent-kit/blob/4c8fad738fa9f59b8988f2e035ba86e7943593b8/src/agent/index.ts#L122)

***

### stake()

> **stake**(`amount`): `Promise`\<`string`\>

#### Parameters

##### amount

`number`

#### Returns

`Promise`\<`string`\>

#### Defined in

[agent/index.ts:139](https://github.com/scriptscrypt/solana-agent-kit/blob/4c8fad738fa9f59b8988f2e035ba86e7943593b8/src/agent/index.ts#L139)

## Properties

### connection

> **connection**: `Connection`

Solana RPC connection

#### Defined in

[agent/index.ts:34](https://github.com/scriptscrypt/solana-agent-kit/blob/4c8fad738fa9f59b8988f2e035ba86e7943593b8/src/agent/index.ts#L34)

***

### wallet

> **wallet**: `Keypair`

Wallet keypair for signing transactions

#### Defined in

[agent/index.ts:35](https://github.com/scriptscrypt/solana-agent-kit/blob/4c8fad738fa9f59b8988f2e035ba86e7943593b8/src/agent/index.ts#L35)

***

### wallet\_address

> **wallet\_address**: `PublicKey`

Public key of the wallet

#### Defined in

[agent/index.ts:36](https://github.com/scriptscrypt/solana-agent-kit/blob/4c8fad738fa9f59b8988f2e035ba86e7943593b8/src/agent/index.ts#L36)

***

### openai\_api\_key

> **openai\_api\_key**: `string`

#### Defined in

[agent/index.ts:37](https://github.com/scriptscrypt/solana-agent-kit/blob/4c8fad738fa9f59b8988f2e035ba86e7943593b8/src/agent/index.ts#L37)