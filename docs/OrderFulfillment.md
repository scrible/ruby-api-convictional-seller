# ConvictionalSeller::OrderFulfillment

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **carrier** | **String** | The shipping carrier | [optional] |
| **tracking_code** | **String** | Tracking code provided by the carrier. | [optional] |
| **tracking_urls** | **Array&lt;String&gt;** |  | [optional] |
| **items** | [**Array&lt;OrderFulfillmentItems&gt;**](OrderFulfillmentItems.md) |  | [optional] |

## Example

```ruby
require 'convictional_seller'

instance = ConvictionalSeller::OrderFulfillment.new(
  carrier: USPS,
  tracking_code: 1Z204E380338943508,
  tracking_urls: null,
  items: null
)
```

