# ConvictionalSeller::PriceUpdateList

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sku** | **String** | The sku of an item in a price list | [optional] |
| **price** | **Float** | The price of an item in a price list | [optional] |
| **markup** | **Float** | The markup in percentage of an item in a price list | [optional] |
| **retail_price** | **Float** | The retail price of an item, based on its price and markup | [optional] |
| **type** | **String** | fixed for dollar markup or percent for percentage | [optional] |

## Example

```ruby
require 'convictional_seller'

instance = ConvictionalSeller::PriceUpdateList.new(
  sku: null,
  price: null,
  markup: null,
  retail_price: null,
  type: null
)
```

