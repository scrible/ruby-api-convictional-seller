# ConvictionalSeller::SellerTax

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount** | **Float** | The amount of tax applied for this type of tax. | [optional] |
| **type** | **String** | The type of tax applied to order, currently &#x60;GS&#x60; and &#x60;SP&#x60; are supported. | [optional] |

## Example

```ruby
require 'convictional_seller'

instance = ConvictionalSeller::SellerTax.new(
  amount: 12.34,
  type: GS
)
```

