# ConvictionalSeller::PatchOption

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **_id** | **String** | The Convictional ID of the option. Immutable. Must be included when updating an option using PATCH/products/{productId}, otherwise creates a new option. | [optional] |
| **name** | **String** | The option name. | [optional] |
| **position** | **Integer** | Indicates which of the variant option values this option name corresponds to. Valid values are 1, 2, or 3. | [optional] |

## Example

```ruby
require 'convictional_seller'

instance = ConvictionalSeller::PatchOption.new(
  _id: null,
  name: Size,
  position: 1
)
```

