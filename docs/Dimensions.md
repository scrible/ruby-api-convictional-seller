# ConvictionalSeller::Dimensions

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **length** | **Float** | A length measurement | [optional] |
| **width** | **Float** | A width measurement | [optional] |
| **height** | **Float** | A height measurement | [optional] |
| **units** | **String** | The units of measurement. Options are cm or in. | [optional] |

## Example

```ruby
require 'convictional_seller'

instance = ConvictionalSeller::Dimensions.new(
  length: 11,
  width: 20,
  height: 14.5,
  units: in
)
```

