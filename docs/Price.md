# ConvictionalSeller::Price

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **_id** | **String** | The database ID | [optional] |
| **list_name** | **String** | The name of the price list | [optional] |
| **currency_name** | **String** | The currency in which the prices are. Can be USD, CAD, EUR, GBP or AUD | [optional] |
| **conversion** | **Float** | The conversion rate | [optional] |
| **markup** | **Float** | The markup in percentage of an item in a price list | [optional] |
| **rounding** | **Float** | Last 2 digits you want prices rounded up to | [optional] |
| **apply_to_new_products** | **Boolean** | Whether the price list will automatically price new products | [optional] |
| **discount_rate** | **Float** | The discount rate used to automatically derive a base price for new products | [optional] |
| **discount_type** | **String** | The type of discount calculation to use. Either \&quot;fixed\&quot; or \&quot;percent\&quot;. | [optional] |
| **list** | [**Array&lt;PriceList&gt;**](PriceList.md) |  | [optional] |
| **custom** | **Array&lt;Object&gt;** |  | [optional] |
| **created** | **Time** | The date this priceList was created | [optional] |
| **updated** | **Time** | The date this priceList was last updated | [optional] |
| **company_id** | **String** | The name of the company this price list belongs to | [optional] |

## Example

```ruby
require 'convictional_seller'

instance = ConvictionalSeller::Price.new(
  _id: null,
  list_name: null,
  currency_name: null,
  conversion: null,
  markup: null,
  rounding: null,
  apply_to_new_products: null,
  discount_rate: null,
  discount_type: null,
  list: null,
  custom: null,
  created: null,
  updated: null,
  company_id: null
)
```

