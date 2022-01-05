# ConvictionalSeller::Invoice

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **_id** | **String** | The Convictional invoice ID. Read only. | [optional] |
| **amount_paid** | **Integer** | Amount paid on the inoice. | [optional] |
| **application_fee** | **Integer** | Application Fee of the invoice. | [optional] |
| **currency** | **String** | Currency code (e.g. CAD). | [optional] |
| **created** | **String** | The time the invoice was created. Read Only. | [optional] |
| **updated** | **String** | The time the invoice was updated. Read Only. | [optional] |
| **notified** | **Boolean** | Notification flag. | [optional] |
| **notified_date** | **String** | The time the notification flag was set. | [optional] |
| **paid** | **Boolean** | Flag if the invoice was paid. | [optional] |
| **paid_date** | **String** | The time the invoice was paid. | [optional] |
| **refunded** | **Boolean** | Flag if the invoice was refunded. | [optional] |
| **refunded_date** | **String** | The time the invoice was refunded. | [optional] |
| **download** | **String** | Download link to the invoice from integrations we utilize, like Stripe | [optional] |
| **hosted_url** | **String** | Hosted link to the invoice from integrations we utilize, like Stripe | [optional] |
| **due_date** | **String** | The date the invoice is due. | [optional] |
| **buyer_id** | **String** | ID of the buyer company. Read Only. | [optional] |
| **seller_id** | **String** | ID of the seller company. Read Only. | [optional] |
| **buyer_company_object_id** | **String** | Convictional ID for the Buyer Company. Read Only. | [optional] |
| **seller_company_object_id** | **String** | Convictional ID for the Seller Company. Read Only. | [optional] |
| **custom** | **Array&lt;Object&gt;** |  | [optional] |
| **edi_sent** | **Boolean** | Indicates if the EDI (810) document has been sent. | [optional] |
| **taxes** | [**Array&lt;SellerTax&gt;**](SellerTax.md) | The line items on the order. | [optional] |
| **items** | [**Array&lt;SellerInvoiceItem&gt;**](SellerInvoiceItem.md) | The line items on the order. | [optional] |
| **posted** | **Boolean** | Indicates if the invoice has been posted to the buyer&#39;s platform. | [optional] |
| **buyer_code** | **String** | Buyer&#39;s specific code for the invoice. | [optional] |
| **seller_code** | **String** | Seller&#39;s specific code for the invoice. | [optional] |
| **source** | **String** | Source of the invoice. | [optional] |
| **source_id** | **String** | ID from the source of invoice. | [optional] |

## Example

```ruby
require 'convictional_seller'

instance = ConvictionalSeller::Invoice.new(
  _id: 573ce4451e02f4bae78788aa,
  amount_paid: 0,
  application_fee: 0,
  currency: USD,
  created: 2020-05-01T19:35:00.000Z,
  updated: 2020-05-01T19:35:00.000Z,
  notified: false,
  notified_date: 2020-05-01T19:35:00.000Z,
  paid: false,
  paid_date: 2020-05-01T19:35:00.000Z,
  refunded: false,
  refunded_date: 2020-05-01T19:35:00.000Z,
  download: https://pay.stripe.com/invoice/acct_XXXX...,
  hosted_url: https://invoice.stripe.com/i/acct_ABC123...,
  due_date: 2020-05-01T19:35:00.000Z,
  buyer_id: company_abc123,
  seller_id: company_def123,
  buyer_company_object_id: 573ce4451e02f4bae78788aa,
  seller_company_object_id: 573ce4451e02f4bae78788aa,
  custom: null,
  edi_sent: true,
  taxes: null,
  items: null,
  posted: true,
  buyer_code: 7101Z,
  seller_code: ABC123,
  source: stripe,
  source_id: in_573ce4451e02f4bae78788aa
)
```

