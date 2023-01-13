---
title: promptNFT
pagenum: 2
---
# Solidity API

## promptNFT

promptNFT can be used for saving prompt with NFT.

_All functions are currently being tested._

### encryptData

```solidity
struct encryptData {
  string version;
  string ephemPublicKey;
  string nonce;
  string ciphertext;
}
```

### nftTokenOwnerEncryptedPromptMap

```solidity
mapping(uint256 => struct promptNFT.encryptData) nftTokenOwnerEncryptedPromptMap
```

### nftContractOwnerEncryptedPromptMap

```solidity
mapping(uint256 => struct promptNFT.encryptData) nftContractOwnerEncryptedPromptMap
```

### constructor

```solidity
constructor(string name_, string symbol_, address payable rentMarketContractAddress_) public
```

### pause

```solidity
function pause() public
```

### unpause

```solidity
function unpause() public
```

### safeMint

```solidity
function safeMint(address to_, string uri_, struct promptNFT.encryptData tokenOwnerEncryptData_, struct promptNFT.encryptData contractOwnerEncryptData_) public returns (uint256)
```

### getContractOwnerPrompt

```solidity
function getContractOwnerPrompt(uint256 tokenId) public view returns (struct promptNFT.encryptData)
```

### getTokenOwnerPrompt

```solidity
function getTokenOwnerPrompt(uint256 tokenId) public view returns (struct promptNFT.encryptData)
```

### claimContractOwnerPrompt

```solidity
function claimContractOwnerPrompt(uint256 tokenId, struct promptNFT.encryptData contractOwnerEncryptData) public
```

### claimTokenOwnerPrompt

```solidity
function claimTokenOwnerPrompt(uint256 tokenId, struct promptNFT.encryptData tokenOwnerEncryptData) public
```

### tokenURI

```solidity
function tokenURI(uint256 tokenId) public view returns (string)
```

### _afterTokenTransfer

```solidity
function _afterTokenTransfer(address from, address to, uint256 tokenId, uint256 batchSize) internal
```

### _beforeTokenTransfer

```solidity
function _beforeTokenTransfer(address from, address to, uint256 tokenId, uint256 batchSize) internal
```

### _burn

```solidity
function _burn(uint256 tokenId) internal
```

### supportsInterface

```solidity
function supportsInterface(bytes4 interfaceId) public view returns (bool)
```

