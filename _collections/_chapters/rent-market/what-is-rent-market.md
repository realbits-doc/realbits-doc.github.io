---
title: What is a rent market?
pagenum: 1
---

### Background

<span style="color:darkgreen">**Rent Market**</span> is a smart contract that enables users to register NFT and <span style="color:darkgreen">**rent NFT**</span>.

### Problem

<span style="color:purple">**NFT**</span> is innately a limited resource item in the digital world. Due to this, <span style="color:purple">**its usage has been restricted to the owner**</span>. However, more people use a specific NFT, so the NFT has more utility.

### Solution

There are a few services that rent NFT to solve an NFT use case. But it is limited to the ERC-721 specification. As an example, in EIP-4907, if NFT is transferred, its renter will be removed, regardless of the renter's wishes. So, <span style="color:darkblue">**Realbits divides ownership of NFT and rentship of NFT**</span>. In other words, even if NFT has been transferred to another owner, its rent usage remains during its lease term.

```mermaid
flowchart TB
    id1(Owner)
    id2(Market)
    id3(Renter)

		subgraph NFT Owner
		id1-. Has a ownership of NFT .->id1
		end

		subgraph Rent Market
		id2-. Manage registered NFT data .->id2
		end

		subgraph NFT Renter
		id3-. Has a rentship of NFT .->id3
		end
```

### How to

When a NFT owner <span style="color:darkblue">**registers NFT to a rent market**</span>, NFT registration data is also recorded, such as rent fee or rent duration. Likewise, when someone <span style="color:darkblue">**rents NFT from a rent market**</span>, rent-metadata will be recorded, such as the rent fee and who is the owner and who is the renter of NFT. Upon termination of the rent, <span style="color:darkblue">**the rent fee will be shared among the NFT owner, the service owner, and the market owner**</span>. Distribution would be handled by calling the settlement function in a smart contract, which can be run by anyone with a gas fee. All rent-related data is stored in smart contracts that anyone can access. If you have a balance in the rental market, you can withdraw your fee.

```mermaid
%%{
  init: {
		"theme": "default",
		"themeVariables": {
				"fontFamily": "Helvetica"
		},
		"sequence": {
			"actorBkg": "#000000",
			"actorFontSize": "18",
			"actorFontFamily": "Helvetica",
			"actorFontWeight": 400,
			"noteFontFamily": "Helvetica",
			"noteFontSize": "12",
			"noteFontWeight": 200,
			"messageFontFamily": "Helvetica",
			"messageFontSize": "16",
			"messageFontWeight": 200,
			"showSequenceNumbers": true
  	},
		"journey": {
			"taskFontFamily": "Helvetica"
		}
  }
}%%

sequenceDiagram
    NFT Owner-->>NFT Owner: Has a ownership of NFT
    NFT Owner->>Rent Market: Register NFT data for renting usage
    NFT Renter->>Rent Market: Pay token and rent NFT usage
    Rent Market-->>NFT Renter: Rent NFT usage
```

### Think more

The rental process of NFT requires many options for running. Early on, each rent payment was to be made through MATIC in a polygon network. However, some users may want to use other ERC-20 tokens. In a beta service operation, rent duration is also a constant term, but some users prefer a flexible lease term.

### Build more

There is currently an optional part that can be minimized. However, as the renting operation continues, more flexible and optional management processes will be implemented.
