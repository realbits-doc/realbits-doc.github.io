---
title: rentMarket
pagenum: 3
---
# Solidity API

## rentMarket

rentMarket can be used for rentNFT market or promptNFT market.

_All function calls are currently being tested._

### tokenItMap

```solidity
struct tokenDataIterableMap.tokenDataMap tokenItMap
```

### collectionItMap

```solidity
struct collectionDataIterableMap.collectionDataMap collectionItMap
```

### serviceItMap

```solidity
struct serviceDataIterableMap.serviceDataMap serviceItMap
```

### registerDataItMap

```solidity
struct registerDataIterableMap.registerDataMap registerDataItMap
```

### rentDataItMap

```solidity
struct rentDataIterableMap.rentDataMap rentDataItMap
```

### pendingRentFeeMap

```solidity
struct pendingRentFeeIterableMap.pendingRentFeeMap pendingRentFeeMap
```

### accountBalanceItMap

```solidity
struct accountBalanceIterableMap.accountBalanceMap accountBalanceItMap
```

### exclusive

```solidity
bool exclusive
```

### constructor

```solidity
constructor(bool exclusive_) public
```

### Fallback

```solidity
event Fallback(address sender)
```

### fallback

```solidity
fallback() external payable
```

### Receive

```solidity
event Receive(address sender, uint256 value)
```

### receive

```solidity
receive() external payable
```

### RegisterToken

```solidity
event RegisterToken(address tokenAddress, string name)
```

### UnregisterToken

```solidity
event UnregisterToken(address tokenAddress, string name)
```

### getAllToken

```solidity
function getAllToken() public view returns (struct tokenDataIterableMap.tokenData[])
```

Return all token data as array type

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | struct tokenDataIterableMap.tokenData[] | All token data as array |

### registerToken

```solidity
function registerToken(address tokenAddress, string name) public returns (bool success)
```

Register token

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| tokenAddress | address | token address |
| name | string |  |

### unregisterToken

```solidity
function unregisterToken(address tokenAddress) public returns (bool success)
```

Unregister token data

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| tokenAddress | address | token address |

### RegisterCollection

```solidity
event RegisterCollection(address collectionAddress, string uri)
```

### UnregisterCollection

```solidity
event UnregisterCollection(address collectionAddress, string uri)
```

### getAllCollection

```solidity
function getAllCollection() public view returns (struct collectionDataIterableMap.collectionData[])
```

Return all collection data as array type

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | struct collectionDataIterableMap.collectionData[] | All collection data as array |

### getCollection

```solidity
function getCollection(address collectionAddress) public view returns (struct collectionDataIterableMap.collectionData)
```

Return matched collection data with collection address.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| collectionAddress | address | collection address |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | struct collectionDataIterableMap.collectionData | Matched collection data |

### registerCollection

```solidity
function registerCollection(address collectionAddress, string uri) public returns (bool success)
```

Register collection

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| collectionAddress | address | collection address |
| uri | string | collection metadata uri |

### unregisterCollection

```solidity
function unregisterCollection(address collectionAddress) public returns (bool success)
```

Unregister collection data

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| collectionAddress | address | collection address |

### RegisterService

```solidity
event RegisterService(address serviceAddress, string uri)
```

### UnregisterService

```solidity
event UnregisterService(address serviceAddress, string uri)
```

### getAllService

```solidity
function getAllService() public view returns (struct serviceDataIterableMap.serviceData[])
```

Return all service data as array type

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | struct serviceDataIterableMap.serviceData[] | All service data as array |

### getService

```solidity
function getService(address serviceAddress) public view returns (struct serviceDataIterableMap.serviceData)
```

Return matched service data with service address.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| serviceAddress | address | service address |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | struct serviceDataIterableMap.serviceData | Matched service data |

### registerService

```solidity
function registerService(address serviceAddress, string uri) public returns (bool success)
```

Register service

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| serviceAddress | address | service address |
| uri | string | service metadata uri |

### unregisterService

```solidity
function unregisterService(address serviceAddress) public returns (bool success)
```

Unregister service data

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| serviceAddress | address | service address |

### RegisterNFT

```solidity
event RegisterNFT(address nftAddress, uint256 tokenId, uint256 rentFee, uint256 rentDuration, address NFTOwnerAddress)
```

### ChangeNFT

```solidity
event ChangeNFT(address nftAddress, uint256 tokenId, uint256 rentFee, address feeTokenAddress, uint256 rentFeeByToken, uint256 rentDuration, address NFTOwnerAddress, address changerAddress)
```

### UnregisterNFT

```solidity
event UnregisterNFT(address nftAddress, uint256 tokenId, uint256 rentFee, address feeTokenAddress, uint256 rentFeeByToken, uint256 rentDuration, address NFTOwnerAddress, address UnregisterAddress)
```

### getAllRegisterData

```solidity
function getAllRegisterData() public view returns (struct registerDataIterableMap.registerData[])
```

Return all registered data as array type

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | struct registerDataIterableMap.registerData[] | All registered data as array |

### getRegisterData

```solidity
function getRegisterData(address nftAddress, uint256 tokenId) public view returns (struct registerDataIterableMap.registerData)
```

