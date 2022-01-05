# ConvictionalSeller::Image

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **source** | **String** | The URL of the image. | [optional] |
| **position** | **Integer** | The index of the image. This will determine the order that images appear in. | [optional] |
| **variant_ids** | **Array&lt;String&gt;** | The variant IDs associated with this image. Set this value via the variant.images field. Read only. | [optional] |

## Example

```ruby
require 'convictional_seller'

instance = ConvictionalSeller::Image.new(
  source: https://mystore.com/product001-1.jpg,
  position: 0,
  variant_ids: null
)
```

