# ConvictionalSeller::PriceListApi

All URIs are relative to *https://api.convictional.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**delete_price_list_by_id**](PriceListApi.md#delete_price_list_by_id) | **DELETE** /prices/{priceId} | Delete price list |
| [**get_price_list_by_id**](PriceListApi.md#get_price_list_by_id) | **GET** /prices/{priceId} | Get price list |
| [**get_price_list_template**](PriceListApi.md#get_price_list_template) | **GET** /templates/price | Get price list template |
| [**post_price_list**](PriceListApi.md#post_price_list) | **POST** /prices | Create price list |
| [**post_price_list_csv**](PriceListApi.md#post_price_list_csv) | **POST** /prices/upload | Upload price list |
| [**put_price_list_by_id**](PriceListApi.md#put_price_list_by_id) | **PUT** /prices/{priceId} | Update price list |


## delete_price_list_by_id

> <InlineResponse2001> delete_price_list_by_id(price_id)

Delete price list

An endpoint for permanently deleting price lists.

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

api_instance = ConvictionalSeller::PriceListApi.new
price_id = 'price_id_example' # String | ID of the price list

begin
  # Delete price list
  result = api_instance.delete_price_list_by_id(price_id)
  p result
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling PriceListApi->delete_price_list_by_id: #{e}"
end
```

#### Using the delete_price_list_by_id_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InlineResponse2001>, Integer, Hash)> delete_price_list_by_id_with_http_info(price_id)

```ruby
begin
  # Delete price list
  data, status_code, headers = api_instance.delete_price_list_by_id_with_http_info(price_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InlineResponse2001>
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling PriceListApi->delete_price_list_by_id_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **price_id** | **String** | ID of the price list |  |

### Return type

[**InlineResponse2001**](InlineResponse2001.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_price_list_by_id

> <Price> get_price_list_by_id(price_id)

Get price list

An endpoint for retrieving price lists. In cases where a price list may contain invalid SKUs, those SKUs are not included in the response.

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

api_instance = ConvictionalSeller::PriceListApi.new
price_id = 'price_id_example' # String | ID of the price list

begin
  # Get price list
  result = api_instance.get_price_list_by_id(price_id)
  p result
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling PriceListApi->get_price_list_by_id: #{e}"
end
```

#### Using the get_price_list_by_id_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Price>, Integer, Hash)> get_price_list_by_id_with_http_info(price_id)

```ruby
begin
  # Get price list
  data, status_code, headers = api_instance.get_price_list_by_id_with_http_info(price_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Price>
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling PriceListApi->get_price_list_by_id_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **price_id** | **String** | ID of the price list |  |

### Return type

[**Price**](Price.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_price_list_template

> String get_price_list_template(authorization)

Get price list template

Returns a CSV template that can be filled with retail and base prices for all variants and then upload it to /prices/upload

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

api_instance = ConvictionalSeller::PriceListApi.new
authorization = '6fbb801c-2f9b-42a3-9c44-4e57463fb3a4' # String | Auth token provided by Convictional upon account creation.

begin
  # Get price list template
  result = api_instance.get_price_list_template(authorization)
  p result
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling PriceListApi->get_price_list_template: #{e}"
end
```

#### Using the get_price_list_template_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(String, Integer, Hash)> get_price_list_template_with_http_info(authorization)

```ruby
begin
  # Get price list template
  data, status_code, headers = api_instance.get_price_list_template_with_http_info(authorization)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => String
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling PriceListApi->get_price_list_template_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **authorization** | **String** | Auth token provided by Convictional upon account creation. |  |

### Return type

**String**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: text/csv, application/json


## post_price_list

> <Price> post_price_list(price)

Create price list

An endpoint to create a price list for the given company API key

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

api_instance = ConvictionalSeller::PriceListApi.new
price = ConvictionalSeller::Price.new # Price | All the fields in a pricelist

begin
  # Create price list
  result = api_instance.post_price_list(price)
  p result
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling PriceListApi->post_price_list: #{e}"
end
```

#### Using the post_price_list_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Price>, Integer, Hash)> post_price_list_with_http_info(price)

```ruby
begin
  # Create price list
  data, status_code, headers = api_instance.post_price_list_with_http_info(price)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Price>
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling PriceListApi->post_price_list_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **price** | [**Price**](Price.md) | All the fields in a pricelist |  |

### Return type

[**Price**](Price.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## post_price_list_csv

> <InlineResponse2002> post_price_list_csv(opts)

Upload price list

An endpoint for creating new price lists using a CSV file.

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

api_instance = ConvictionalSeller::PriceListApi.new
opts = {
  name: 'name_example', # String | The name of the new price list.
  file: [{ ... }] # Array<Object> | A CSV file containing price list information. The following fields represent the columns in the CSV file. All columns must be present in the given order and the first row of each column must contain the exact header from below. The columns marked as read only must still be included in requests, but can be blank except for the header.
}

begin
  # Upload price list
  result = api_instance.post_price_list_csv(opts)
  p result
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling PriceListApi->post_price_list_csv: #{e}"
end
```

#### Using the post_price_list_csv_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InlineResponse2002>, Integer, Hash)> post_price_list_csv_with_http_info(opts)

```ruby
begin
  # Upload price list
  data, status_code, headers = api_instance.post_price_list_csv_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InlineResponse2002>
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling PriceListApi->post_price_list_csv_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | The name of the new price list. | [optional] |
| **file** | [**Array&lt;Object&gt;**](Object.md) | A CSV file containing price list information. The following fields represent the columns in the CSV file. All columns must be present in the given order and the first row of each column must contain the exact header from below. The columns marked as read only must still be included in requests, but can be blank except for the header. | [optional] |

### Return type

[**InlineResponse2002**](InlineResponse2002.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json


## put_price_list_by_id

> <Price> put_price_list_by_id(price_id, opts)

Update price list

An endpoint for fully updating price lists.

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

api_instance = ConvictionalSeller::PriceListApi.new
price_id = 'price_id_example' # String | ID of the price list
opts = {
  price_update: ConvictionalSeller::PriceUpdate.new # PriceUpdate | 
}

begin
  # Update price list
  result = api_instance.put_price_list_by_id(price_id, opts)
  p result
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling PriceListApi->put_price_list_by_id: #{e}"
end
```

#### Using the put_price_list_by_id_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Price>, Integer, Hash)> put_price_list_by_id_with_http_info(price_id, opts)

```ruby
begin
  # Update price list
  data, status_code, headers = api_instance.put_price_list_by_id_with_http_info(price_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Price>
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling PriceListApi->put_price_list_by_id_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **price_id** | **String** | ID of the price list |  |
| **price_update** | [**PriceUpdate**](PriceUpdate.md) |  | [optional] |

### Return type

[**Price**](Price.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

