# ConvictionalSeller::GoogleProductCategory

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **code** | **Integer** | The category code from the Google Product Taxonomy. If only the category code is provided, we will set the corresponding category name. If this product should not be categorized, set this value to 0 and category name to \&quot;\&quot;. | [optional] |
| **name** | **String** | The category name from the Google Product Taxonomy. If only the category name is provided, we will set the corresponding category code. If this product should not be categorized, set this value to \&quot;\&quot; and category code to 0. | [optional] |

## Example

```ruby
require 'convictional_seller'

instance = ConvictionalSeller::GoogleProductCategory.new(
  code: null,
  name: null
)
```

