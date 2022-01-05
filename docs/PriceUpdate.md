# ConvictionalSeller::PriceUpdate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **list_name** | **String** | The name of the price list | [optional] |
| **currency_name** | **String** | The currency in which the prices are. Can be USD, CAD, EUR, GBP or AUD | [optional] |
| **conversion** | **Float** | The conversion rate | [optional] |
| **rounding** | **Float** | Last 2 digits you want prices rounded up to | [optional] |
| **apply_to_new_products** | **Boolean** | Whether the price list will automatically price new products | [optional] |
| **discount_rate** | **Float** | The discount rate used to automatically derive a base price for new products | [optional] |
| **discount_type** | **String** | The type of discount calculation to use. Either \&quot;fixed\&quot; or \&quot;percent\&quot;. | [optional] |
| **list** | [**Array&lt;PriceUpdateList&gt;**](PriceUpdateList.md) |  | [optional] |

## Example

```ruby
require 'convictional_seller'

instance = ConvictionalSeller::PriceUpdate.new(
  list_name: null,
  currency_name: null,
  conversion: null,
  rounding: null,
  apply_to_new_products: null,
  discount_rate: null,
  discount_type: null,
  list: null
)
```

