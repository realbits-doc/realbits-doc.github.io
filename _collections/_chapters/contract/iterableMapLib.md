---
title: iterableMapLib
pagenum: 1
---
# Solidity API

## pendingRentFeeIterableMap

### pendingRentFee

```solidity
struct pendingRentFee {
  address renterAddress;
  address serviceAddress;
  address feeTokenAddress;
  uint256 amount;
}
```

### pendingRentFeeEntry

```solidity
struct pendingRentFeeEntry {
  uint256 idx;
  struct pendingRentFeeIterableMap.pendingRentFee data;
}
```

### pendingRentFeeMap

```solidity
struct pendingRentFeeMap {
  mapping(string => struct pendingRentFeeIterableMap.pendingRentFeeEntry) data;
  string[] keys;
}
```

### encodeKey

```solidity
function encodeKey(address renterAddress, address serviceAddress, address feeTokenAddress) public pure returns (string)
```

### decodeKey

```solidity
function decodeKey(struct pendingRentFeeIterableMap.pendingRentFeeMap self, string key) public view returns (address renterAddress, address serviceAddress, address feeTokenAddress)
```

### insert

```solidity
function insert(struct pendingRentFeeIterableMap.pendingRentFeeMap self, address renterAddress, address serviceAddress, address feeTokenAddress, uint256 amount) public returns (bool success)
```

### add

```solidity
function add(struct pendingRentFeeIterableMap.pendingRentFeeMap self, address renterAddress, address serviceAddress, address feeTokenAddress, uint256 amount) public returns (bool success)
```

### sub

```solidity
function sub(struct pendingRentFeeIterableMap.pendingRentFeeMap self, address renterAddress, address serviceAddress, address feeTokenAddress, uint256 amount) public returns (bool success)
```

### remove

```solidity
function remove(struct pendingRentFeeIterableMap.pendingRentFeeMap self, address renterAddress, address serviceAddress, address feeTokenAddress) public returns (bool success)
```

### contains

```solidity
function contains(struct pendingRentFeeIterableMap.pendingRentFeeMap self, address renterAddress, address serviceAddress, address feeTokenAddress) public view returns (bool exists)
```

### size

```solidity
function size(struct pendingRentFeeIterableMap.pendingRentFeeMap self) public view returns (uint256)
```

### getAmount

```solidity
function getAmount(struct pendingRentFeeIterableMap.pendingRentFeeMap self, address renterAddress, address serviceAddress, address feeTokenAddress) public view returns (uint256)
```

### getByAddress

```solidity
function getByAddress(struct pendingRentFeeIterableMap.pendingRentFeeMap self, address renterAddress, address serviceAddress, address feeTokenAddress) public view returns (struct pendingRentFeeIterableMap.pendingRentFee)
```

### getKeyByIndex

```solidity
function getKeyByIndex(struct pendingRentFeeIterableMap.pendingRentFeeMap self, uint256 idx) public view returns (string)
```

### getDataByIndex

```solidity
function getDataByIndex(struct pendingRentFeeIterableMap.pendingRentFeeMap self, uint256 idx) public view returns (struct pendingRentFeeIterableMap.pendingRentFee)
```

## accountBalanceIterableMap

### accountBalance

```solidity
struct accountBalance {
  address accountAddress;
  address tokenAddress;
  uint256 amount;
}
```

### accountBalanceEntry

```solidity
struct accountBalanceEntry {
  uint256 idx;
  struct accountBalanceIterableMap.accountBalance data;
}
```

### accountBalanceMap

```solidity
struct accountBalanceMap {
  mapping(string => struct accountBalanceIterableMap.accountBalanceEntry) data;
  string[] keys;
}
```

### encodeKey

```solidity
function encodeKey(address accountAddress, address tokenAddress) public pure returns (string)
```

### decodeKey

```solidity
function decodeKey(struct accountBalanceIterableMap.accountBalanceMap self, string key) public view returns (address accountAddress, address tokenAddress)
```

### add

```solidity
function add(struct accountBalanceIterableMap.accountBalanceMap self, address accountAddress, address tokenAddress, uint256 amount) public returns (bool success)
```

### insert

```solidity
function insert(struct accountBalanceIterableMap.accountBalanceMap self, address accountAddress, address tokenAddress, uint256 amount) public returns (bool success)
```

### remove

