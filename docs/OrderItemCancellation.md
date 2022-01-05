# ConvictionalSeller::OrderItemCancellation

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **reason** | **String** | The reason for cancellation. | [optional][default to &#39;&#39;] |
| **new_quantity** | **Integer** | Allows partial item cancellation. The quantity of the item to remain uncancelled. Must be greater or equal to the fulfilled quantity and less than the total item quantity. | [optional][default to 0] |

## Example

```ruby
require 'convictional_seller'

instance = ConvictionalSeller::OrderItemCancellation.new(
  reason: Out of stock.,
  new_quantity: 1
)
```

