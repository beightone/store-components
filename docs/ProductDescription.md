📢 Use this project, [contribute](https://github.com/vtex-apps/store-components) to it or open issues to help evolve it using [Store Discussion](https://github.com/vtex-apps/store-discussion). 

# Product Description

The `product-description` is a VTEX block exported by the [Store Components app](https://vtex.io/docs/components/all/vtex.store-components/) that displays the description of a product.

## Configuration

1. Add the `vtex.store-components` app as a dependency in your theme's `manifest.json` file:

```json
  "dependencies": {
    "vtex.store-components": "2.x"
  }
```

2. Add the `product-description` block to any block below `store.product`(product template). For example:

```json
  "store.product": {
    "children": [
      "flex-layout.row#product",
    ]
  },
  "flex-layout.row#product": {
    "children": [
      "product-description"
    ]
  }
```

| Prop name | Type | Description | Default value |
| :-------: | :--: | :---------: | :-----------: |
| `title` | `string` | Custom title for the description section. | `undefined` |
| `collapseContent` | `boolean` | Whether the description should always be fully displayed, regardless of its number of characters (`true`) or not (`false`) i.e. it should collapse and display a `Show More` button instead. | `true` |

## Customization

In order to apply CSS customizations in this and other blocks, follow the instructions given in the recipe on [Using CSS Handles for store customization](https://vtex.io/docs/recipes/style/using-css-handles-for-store-customization).

| CSS Handles |
| :---------: |
| `productDescriptionContainer` |
| `productDescriptionTitle`     |
| `productDescriptionText`      |