```solidity
function remove(struct accountBalanceIterableMap.accountBalanceMap self, address accountAddress, address tokenAddress) public returns (bool success)
```

### contains

```solidity
function contains(struct accountBalanceIterableMap.accountBalanceMap self, address accountAddress, address tokenAddress) public view returns (bool exists)
```

### size

```solidity
function size(struct accountBalanceIterableMap.accountBalanceMap self) public view returns (uint256)
```

### getAmount

```solidity
function getAmount(struct accountBalanceIterableMap.accountBalanceMap self, address accountAddress, address tokenAddress) public view returns (uint256)
```

### getByAddress

```solidity
function getByAddress(struct accountBalanceIterableMap.accountBalanceMap self, address accountAddress, address tokenAddress) public view returns (struct accountBalanceIterableMap.accountBalance)
```

### getKeyByIndex

```solidity
function getKeyByIndex(struct accountBalanceIterableMap.accountBalanceMap self, uint256 idx) public view returns (string)
```

### getDataByIndex

```solidity
function getDataByIndex(struct accountBalanceIterableMap.accountBalanceMap self, uint256 idx) public view returns (struct accountBalanceIterableMap.accountBalance)
```

## tokenDataIterableMap

### tokenData

```solidity
struct tokenData {
  address tokenAddress;
  string name;
}
```

### tokenDataEntry

```solidity
struct tokenDataEntry {
  uint256 idx;
  struct tokenDataIterableMap.tokenData data;
}
```

### tokenDataMap

```solidity
struct tokenDataMap {
  mapping(string => struct tokenDataIterableMap.tokenDataEntry) data;
  string[] keys;
}
```

### encodeKey

```solidity
function encodeKey(address tokenAddress) public pure returns (string)
```

### decodeKey

```solidity
function decodeKey(struct tokenDataIterableMap.tokenDataMap self, string key) public view returns (address tokenAddress)
```

### insert

```solidity
function insert(struct tokenDataIterableMap.tokenDataMap self, address tokenAddress, string name) public returns (bool success)
```

### remove

```solidity
function remove(struct tokenDataIterableMap.tokenDataMap self, address tokenAddress) public returns (bool success)
```

### contains

```solidity
function contains(struct tokenDataIterableMap.tokenDataMap self, address tokenAddress) public view returns (bool exists)
```

### size

```solidity
function size(struct tokenDataIterableMap.tokenDataMap self) public view returns (uint256)
```

### getName

```solidity
function getName(struct tokenDataIterableMap.tokenDataMap self, address tokenAddress) public view returns (string)
```

### getByAddress

```solidity
function getByAddress(struct tokenDataIterableMap.tokenDataMap self, address tokenAddress) public view returns (struct tokenDataIterableMap.tokenData)
```

### getKeyByIndex

```solidity
function getKeyByIndex(struct tokenDataIterableMap.tokenDataMap self, uint256 idx) public view returns (string)
```

### getDataByIndex

```solidity
function getDataByIndex(struct tokenDataIterableMap.tokenDataMap self, uint256 idx) public view returns (struct tokenDataIterableMap.tokenData)
```

## collectionDataIterableMap

### collectionData

```solidity
struct collectionData {
  address collectionAddress;
  string uri;
}
```

### collectionDataEntry

```solidity
struct collectionDataEntry {
  uint256 idx;
  struct collectionDataIterableMap.collectionData data;
}
```

### collectionDataMap

```solidity
struct collectionDataMap {
  mapping(string => struct collectionDataIterableMap.collectionDataEntry) data;
  string[] keys;
}
```

### encodeKey

```solidity
function encodeKey(address collectionAddress) public pure returns (string)
```

### decodeKey

```solidity
function decodeKey(struct collectionDataIterableMap.collectionDataMap self, string key) public view returns (address collectionAddress)
```

### insert

```solidity
function insert(struct collectionDataIterableMap.collectionDataMap self, address collectionAddress, string uri) public returns (bool success)
```

### remove

```solidity
function remove(struct collectionDataIterableMap.collectionDataMap self, address collectionAddress) public returns (bool success)
```

### contains

```solidity
function contains(struct collectionDataIterableMap.collectionDataMap self, address collectionAddress) public view returns (bool exists)
```

### size

```solidity
function size(struct collectionDataIterableMap.collectionDataMap self) public view returns (uint256)
```

### getUri

```solidity
function getUri(struct collectionDataIterableMap.collectionDataMap self, address collectionAddress) public view returns (string)
```

