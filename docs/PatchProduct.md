# ConvictionalSeller::PatchProduct

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **active** | **Boolean** | Whether or not this product is active. | [optional] |
| **body_html** | **String** | The HTML body or description of the product.  Input will be sanitized before saving. | [optional] |
| **tags** | **Array&lt;String&gt;** | The tags associated with the product | [optional] |
| **title** | **String** | The title of the product. Cannot be an empty string if defined. | [optional] |
| **type** | **String** | The type of the product. Deprecated. | [optional] |
| **vendor** | **String** | The brand of the product. | [optional] |
| **variants** | [**Array&lt;PatchVariant&gt;**](PatchVariant.md) | Array of variants to update. Including the _id field will update a variant. Excluding the _id field will create a new variant. | [optional] |
| **images** | [**Array&lt;PatchImage&gt;**](PatchImage.md) | Array of product images to update. Including the _id field will update an image. Excluding the _id field will create a new image. The source of an image cannot be updated, to change this you must delete the old image and create a new one. | [optional] |
| **options** | [**Array&lt;PatchOption&gt;**](PatchOption.md) | Array of option updates. Including the _id field will update an option. Excluding the _id field will create a new option. | [optional] |
| **google_product_category** | [**GoogleProductCategory**](GoogleProductCategory.md) |  | [optional] |
| **attributes** | **Array&lt;Hash&gt;** | Attribute updates. | [optional] |

## Example

```ruby
require 'convictional_seller'

instance = ConvictionalSeller::PatchProduct.new(
  active: true,
  body_html: &lt;p&gt;This is a great product&lt;/p&gt;,
  tags: null,
  title: My Product,
  type: item,
  vendor: Brand TM,
  variants: {&quot;_id&quot;:&quot;6023f23334ca2118255da096&quot;,&quot;title&quot;:&quot;my new title&quot;},
  images: null,
  options: null,
  google_product_category: null,
  attributes: null
)
```

