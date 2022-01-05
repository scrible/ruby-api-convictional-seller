# ConvictionalSeller::SellerOrderRefund

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **cancel_unfulfilled** | **Boolean** | Whether unfulfilled items should be cancelled | [optional] |
| **items** | [**Array&lt;SellerOrderRefundItem&gt;**](SellerOrderRefundItem.md) | The items that are being refunded | [optional] |

## Example

```ruby
require 'convictional_seller'

instance = ConvictionalSeller::SellerOrderRefund.new(
  cancel_unfulfilled: false,
  items: null
)
```