### getByAddress

```solidity
function getByAddress(struct collectionDataIterableMap.collectionDataMap self, address collectionAddress) public view returns (struct collectionDataIterableMap.collectionData)
```

### getKeyByIndex

```solidity
function getKeyByIndex(struct collectionDataIterableMap.collectionDataMap self, uint256 idx) public view returns (string)
```

### getDataByIndex

```solidity
function getDataByIndex(struct collectionDataIterableMap.collectionDataMap self, uint256 idx) public view returns (struct collectionDataIterableMap.collectionData)
```

## serviceDataIterableMap

### serviceData

```solidity
struct serviceData {
  address serviceAddress;
  string uri;
}
```

### serviceDataEntry

```solidity
struct serviceDataEntry {
  uint256 idx;
  struct serviceDataIterableMap.serviceData data;
}
```

### serviceDataMap

```solidity
struct serviceDataMap {
  mapping(string => struct serviceDataIterableMap.serviceDataEntry) data;
  string[] keys;
}
```

### encodeKey

```solidity
function encodeKey(address serviceAddress) public pure returns (string)
```

### decodeKey

```solidity
function decodeKey(struct serviceDataIterableMap.serviceDataMap self, string key) public view returns (address serviceAddress)
```

### insert

```solidity
function insert(struct serviceDataIterableMap.serviceDataMap self, address serviceAddress, string uri) public returns (bool success)
```

### remove

```solidity
function remove(struct serviceDataIterableMap.serviceDataMap self, address serviceAddress) public returns (bool success)
```

### contains

```solidity
function contains(struct serviceDataIterableMap.serviceDataMap self, address serviceAddress) public view returns (bool exists)
```

### size

```solidity
function size(struct serviceDataIterableMap.serviceDataMap self) public view returns (uint256)
```

### getUri

```solidity
function getUri(struct serviceDataIterableMap.serviceDataMap self, address serviceAddress) public view returns (string)
```

### getByAddress

```solidity
function getByAddress(struct serviceDataIterableMap.serviceDataMap self, address serviceAddress) public view returns (struct serviceDataIterableMap.serviceData)
```

### getKeyByIndex

```solidity
function getKeyByIndex(struct serviceDataIterableMap.serviceDataMap self, uint256 idx) public view returns (string)
```

### getDataByIndex

```solidity
function getDataByIndex(struct serviceDataIterableMap.serviceDataMap self, uint256 idx) public view returns (struct serviceDataIterableMap.serviceData)
```

## requestDataIterableMap

### requestData

```solidity
struct requestData {
  address nftAddress;
  uint256 tokenId;
}
```

### requestDataEntry

```solidity
struct requestDataEntry {
  uint256 idx;
  struct requestDataIterableMap.requestData data;
}
```

### requestDataMap

```solidity
struct requestDataMap {
  mapping(string => struct requestDataIterableMap.requestDataEntry) data;
  string[] keys;
}
```

### encodeKey

```solidity
function encodeKey(address nftAddress, uint256 tokenId) public pure returns (string)
```

### decodeKey

```solidity
function decodeKey(struct requestDataIterableMap.requestDataMap self, string key) public view returns (address nftAddress, uint256 tokenId)
```

### insert

```solidity
function insert(struct requestDataIterableMap.requestDataMap self, address nftAddress, uint256 tokenId) public returns (bool success)
```

### remove

```solidity
function remove(struct requestDataIterableMap.requestDataMap self, address nftAddress, uint256 tokenId) public returns (bool success)
```

### contains

```solidity
function contains(struct requestDataIterableMap.requestDataMap self, address nftAddress, uint256 tokenId) public view returns (bool exists)
```

### size

```solidity
function size(struct requestDataIterableMap.requestDataMap self) public view returns (uint256)
```

### getByNFT

```solidity
function getByNFT(struct requestDataIterableMap.requestDataMap self, address nftAddress, uint256 tokenId) public view returns (struct requestDataIterableMap.requestData)
```

### getKeyByIndex

```solidity
function getKeyByIndex(struct requestDataIterableMap.requestDataMap self, uint256 idx) public view returns (string)
```

### getDataByIndex

```solidity
function getDataByIndex(struct requestDataIterableMap.requestDataMap self, uint256 idx) public view returns (struct requestDataIterableMap.requestData)
```

## registerDataIterableMap

