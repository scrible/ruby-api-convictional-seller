# ConvictionalSeller::SellerOrderRefundItem

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **item_id** | **String** | ID of the item that was refunded | [optional] |
| **reason** | **String** | The reason for returning this item | [optional] |
| **quantity_to_refund** | **Integer** | The number of items to refund (must be less than remaining quantity on order) | [optional] |

## Example

```ruby
require 'convictional_seller'

instance = ConvictionalSeller::SellerOrderRefundItem.new(
  item_id: 573ce4455502f4bae7878555,
  reason: Bad Stitching on sleeve,
  quantity_to_refund: 3
)
```

