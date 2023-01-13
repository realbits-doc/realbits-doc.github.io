---
title: How to rent
pagenum: 2
---

### Process

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
	NFT Owner->>Rent Market: Deposit
	Rent Market->>User: Rent
	User->>Rent Market: Rent Fee
	Rent Market->>Rent Market: Share Fee
	Rent Market->>NFT Owner: Share Fee
	Rent Market->>Service Owner: Share Fee
```
