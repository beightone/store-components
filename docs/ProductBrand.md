📢 Use this project, [contribute](https://github.com/vtex-apps/store-components) to it or open issues to help evolve it using [Store Discussion](https://github.com/vtex-apps/store-discussion). 

# Product Brand

The `product-brand` is a VTEX block exported by the [Store Components app](https://vtex.io/docs/components/all/vtex.store-components/) that displays either the **name** or the **logo** of a **product's brand**.

![product-brand](https://user-images.githubusercontent.com/52087100/70259346-bb081f80-176c-11ea-84db-5785c45829ce.png)

## Configuration

1. Add the `vtex.store-components` app as a dependency in your theme's `manifest.json` file:

```json
  "dependencies: {
    "vtex.store-components": "3.x"
  }
```

2. Add the `product-brand` block to any block below `store.product` (product template). For example:

```json
  "store.product": {
    "children": [
      "flex-layout.row#product",
    ]
  },
  "flex-layout.row#product": {
    "children": [
      "product-brand"
    ]
  },
  "product-brand": {
    "props": {
      "displayMode": "text"
    }
  },
```

| Prop name | Type | Description | Default value | 
| :-------: | :--: | :---------: | ------------: |
| `brandName` | `string` | Brand name. If no value is declared, the brand name will be displayed according to the data fetched from the product context. | `undefined` | 
| `brandId` | `number` | Brand ID. If no value is declared, the brand ID will be displayed according to the data fetched from the product context. | `undefined` | 
| `displayMode` | `enum` | Defines how the product's brand should be displayed. Possible values are: `text` (displays the name of the product's brand) and `logo`. | `logo` | 
| `fallbackToText` | `boolean` | Whether the brand name should be displayed in scenarios where no logo image is found in the admin's Catalog (`true`) or not (`false`). *Caution*: This prop should only be used when the `displayMode` prop is set to `logo`. | `true` | 
| `height` | `number` | Desired height for the logo. *Caution*: This prop should only be used when the `displayMode` prop is set to `logo`. | `100` | 
| `excludeBrands` | `[string]` | List of brand names or brand IDs that should not be displayed by the Product Brand block. This prop is extremely useful to hide default or test brand names/logos on the store front. | `undefined` | 
| `logoWithLink` | `boolean` | Whether the brand logo should have a link that leads users to the brand's website (`true`) ou not (`false`). | `false` | 

## Customization 

In order to apply CSS customizations in this and other blocks, follow the instructions given in the recipe [Using CSS Handles for store customization](https://vtex.io/docs/recipes/style/using-css-handles-for-store-customization).

| CSS Handles |
| :---------: |
| `productBrandContainer` |
| `productBrandLogo` |
| `productBrandLogoLink` |
| `productBrandLogoSpacer` |
| `productBrandLogoWrapper` |
| `productBrandName` |
| `productBrandNameSpacer` |
