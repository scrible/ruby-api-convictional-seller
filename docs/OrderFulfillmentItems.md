# ConvictionalSeller::OrderFulfillmentItems

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | The line item ID (corresponds to the sellerItemCode on the order item). | [optional] |
| **sku** | **String** | The product SKU | [optional] |
| **quantity** | **Integer** | The amount shipped | [optional] |

## Example

```ruby
require 'convictional_seller'

instance = ConvictionalSeller::OrderFulfillmentItems.new(
  id: 1,
  sku: SKU123,
  quantity: 2
)
```

