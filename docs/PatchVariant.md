# ConvictionalSeller::PatchVariant

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **_id** | **String** | The Convictional ID of the variant. Immutable. Must be included when updating a variant using PATCH /products/{productId}. Excluding this field will create a new variant. | [optional] |
| **barcode** | **String** | The barcode of the variant | [optional] |
| **barcode_type** | **String** | The type of barcode. Options are upc, gtin-13, gtin-14, or ean-8. The value \&quot;gtin\&quot; is also valid but is deprecated and will be converted to \&quot;gtin-13\&quot;. | [optional] |
| **dimensions** | [**Dimensions**](.md) |  | [optional] |
| **inventory_quantity** | **Integer** | The amount of stock available | [optional] |
| **retail_price** | **Float** | The desired retail price for this SKU, specific to this price list. | [optional] |
| **sku** | **String** | The SKU in the seller system. When creating a new variant, a SKU will be generated if one is not provided. | [optional] |
| **title** | **String** | The title of the variant | [optional] |
| **weight** | **Float** | The weight of the variant | [optional] |
| **weight_units** | **String** | The units of weight. Options are g, kg, lb, oz, or t. | [optional] |
| **images** | [**Array&lt;PatchVariantImages&gt;**](PatchVariantImages.md) | This is a convenience field used when creating a new variant which will associate the variant with images on the product. Setting this field will update the product images to include the new variant ID in the image.variantIds array. For existing variants, update the image.variantIds field directly. | [optional] |
| **attributes** | **Array&lt;Hash&gt;** | Attribute updates. | [optional] |

## Example

```ruby
require 'convictional_seller'

instance = ConvictionalSeller::PatchVariant.new(
  _id: null,
  barcode: 036000291452,
  barcode_type: upc,
  dimensions: null,
  inventory_quantity: 5,
  retail_price: 10.99,
  sku: variant-01,
  title: My Variant,
  weight: 1.5,
  weight_units: lb,
  images: null,
  attributes: null
)
```

