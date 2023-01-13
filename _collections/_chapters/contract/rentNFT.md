---
title: rentNFT
pagenum: 1
---
# Solidity API

## rentNFT

You can use this contract for building and deploying NFT.

_All function calls are currently being tested._

### PAUSER_ROLE

```solidity
bytes32 PAUSER_ROLE
```

PAUSER_ROLE

_PAUSER_ROLE_

### MINTER_ROLE

```solidity
bytes32 MINTER_ROLE
```

MINTER_ROLE

_MINTER_ROLE_

### SETTER_ROLE

```solidity
bytes32 SETTER_ROLE
```

SETTER_ROLE

_SETTER_ROLE_

### constructor

```solidity
constructor(string name_, string symbol_, string baseTokenURI_) public
```

Constructor function

_Set base token URI and set each role of DEFAULT_ADMIN_ROLE, PAUSER_ROLE, MINTER_ROLE, and SETTER_ROLE_

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| name_ | string | NFT token name |
| symbol_ | string | NFT token symbol |
| baseTokenURI_ | string | base URI of NFT token |

### _baseURI

```solidity
function _baseURI() internal view returns (string)
```

Return base URI of token

_Override _baseURI function from ERC721.sol_

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | string | Base URI of token as string |

### setBaseURI

```solidity
function setBaseURI(string baseTokenURI_) public
```

Set base URI of token

_Only sender who has SETTER_ROLE can set base URI_

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| baseTokenURI_ | string | URI of token as string |

### getBaseURI

```solidity
function getBaseURI() public view returns (string)
```

Get base URI of token

_Return _baseTokenURI variable_

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | string | base URI of token as string |

### pause

```solidity
function pause() public
```

Pause this NFT

_Call _pause function in Pausible. Only sender who has PAUSER_ROLE can pause_

### unpause

```solidity
function unpause() public
```

Unpause this NFT

_Call _unpause function in Pausible. Only sender who has PAUSER_ROLE can pause_

### safeMint

```solidity
function safeMint(address to_) public
```

Mint NFT with auto incremented token ID

_After increasing token ID, call _safeMint function in ERC721.sol_

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| to_ | address | Receiver address who will receive minted NFT |

### safeMintAmount

```solidity
function safeMintAmount(address to_, uint256 amount_) public
```

Mint NFT by amount

_Loop calling _safeMint function by amount_

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| to_ | address | Receiver address who will receive minted NFT |
| amount_ | uint256 | Amount by which NFT will be minted |

### _beforeTokenTransfer

```solidity
function _beforeTokenTransfer(address from, address to, uint256 tokenId, uint256 batchSize) internal
```

Hook function which is called before token will be transfered

_Override this function from ERC721 and ERC721Enumerable. Only can be called when not paused_

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| from | address | from address which will send token |
| to | address | to address which will receive token |
| tokenId | uint256 | token ID which will be transfered |
| batchSize | uint256 | batch size |

### supportsInterface

```solidity
function supportsInterface(bytes4 interfaceId) public view returns (bool)
```

Check function where or not supporting a specific interface

_Override this function from ERC721 and ERC721Enumerable and AccessControl_

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| interfaceId | bytes4 | interface ID as bytes4 |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | bool | success or failure |

