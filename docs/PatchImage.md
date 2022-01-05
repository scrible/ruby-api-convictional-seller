# ConvictionalSeller::PatchImage

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **_id** | **String** | The Convictional ID of the image. Immutable. Must be included when updating an image using PATCH /products/{productId}. Excluding this field will create a new image. | [optional] |
| **source** | **String** | The public URL where the image is hosted. Immutable. Must be included when creating a new image. The source must be unique for all images on the product. | [optional] |
| **position** | **Integer** | Used to indicate the order of images. | [optional] |
| **variant_ids** | **Array&lt;String&gt;** | An array of variant IDs indicating the image is associated with these variants. Must send the entire array when updating. | [optional] |

## Example

```ruby
require 'convictional_seller'

instance = ConvictionalSeller::PatchImage.new(
  _id: null,
  source: null,
  position: 1,
  variant_ids: null
)
```

