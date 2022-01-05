# ConvictionalSeller::ProductApi

All URIs are relative to *https://api.convictional.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**delete_product_by_id**](ProductApi.md#delete_product_by_id) | **DELETE** /products/{productId} | Delete product |
| [**delete_product_image_by_id**](ProductApi.md#delete_product_image_by_id) | **DELETE** /products/{productId}/images/{imageId} | Delete image |
| [**get_product_by_id**](ProductApi.md#get_product_by_id) | **GET** /products/{productId} | Get product |
| [**get_products**](ProductApi.md#get_products) | **GET** /products | List products |
| [**patch_product_by_id**](ProductApi.md#patch_product_by_id) | **PATCH** /products/{productId} | Update product |
| [**post_products**](ProductApi.md#post_products) | **POST** /products | Create product |


## delete_product_by_id

> <InlineResponse200> delete_product_by_id(product_id)

Delete product

An endpoint for deleting a product with the provided ID

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

api_instance = ConvictionalSeller::ProductApi.new
product_id = 'product_id_example' # String | ID of the product to delete

begin
  # Delete product
  result = api_instance.delete_product_by_id(product_id)
  p result
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling ProductApi->delete_product_by_id: #{e}"
end
```

#### Using the delete_product_by_id_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InlineResponse200>, Integer, Hash)> delete_product_by_id_with_http_info(product_id)

```ruby
begin
  # Delete product
  data, status_code, headers = api_instance.delete_product_by_id_with_http_info(product_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InlineResponse200>
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling ProductApi->delete_product_by_id_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** | ID of the product to delete |  |

### Return type

[**InlineResponse200**](InlineResponse200.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## delete_product_image_by_id

> Object delete_product_image_by_id(product_id, image_id)

Delete image

An endpoint for deleting a product image

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

api_instance = ConvictionalSeller::ProductApi.new
product_id = 'product_id_example' # String | ID of the product to be deleted from
image_id = 'image_id_example' # String | ID of the image to be deleted

begin
  # Delete image
  result = api_instance.delete_product_image_by_id(product_id, image_id)
  p result
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling ProductApi->delete_product_image_by_id: #{e}"
end
```

#### Using the delete_product_image_by_id_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> delete_product_image_by_id_with_http_info(product_id, image_id)

```ruby
begin
  # Delete image
  data, status_code, headers = api_instance.delete_product_image_by_id_with_http_info(product_id, image_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling ProductApi->delete_product_image_by_id_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** | ID of the product to be deleted from |  |
| **image_id** | **String** | ID of the image to be deleted |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_product_by_id

> <Product> get_product_by_id(product_id)

Get product

An endpoint for getting products.

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

api_instance = ConvictionalSeller::ProductApi.new
product_id = 'product_id_example' # String | ID of the product to get

begin
  # Get product
  result = api_instance.get_product_by_id(product_id)
  p result
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling ProductApi->get_product_by_id: #{e}"
end
```

#### Using the get_product_by_id_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Product>, Integer, Hash)> get_product_by_id_with_http_info(product_id)

```ruby
begin
  # Get product
  data, status_code, headers = api_instance.get_product_by_id_with_http_info(product_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Product>
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling ProductApi->get_product_by_id_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** | ID of the product to get |  |

### Return type

[**Product**](Product.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_products

> <Array<Product>> get_products(opts)

List products

An endpoint to get products, can be used by buyers or sellers

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

api_instance = ConvictionalSeller::ProductApi.new
opts = {
  title: 'title_example', # String | Filters products by title. This can either be an exact title or a title similar.
  vendor: 'vendor_example', # String | Filters products by brand (e.g. product.vendor field values). Must be an exact match.
  product_code: 'product_code_example', # String | Filters products by product code. This can either be an exact product code or a product code similar.
  active: true, # Boolean | Filter out products are active or not active. This field is not required.
  company_id: 'company_id_example', # String | Filters products by seller company ID. Must be an exact match.
  tags: 'tags_example', # String | Filters products by tags. This is comma delimited for multiple tags. It returns products that have at any of the tags. Must be an exact match. Sellers only.
  page: 56, # Integer | The page number of results to return. Note this is a zero-based index.
  limit: 56 # Integer | The number of results per page. Max is 250.
}

begin
  # List products
  result = api_instance.get_products(opts)
  p result
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling ProductApi->get_products: #{e}"
end
```

#### Using the get_products_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Product>>, Integer, Hash)> get_products_with_http_info(opts)

```ruby
begin
  # List products
  data, status_code, headers = api_instance.get_products_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Product>>
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling ProductApi->get_products_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **title** | **String** | Filters products by title. This can either be an exact title or a title similar. | [optional] |
| **vendor** | **String** | Filters products by brand (e.g. product.vendor field values). Must be an exact match. | [optional] |
| **product_code** | **String** | Filters products by product code. This can either be an exact product code or a product code similar. | [optional] |
| **active** | **Boolean** | Filter out products are active or not active. This field is not required. | [optional] |
| **company_id** | **String** | Filters products by seller company ID. Must be an exact match. | [optional] |
| **tags** | **String** | Filters products by tags. This is comma delimited for multiple tags. It returns products that have at any of the tags. Must be an exact match. Sellers only. | [optional] |
| **page** | **Integer** | The page number of results to return. Note this is a zero-based index. | [optional][default to 0] |
| **limit** | **Integer** | The number of results per page. Max is 250. | [optional][default to 25] |

### Return type

[**Array&lt;Product&gt;**](Product.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## patch_product_by_id

> <Product> patch_product_by_id(product_id, patch_product)

Update product

An endpoint for partially updating a product with the provided ID. New variants, images, and options can be created by omitting their respective _id fields.

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

api_instance = ConvictionalSeller::ProductApi.new
product_id = 'product_id_example' # String | ID of the product to update
patch_product = ConvictionalSeller::PatchProduct.new # PatchProduct | 

begin
  # Update product
  result = api_instance.patch_product_by_id(product_id, patch_product)
  p result
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling ProductApi->patch_product_by_id: #{e}"
end
```

#### Using the patch_product_by_id_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Product>, Integer, Hash)> patch_product_by_id_with_http_info(product_id, patch_product)

```ruby
begin
  # Update product
  data, status_code, headers = api_instance.patch_product_by_id_with_http_info(product_id, patch_product)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Product>
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling ProductApi->patch_product_by_id_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_id** | **String** | ID of the product to update |  |
| **patch_product** | [**PatchProduct**](PatchProduct.md) |  |  |

### Return type

[**Product**](Product.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## post_products

> <Product> post_products(product)

Create product

An endpoint for sellers to create new products.

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

api_instance = ConvictionalSeller::ProductApi.new
product = ConvictionalSeller::Product.new({code: 'code_example', title: 'title_example', variants: [ConvictionalSeller::Variant.new]}) # Product | All the fields in a product

begin
  # Create product
  result = api_instance.post_products(product)
  p result
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling ProductApi->post_products: #{e}"
end
```

#### Using the post_products_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Product>, Integer, Hash)> post_products_with_http_info(product)

```ruby
begin
  # Create product
  data, status_code, headers = api_instance.post_products_with_http_info(product)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Product>
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling ProductApi->post_products_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product** | [**Product**](Product.md) | All the fields in a product |  |

### Return type

[**Product**](Product.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json, text/csv
- **Accept**: application/json

