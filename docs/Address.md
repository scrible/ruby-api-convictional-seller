# ConvictionalSeller::Address

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | The name of the customer receiving the fulfillment. | [optional] |
| **address_one** | **String** | Address line one. |  |
| **address_two** | **String** | Address line two. | [optional] |
| **city** | **String** | The city. |  |
| **state** | **String** | The state or province. | [optional] |
| **country** | **String** | The country. |  |
| **zip** | **String** | The zip code or postal code. | [optional] |
| **company** | **String** | The name of the organization receiving the fulfillment. | [optional] |

## Example

```ruby
require 'convictional_seller'

instance = ConvictionalSeller::Address.new(
  name: Jane Doe,
  address_one: 123 Main St,
  address_two: Apt. 411,
  city: Waterloo,
  state: Ontario,
  country: Canada,
  zip: A1A 1A1,
  company: My Business Inc.
)
```

