# ConvictionalSeller::Variant

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **_id** | **String** | The Convictional variant ID. Read only. | [optional] |
| **sku** | **String** | The seller&#39;s unique SKU for this variant. | [optional] |
| **title** | **String** | The name of the variant. | [optional] |
| **id** | **Integer** | A legacy Convictional ID for this variant. Read only. | [optional] |
| **inventory_quantity** | **Integer** | The amount of stock available. | [optional] |
| **barcode** | **String** | The barcode of the variant. | [optional] |
| **barcode_type** | **String** | The type of barcode. Options are upc, gtin-13, gtin-14, or ean-8. The value \&quot;gtin\&quot; is also valid but is deprecated and will be converted to \&quot;gtin-13\&quot;. | [optional] |
| **option1** | **String** | The value for option 1. | [optional] |
| **option2** | **String** | The value for option 2. | [optional] |
| **option3** | **String** | The value for option 3. | [optional] |
| **partner_price** | **Float** | Available to buyers only. Shows the MSRP set by the seller. Read only. | [optional] |
| **base_price** | **Float** | Available to buyers only. The wholesale cost of this variant. Read only. | [optional] |
| **base_currency** | **String** | Available to buyers only. The currency of basePrice. Read only. | [optional] |
| **images** | [**Array&lt;VariantImages&gt;**](VariantImages.md) | An array of images corresponding to this variant. | [optional] |
| **attributes** | **Hash&lt;String, Object&gt;** | Attributes are to be used to store additional details regarding this resource that are not supported on the Convictional resource. The object keys are the names for your attributes. | [optional] |

## Example

```ruby
require 'convictional_seller'

instance = ConvictionalSeller::Variant.new(
  _id: 123456789,
  sku: null,
  title: null,
  id: 123456789,
  inventory_quantity: null,
  barcode: null,
  barcode_type: null,
  option1: null,
  option2: null,
  option3: null,
  partner_price: null,
  base_price: null,
  base_currency: CAD,
  images: null,
  attributes: null
)
```

