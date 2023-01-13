---
title: How to rent
pagenum: 2
---

### Total Process

In a NFT rent market ecosystem, there are three parties. They are content, service, and market owner. <span style="color:darkblue">**An NFT content owner registers their collection with a rent market**</span>. This is done with their collection contract address and collection information URL, which the rent market uses to display a title and image for the collection. As the user rents NFT content through the service, the owner's address is recorded, to whom the rent fee will be transferred. Additionally, <span style="color:darkblue">**the service owner is required to register the service owner's address and information URL**</span>. <span style="color:darkblue">**Market owner is running a NFT rent market.**</span> A portion of the rent fee will be transferred to the owner's address. And later, <span style="color:darkblue">**each party can withdraw their rent fee token from a rent market**</span>.

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
	Note over Service Owner,Rent Market: Service Register Process
	Service Owner->>Rent Market: Register service to rent market

	Note over NFT Owner,Rent Market: NFT Register Process
	NFT Owner->>Rent Market: Register NFT collection to rent market
	NFT Owner->>Rent Market: Register NFT data for renting

	Note over Service Owner,NFT Owner: Rent Process
	Renter->>Rent Market: Rent NFT by recording rent data with rent fee

	Note over Service Owner,NFT Owner: Share Process
	Rent Market->>Rent Market: Share rent fee for rent market portion
	Rent Market->>NFT Owner: Share rent fee for NFT owner portion
	Rent Market->>Service Owner: Share fee for service owner portion

	Note over Service Owner,NFT Owner: Withdraw Process
	Rent Market->>Rent Market: Withdraw token from rent market
	Rent Market->>NFT Owner: Withdraw token from NFT owner
	Rent Market->>Service Owner: Withdraw token from service owner
```

### How to register service

### How to register collection

### How to register NFT
