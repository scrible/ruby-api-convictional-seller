# ConvictionalSeller::OrderUpdate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **billed** | **Boolean** | Set billed to true to indicate that the order was billed outside of Convictional. This can only be set if the order is not already billed. You can set billed to false only if the order was billed outside of Convictional and is not refunded. | [optional] |
| **note** | **String** | Add an extra note that is specific to an order | [optional] |
| **attributes** | **Array&lt;Hash&gt;** | Attribute updates. | [optional] |

## Example

```ruby
require 'convictional_seller'

instance = ConvictionalSeller::OrderUpdate.new(
  billed: true,
  note: This is a note,
  attributes: null
)
```

