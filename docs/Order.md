# ConvictionalSeller::Order

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **_id** | **String** | The Convictional order ID. Read only. | [optional] |
| **buyer_order_code** | **String** | ID of the order in the buyer&#39;s system. | [optional] |
| **seller_order_code** | **String** | ID of the order in the seller&#39;s system. | [optional] |
| **buyer_company_id** | **String** | ID of the buyer company. | [optional] |
| **seller_company_id** | **String** | ID of the seller company. | [optional] |
| **buyer_email** | **String** | Email for notifications. | [optional] |
| **currency** | **String** | Currency code (e.g. CAD). | [optional] |
| **invoice_id** | **String** | ID of the associated invoice. | [optional] |
| **note** | **String** | A note relating to the order. | [optional] |
| **has_cancellations** | **Boolean** | Indicates if any line items have been cancelled. | [optional] |
| **shipping_address** | [**Address**](Address.md) |  | [optional] |
| **fill_time** | **Float** | The number of hours between the order being posted and the order being fulfilled. Null if not fulfilled. | [optional] |
| **ship_time** | **Float** | The number of hours between the order being created and the order being shipped. | [optional] |
| **packing_slip** | **String** | The URL to download a packing slip for this order. | [optional] |
| **custom** | **Array&lt;Object&gt;** |  | [optional] |
| **items** | [**Array&lt;OrderItem&gt;**](OrderItem.md) | The line items on the order. | [optional] |
| **created** | **String** | The time the order was created. Read Only. | [optional] |
| **updated** | **String** | The time the order was updated. Read Only. | [optional] |
| **posted** | **Boolean** | Indicates if the order has been posted to the seller&#39;s platform. Read Only. | [optional] |
| **posted_date** | **String** | The time the order was posted to the seller&#39;s platform. Read Only. | [optional] |
| **shipped** | **Boolean** | Indicates if the order has been fully shipped. Read Only. | [optional] |
| **shipped_date** | **String** | The time the order was fully shipped. Read Only. | [optional] |
| **billed** | **Boolean** | Indicates if the order has been invoiced. Read Only. | [optional] |
| **billed_date** | **String** | The time the order was invoiced. Read Only. | [optional] |

## Example

```ruby
require 'convictional_seller'

instance = ConvictionalSeller::Order.new(
  _id: 573ce4451e02f4bae78788aa,
  buyer_order_code: order_abc123,
  seller_order_code: order_def123,
  buyer_company_id: company_abc123,
  seller_company_id: company_def123,
  buyer_email: buyer@company.com,
  currency: USD,
  invoice_id: invoice_abc123,
  note: This order is ready to ship.,
  has_cancellations: true,
  shipping_address: null,
  fill_time: 12.5,
  ship_time: 0.5,
  packing_slip: https://app.convictional.com/orders/1234/packingslip,
  custom: null,
  items: null,
  created: 2020-05-01T19:35:00.000Z,
  updated: 2020-05-01T19:35:00.000Z,
  posted: true,
  posted_date: 2020-05-01T19:35:00.000Z,
  shipped: true,
  shipped_date: 2020-05-01T19:35:00.000Z,
  billed: true,
  billed_date: 2020-05-01T19:35:00.000Z
)
```