### registerData

```solidity
struct registerData {
  address nftAddress;
  uint256 tokenId;
  uint256 rentFee;
  address feeTokenAddress;
  uint256 rentFeeByToken;
  uint256 rentDuration;
}
```

### registerDataEntry

```solidity
struct registerDataEntry {
  uint256 idx;
  struct registerDataIterableMap.registerData data;
}
```

### registerDataMap

```solidity
struct registerDataMap {
  mapping(string => struct registerDataIterableMap.registerDataEntry) data;
  string[] keys;
}
```

### encodeKey

```solidity
function encodeKey(address nftAddress, uint256 tokenId) public pure returns (string)
```

### decodeKey

```solidity
function decodeKey(struct registerDataIterableMap.registerDataMap self, string key) public view returns (address nftAddress, uint256 tokenId)
```

### insert

```solidity
function insert(struct registerDataIterableMap.registerDataMap self, address nftAddress, uint256 tokenId, uint256 rentFee, address feeTokenAddress, uint256 rentFeeByToken, uint256 rentDuration) public returns (bool success)
```

### set

```solidity
function set(struct registerDataIterableMap.registerDataMap self, address nftAddress, uint256 tokenId, uint256 rentFee, address feeTokenAddress, uint256 rentFeeByToken, uint256 rentDuration) public returns (bool success)
```

### remove

```solidity
function remove(struct registerDataIterableMap.registerDataMap self, address nftAddress, uint256 tokenId) public returns (bool success)
```

### contains

```solidity
function contains(struct registerDataIterableMap.registerDataMap self, address nftAddress, uint256 tokenId) public view returns (bool exists)
```

### size

```solidity
function size(struct registerDataIterableMap.registerDataMap self) public view returns (uint256)
```

### getByNFT

```solidity
function getByNFT(struct registerDataIterableMap.registerDataMap self, address nftAddress, uint256 tokenId) public view returns (struct registerDataIterableMap.registerData)
```

### getKeyByIndex

```solidity
function getKeyByIndex(struct registerDataIterableMap.registerDataMap self, uint256 idx) public view returns (string)
```

### getDataByIndex

```solidity
function getDataByIndex(struct registerDataIterableMap.registerDataMap self, uint256 idx) public view returns (struct registerDataIterableMap.registerData)
```

## rentDataIterableMap

### rentData

```solidity
struct rentData {
  address nftAddress;
  uint256 tokenId;
  uint256 rentFee;
  address feeTokenAddress;
  uint256 rentFeeByToken;
  bool isRentByToken;
  uint256 rentDuration;
  address renterAddress;
  address renteeAddress;
  address serviceAddress;
  uint256 rentStartTimestamp;
}
```

### rentDataEntry

```solidity
struct rentDataEntry {
  uint256 idx;
  struct rentDataIterableMap.rentData data;
}
```

### rentDataMap

```solidity
struct rentDataMap {
  mapping(string => struct rentDataIterableMap.rentDataEntry) data;
  string[] keys;
}
```

### encodeKey

```solidity
function encodeKey(address nftAddress, uint256 tokenId) public pure returns (string)
```

### decodeKey

```solidity
function decodeKey(struct rentDataIterableMap.rentDataMap self, string key) public view returns (address nftAddress, uint256 tokenId)
```

### insert

```solidity
function insert(struct rentDataIterableMap.rentDataMap self, struct rentDataIterableMap.rentData data) public returns (bool success)
```

### remove

```solidity
function remove(struct rentDataIterableMap.rentDataMap self, address nftAddress, uint256 tokenId) public returns (bool success)
```

### contains

```solidity
function contains(struct rentDataIterableMap.rentDataMap self, address nftAddress, uint256 tokenId) public view returns (bool exists)
```

### size

```solidity
function size(struct rentDataIterableMap.rentDataMap self) public view returns (uint256)
```

### getByNFT

```solidity
function getByNFT(struct rentDataIterableMap.rentDataMap self, address nftAddress, uint256 tokenId) public view returns (struct rentDataIterableMap.rentData)
```

### getKeyByIndex

```solidity
function getKeyByIndex(struct rentDataIterableMap.rentDataMap self, uint256 idx) public view returns (string)
```

### getDataByIndex

```solidity
function getDataByIndex(struct rentDataIterableMap.rentDataMap self, uint256 idx) public view returns (struct rentDataIterableMap.rentData)
```

