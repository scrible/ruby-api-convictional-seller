# ConvictionalSeller::Product

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **_id** | **String** | The Convictional product ID. Read only. | [optional] |
| **code** | **String** | The seller&#39;s unique code for this product. |  |
| **active** | **Boolean** | Is this product active? Active products are visible to partners. | [optional] |
| **body_html** | **String** | The HTML body. Input will be sanitized before saving. | [optional] |
| **images** | [**Array&lt;Image&gt;**](Image.md) | Images of the product. Must be accessible via public URL. | [optional] |
| **tags** | **Array&lt;String&gt;** | Add tags to the product to make it easier for buyers to categorize. | [optional] |
| **title** | **String** | The name of the product. |  |
| **variants** | [**Array&lt;Variant&gt;**](Variant.md) | Include one variant per size, color, etc. If there are no variants then include a single entry to be the default. |  |
| **vendor** | **String** | The vendor of the product. | [optional] |
| **options** | [**Array&lt;ProductOptions&gt;**](ProductOptions.md) |  | [optional] |
| **google_product_category** | [**GoogleProductCategory**](GoogleProductCategory.md) |  | [optional] |
| **attributes** | **Hash&lt;String, Object&gt;** | Attributes are to be used to store additional details regarding this resource that are not supported on the Convictional resource. The object keys are the names for your attributes. | [optional] |
| **custom** | **Array&lt;Object&gt;** |  | [optional] |
| **created** | **Time** | The date this product was created. Read only. | [optional] |
| **updated** | **Time** | The date this product was last updated. Read only. | [optional] |
| **company_id** | **String** | The legacy company ID of the seller. Read only. | [optional] |
| **delisted** | **Boolean** | Is this product delisted? Read only. | [optional] |
| **delisted_at** | **Time** | The date this product was delisted. Read only. | [optional] |

## Example

```ruby
require 'convictional_seller'

instance = ConvictionalSeller::Product.new(
  _id: null,
  code: null,
  active: null,
  body_html: null,
  images: null,
  tags: null,
  title: null,
  variants: null,
  vendor: null,
  options: null,
  google_product_category: null,
  attributes: null,
  custom: null,
  created: null,
  updated: null,
  company_id: null,
  delisted: null,
  delisted_at: null
)
```

