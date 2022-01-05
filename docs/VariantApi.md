# ConvictionalSeller::VariantApi

All URIs are relative to *https://api.convictional.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**patch_variant_by_id**](VariantApi.md#patch_variant_by_id) | **PATCH** /products/{productId}/variants/{variantId} | Update variant |


## patch_variant_by_id

> <Variant> patch_variant_by_id(product_id, variant_id, patch_variant)

Update variant

An endpoint for partially updating a product variant with the provided ID

### Examples

```ruby
require 'time'
require 'convictional_seller'
# setup authorization
ConvictionalSeller.configure do |config|
  # Configure API key authorization: ApiKeyAuth
  config.api_key['ApiKeyAuth'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['ApiKeyAuth'] = 'Bearer'
end

api_instance = ConvictionalSeller::VariantApi.new
product_id = 'product_id_example' # String | ID of the product to update
variant_id = 'variant_id_example' # String | ID of the variant to update
patch_variant = ConvictionalSeller::PatchVariant.new # PatchVariant | 

begin
  # Update variant
  result = api_instance.patch_variant_by_id(product_id, variant_id, patch_variant)
  p result
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling VariantApi->patch_variant_by_id: #{e}"
end
```

#### Using the patch_variant_by_id_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Variant>, Integer, Hash)> patch_variant_by_id_with_http_info(product_id, variant_id, patch_variant)

```ruby
begin
  # Update variant
  data, status_code, headers = api_instance.patch_variant_by_id_with_http_info(product_id, variant_id, patch_variant)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Variant>
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling VariantApi->patch_variant_by_id_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** | ID of the product to update |  |
| **variant_id** | **String** | ID of the variant to update |  |
| **patch_variant** | [**PatchVariant**](PatchVariant.md) |  |  |

### Return type

[**Variant**](Variant.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

