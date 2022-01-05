# ConvictionalSeller::OrderItem

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **_id** | **String** | The Convictional order item ID. | [optional] |
| **seller_variant_code** | **String** | The seller&#39;s code for this variant. | [optional] |
| **quantity** | **Integer** | The quantity ordered for this line item. | [optional] |
| **cancelled** | **Boolean** | Indicates if this line item has been cancelled. | [optional] |
| **cancelled_reason** | **String** | The reason for the cancellation. | [optional] |
| **cancelled_by** | **String** | Identifies the company that initiated the cancellation. Options: \&quot;buyer\&quot;, \&quot;seller\&quot;, or \&quot;\&quot; (blank only if item is not cancelled). | [optional] |
| **cancelled_date** | **String** | The time the item was cancelled. Read Only. | [optional] |

## Example

```ruby
require 'convictional_seller'

instance = ConvictionalSeller::OrderItem.new(
  _id: 6023f23334ca2118255da096,
  seller_variant_code: ABC123,
  quantity: 2,
  cancelled: false,
  cancelled_reason: Out of stock,
  cancelled_by: seller,
  cancelled_date: 2020-05-01T19:35:00.000Z
)
```