Return matched registered data with NFT address and token ID

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| nftAddress | address | NFT address |
| tokenId | uint256 | token ID |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | struct registerDataIterableMap.registerData | Matched registered data |

### registerNFT

```solidity
function registerNFT(address nftAddress, uint256 tokenId) public returns (bool success)
```

Request to register NFT. Sender should be an owner of NFT and NFT collection is already registered.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| nftAddress | address | NFT address |
| tokenId | uint256 | NFT token ID |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| success | bool | or failture (bool). |

### changeNFT

```solidity
function changeNFT(address nftAddress, uint256 tokenId, uint256 rentFee, address feeTokenAddress, uint256 rentFeeByToken, uint256 rentDuration) public returns (bool success)
```

Change NFT data

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| nftAddress | address | NFT address |
| tokenId | uint256 | NFT token ID |
| rentFee | uint256 | rent fee |
| feeTokenAddress | address | fee token address |
| rentFeeByToken | uint256 | rent fee by token |
| rentDuration | uint256 | rent duration |

### unregisterNFT

```solidity
function unregisterNFT(address nftAddress, uint256 tokenId) public returns (bool success)
```

Unregister NFT data

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| nftAddress | address | NFT address |
| tokenId | uint256 | NFT token ID |

### RentNFT

```solidity
event RentNFT(address nftAddress, uint256 tokenId, uint256 rentFee, address feeTokenAddress, uint256 rentFeeByToken, bool isRentByToken, uint256 rentDuration, address renterAddress, address renteeAddress, address serviceAddress, uint256 rentStartTimestamp)
```

### UnrentNFT

```solidity
event UnrentNFT(address nftAddress, uint256 tokenId, uint256 rentFee, address feeTokenAddress, uint256 rentFeeByToken, bool isRentByToken, uint256 rentDuration, address renterAddress, address renteeAddress, address serviceAddress, uint256 rentStartTimestamp)
```

### getAllRentData

```solidity
function getAllRentData() public view returns (struct rentDataIterableMap.rentData[])
```

Return the all rented NFT data.

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | struct rentDataIterableMap.rentData[] | All rented NFT data array. |

### getRentData

```solidity
function getRentData(address nftAddress, uint256 tokenId) public view returns (struct rentDataIterableMap.rentData)
```

Return matched rented data with NFT address and token ID

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| nftAddress | address | NFT address |
| tokenId | uint256 | token ID |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | struct rentDataIterableMap.rentData | Matched rented data |

### rentNFT

```solidity
function rentNFT(address nftAddress, uint256 tokenId, address serviceAddress) public payable returns (bool success)
```

Rent NFT

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| nftAddress | address | NFT address |
| tokenId | uint256 | NFT token ID |
| serviceAddress | address | service address |

### rentNFTByToken

```solidity
function rentNFTByToken(address nftAddress, uint256 tokenId, address serviceAddress) public payable returns (bool success)
```

Rent NFT by token

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| nftAddress | address | NFT address |
| tokenId | uint256 | NFT token ID |
| serviceAddress | address | service address |

### unrentNFT

```solidity
function unrentNFT(address nftAddress, uint256 tokenId) public returns (bool success)
```

Unrent NFT

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| nftAddress | address | NFT address |
| tokenId | uint256 | NFT token ID |

### SettleRentData

```solidity
event SettleRentData(address nftAddress, uint256 tokenId, uint256 rentFee, address feeTokenAddress, uint256 rentFeeByToken, bool isRentByToken, uint256 rentDuration, address renterAddress, address renteeAddress, address serviceAddress, uint256 rentStartTimestamp)
```

### settleRentData

```solidity
function settleRentData(address nftAddress, uint256 tokenId) public returns (bool success)
```

### WithdrawMyBalance

```solidity
event WithdrawMyBalance(address recipient, address tokenAddress, uint256 amount)
```

### getAllPendingRentFee

```solidity
function getAllPendingRentFee() public view returns (struct pendingRentFeeIterableMap.pendingRentFee[])
```

Return all pending rent fee data as array type

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | struct pendingRentFeeIterableMap.pendingRentFee[] | All pending rent fee data as array |

### getAllAccountBalance

```solidity
function getAllAccountBalance() public view returns (struct accountBalanceIterableMap.accountBalance[])
```

Return all account balance data as array type

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | struct accountBalanceIterableMap.accountBalance[] | All account balance data as array |

### withdrawMyBalance

```solidity
function withdrawMyBalance(address recipient, address tokenAddress) public payable returns (bool success)
```

### getMarketShareAddress

```solidity
function getMarketShareAddress() public view returns (address shareAddress)
```

### setMarketShareAddress

```solidity
function setMarketShareAddress(address shareAddress) public
```

### getMyBalance

```solidity
function getMyBalance(address tokenAddress) public view returns (uint256 balance)
```

### getFeeQuota

```solidity
function getFeeQuota() public view returns (uint256 renterFeeQuota, uint256 serviceFeeQuota, uint256 marketFeeQuota)
```

### setFeeQuota

```solidity
function setFeeQuota(uint256 renterFeeQuota, uint256 serviceFeeQuota, uint256 marketFeeQuota) public
```

### isOwnerOrRenter

```solidity
function isOwnerOrRenter(address account) public view returns (bool success)
```

