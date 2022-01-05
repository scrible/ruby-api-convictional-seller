# ConvictionalSeller::OrderCancellation

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **reason** | **String** | The reason for cancellation. | [optional] |
| **unfulfilled_only** | **Boolean** | Only cancel unfulfilled line items, rather than the entire order. | [optional][default to false] |

## Example

```ruby
require 'convictional_seller'

instance = ConvictionalSeller::OrderCancellation.new(
  reason: Out of stock.,
  unfulfilled_only: false
)
```

