# ConvictionalSeller::SellerInvoiceItem

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **_id** | **String** | ID of the item for the invoice. | [optional] |
| **amount_cents** | **Integer** | The amount of referenced item, in cents. | [optional] |
| **reference** | **String** | What this item is refenced from. | [optional] |
| **reference_id** | **String** | Referenced type Convictional ID. Read Only. | [optional] |

## Example

```ruby
require 'convictional_seller'

instance = ConvictionalSeller::SellerInvoiceItem.new(
  _id: 6023f23334ca2118255da096,
  amount_cents: 1600,
  reference: order,
  reference_id: 6023f23334ca2118255da096
)
```

