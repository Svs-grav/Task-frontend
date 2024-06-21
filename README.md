# Inforce Frontend Test Task

## The Stack

* JavaScript / TypeScript
* React
* Your Cache Manager/ Query library of choice
* Vanilla CSS or your CSS library of choice

## Setup

`git clone https://github.com/Svs-grav/inforce-frontend-test`
`cd inforce-frontend-test`
`npm i`
`npx json-server db.json`
`npm run dev`

## Requirements

#### Product List View 

1. Display the product list
2. DIsplay an `Add` button
	1. The `Add` button should open a modal with input fields for each `Product` schema property
	2. Inside the modal, display the `Save` and `Cancel` buttons.
	3. The `Cancel` button should prompt the user to confirm or cancel the destructive action
3. The product list must be sorted by `name` by default with a dropdown option to sort by `count`
4. Clicking on the product card should take the user to the individual product view 

#### Individual Product View

1. The product details and comments should be displayed here
2. An `Edit` button should open a modal allowing the user to update the selected product
3. A `Delete` button should prompt the user to confirm or cancel the destructive action
4. Display buttons to add and remove comments
5. A button must be displayed to take the user back to the product list view

## Guidelines 

* Spend no longer than 5 hours to build as many features as you can
* Prioritize feature and code quality over quantity
* `json-server` - https://www.npmjs.com/package/json-server must be used to read and write mock data to `db.json`:
* Push the finished project to your own repository

## Data Interfaces 

```ts
interface Product {
	"id": number,
	"imageUrl": string,
	"name": string,
	"count": number,
	"size": {
		"width": number,
		"height": number,
	},
	"weight": string,
}

interface Comment {
	"id": number,
	"productId": number,
	"description": string,
	"date": Date
}
```
