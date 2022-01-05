# ConvictionalSeller::ResponseMetaData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **has_more** | **Boolean** | Pagination flag to indicate if there is more data available. | [optional] |
| **_next** | **String** | Absolute link to the next page of results. Is \&quot;\&quot; if hasMore is false. | [optional] |
| **previous** | **String** | Absolute link to the previous page of results. Is \&quot;\&quot; if on first page. | [optional] |

## Example

```ruby
require 'convictional_seller'

instance = ConvictionalSeller::ResponseMetaData.new(
  has_more: false,
  _next: null,
  previous: null
)
```

