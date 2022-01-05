# ConvictionalSeller::OrderApi

All URIs are relative to *https://api.convictional.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**cancel_order**](OrderApi.md#cancel_order) | **POST** /orders/{orderId}/cancel | Cancel order |
| [**cancel_order_item**](OrderApi.md#cancel_order_item) | **POST** /orders/{orderId}/items/{itemId}/cancel | Cancel order item |
| [**get_order_by_id**](OrderApi.md#get_order_by_id) | **GET** /orders/{orderId} | Get order |
| [**get_orders**](OrderApi.md#get_orders) | **GET** /orders | List orders |
| [**invoice_order**](OrderApi.md#invoice_order) | **POST** /orders/{orderId}/invoices | Create invoice |
| [**post_fulfillment**](OrderApi.md#post_fulfillment) | **POST** /orders/{orderId}/fulfillments | Create fulfillment |
| [**refund_order**](OrderApi.md#refund_order) | **POST** /orders/{orderId}/refund | Create refund |
| [**update_order_by_id**](OrderApi.md#update_order_by_id) | **PATCH** /orders/{orderId} | Update order |


## cancel_order

> <Order> cancel_order(order_id, authorization, order_cancellation)

Cancel order

Use this endpoint to cancel an entire order. After an order is cancelled, order.hasCancellations=true and each order item will have orderItem.cancelled=true. Orders cannot be uncancelled afterwards. Any order can be cancelled, including flagged orders and unposted orders, as long as the order is not already fully cancelled or fully fulfilled. Partially fulfilled orders can only be cancelled if unfulfilledOnly=true is sent. When unfulfilledOnly=true is sent, order items that have already been fulfilled are not cancelled, and all unfulfilled order items are cancelled. If the order had no fulfillments, this endpoint behaves the same as when omitting the unfulfilledOnly flag. If the order had at least one fulfillment, then in addition to setting the cancelled status, order.shipped will be set to true and the order is now considered fully fulfilled. If an order item has been partially - but not completely - fulfilled, then that order item will be cancelled and a new uncancelled order item will be created representing the quantity that had already been fulfilled.

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

api_instance = ConvictionalSeller::OrderApi.new
order_id = 'order_id_example' # String | ID of the order to cancel
authorization = '6fbb801c-2f9b-42a3-9c44-4e57463fb3a4' # String | Auth token provided by Convictional upon account creation.
order_cancellation = ConvictionalSeller::OrderCancellation.new # OrderCancellation | An object with cancellation settings

begin
  # Cancel order
  result = api_instance.cancel_order(order_id, authorization, order_cancellation)
  p result
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling OrderApi->cancel_order: #{e}"
end
```

#### Using the cancel_order_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Order>, Integer, Hash)> cancel_order_with_http_info(order_id, authorization, order_cancellation)

```ruby
begin
  # Cancel order
  data, status_code, headers = api_instance.cancel_order_with_http_info(order_id, authorization, order_cancellation)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Order>
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling OrderApi->cancel_order_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order_id** | **String** | ID of the order to cancel |  |
| **authorization** | **String** | Auth token provided by Convictional upon account creation. |  |
| **order_cancellation** | [**OrderCancellation**](OrderCancellation.md) | An object with cancellation settings |  |

### Return type

[**Order**](Order.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## cancel_order_item

> <OrderItem> cancel_order_item(order_id, item_id, authorization, order_item_cancellation)

Cancel order item

Cancel a single order item on an order. Order items are fully cancelled by default. Order items can be partially cancelled by using the newQuantity parameter. Note that doing a partial cancellation will cancel the original order item and create a new order item representing the uncancelled quantity. Fulfilled items cannot be cancelled.

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

api_instance = ConvictionalSeller::OrderApi.new
order_id = 'order_id_example' # String | ID of the order
item_id = 'item_id_example' # String | ID of the order item
authorization = '6fbb801c-2f9b-42a3-9c44-4e57463fb3a4' # String | Auth token provided by Convictional upon account creation.
order_item_cancellation = ConvictionalSeller::OrderItemCancellation.new # OrderItemCancellation | 

begin
  # Cancel order item
  result = api_instance.cancel_order_item(order_id, item_id, authorization, order_item_cancellation)
  p result
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling OrderApi->cancel_order_item: #{e}"
end
```

#### Using the cancel_order_item_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<OrderItem>, Integer, Hash)> cancel_order_item_with_http_info(order_id, item_id, authorization, order_item_cancellation)

```ruby
begin
  # Cancel order item
  data, status_code, headers = api_instance.cancel_order_item_with_http_info(order_id, item_id, authorization, order_item_cancellation)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <OrderItem>
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling OrderApi->cancel_order_item_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order_id** | **String** | ID of the order |  |
| **item_id** | **String** | ID of the order item |  |
| **authorization** | **String** | Auth token provided by Convictional upon account creation. |  |
| **order_item_cancellation** | [**OrderItemCancellation**](OrderItemCancellation.md) |  |  |

### Return type

[**OrderItem**](OrderItem.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## get_order_by_id

> <Order> get_order_by_id(order_id)

Get order

An endpoint for getting an order.

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

api_instance = ConvictionalSeller::OrderApi.new
order_id = 'order_id_example' # String | ID of the order to get

begin
  # Get order
  result = api_instance.get_order_by_id(order_id)
  p result
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling OrderApi->get_order_by_id: #{e}"
end
```

#### Using the get_order_by_id_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Order>, Integer, Hash)> get_order_by_id_with_http_info(order_id)

```ruby
begin
  # Get order
  data, status_code, headers = api_instance.get_order_by_id_with_http_info(order_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Order>
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling OrderApi->get_order_by_id_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order_id** | **String** | ID of the order to get |  |

### Return type

[**Order**](Order.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_orders

> <Array<Order>> get_orders(authorization, opts)

List orders

An endpoint for getting orders.

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

api_instance = ConvictionalSeller::OrderApi.new
authorization = '6fbb801c-2f9b-42a3-9c44-4e57463fb3a4' # String | Auth token provided by Convictional upon account creation.
opts = {
  page: 0, # Integer | The page number of resources to return.
  limit: 250, # Integer | The number of resources to return.
  shipped: false, # Boolean | Return orders that are marked as shipped.
  posted: false, # Boolean | Return orders that are synced to the seller.
  billed: false, # Boolean | Return orders that are marked as billed/invoiced.
  refunded: false, # Boolean | Return orders that are marked as refunded.
  created_min: '2020-06-25T19:00:00.000+00:00' # String | Return resources created after a given time. Use RFC 3339 format.
}

begin
  # List orders
  result = api_instance.get_orders(authorization, opts)
  p result
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling OrderApi->get_orders: #{e}"
end
```

#### Using the get_orders_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Order>>, Integer, Hash)> get_orders_with_http_info(authorization, opts)

```ruby
begin
  # List orders
  data, status_code, headers = api_instance.get_orders_with_http_info(authorization, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Order>>
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling OrderApi->get_orders_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **authorization** | **String** | Auth token provided by Convictional upon account creation. |  |
| **page** | **Integer** | The page number of resources to return. | [optional][default to 0] |
| **limit** | **Integer** | The number of resources to return. | [optional][default to 50] |
| **shipped** | **Boolean** | Return orders that are marked as shipped. | [optional] |
| **posted** | **Boolean** | Return orders that are synced to the seller. | [optional] |
| **billed** | **Boolean** | Return orders that are marked as billed/invoiced. | [optional] |
| **refunded** | **Boolean** | Return orders that are marked as refunded. | [optional] |
| **created_min** | **String** | Return resources created after a given time. Use RFC 3339 format. | [optional] |

### Return type

[**Array&lt;Order&gt;**](Order.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## invoice_order

> <SellerInvoiceResponse> invoice_order(order_id, authorization, seller_order_invoice_tax)

Create invoice

Creates an invoice for the given order ID for manual billing. Currently for taxes, we support only `GS` (Goods & Services Tax) and `SP` (State/Provincial Sales Tax) values for `Type`. Invoices are only able to be generated after the order has been shipped. 

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

api_instance = ConvictionalSeller::OrderApi.new
order_id = 'order_id_example' # String | ID of the order to invoice
authorization = '6fbb801c-2f9b-42a3-9c44-4e57463fb3a4' # String | Auth token provided by Convictional upon account creation.
seller_order_invoice_tax = ConvictionalSeller::SellerOrderInvoiceTax.new # SellerOrderInvoiceTax | An object with tax specific settings for the invoice

begin
  # Create invoice
  result = api_instance.invoice_order(order_id, authorization, seller_order_invoice_tax)
  p result
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling OrderApi->invoice_order: #{e}"
end
```

#### Using the invoice_order_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SellerInvoiceResponse>, Integer, Hash)> invoice_order_with_http_info(order_id, authorization, seller_order_invoice_tax)

```ruby
begin
  # Create invoice
  data, status_code, headers = api_instance.invoice_order_with_http_info(order_id, authorization, seller_order_invoice_tax)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SellerInvoiceResponse>
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling OrderApi->invoice_order_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order_id** | **String** | ID of the order to invoice |  |
| **authorization** | **String** | Auth token provided by Convictional upon account creation. |  |
| **seller_order_invoice_tax** | [**SellerOrderInvoiceTax**](SellerOrderInvoiceTax.md) | An object with tax specific settings for the invoice |  |

### Return type

[**SellerInvoiceResponse**](SellerInvoiceResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## post_fulfillment

> <InlineResponse2003> post_fulfillment(order_id, order_fulfillment)

Create fulfillment

An endpoint for creating fulfillments on orders. Order items that have been cancelled cannot be fulfilled.

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

api_instance = ConvictionalSeller::OrderApi.new
order_id = 'order_id_example' # String | ID of the order with the new fulfillment
order_fulfillment = ConvictionalSeller::OrderFulfillment.new # OrderFulfillment | An object containing fulfillment details

begin
  # Create fulfillment
  result = api_instance.post_fulfillment(order_id, order_fulfillment)
  p result
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling OrderApi->post_fulfillment: #{e}"
end
```

#### Using the post_fulfillment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InlineResponse2003>, Integer, Hash)> post_fulfillment_with_http_info(order_id, order_fulfillment)

```ruby
begin
  # Create fulfillment
  data, status_code, headers = api_instance.post_fulfillment_with_http_info(order_id, order_fulfillment)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InlineResponse2003>
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling OrderApi->post_fulfillment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order_id** | **String** | ID of the order with the new fulfillment |  |
| **order_fulfillment** | [**OrderFulfillment**](OrderFulfillment.md) | An object containing fulfillment details |  |

### Return type

[**InlineResponse2003**](InlineResponse2003.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## refund_order

> <SellerOrderRefund> refund_order(order_id, authorization, seller_order_refund)

Create refund

Use this endpoint to add a refund to an existing order. This will add a new entry to the `refunds` array on the order object. If `cancelUnfulfilled` is set to true, then any item that is being refunded and is not already shipped will be cancelled as well as refunded. **Note that this endpoint does not currently handle return shipping or refund payout.

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

api_instance = ConvictionalSeller::OrderApi.new
order_id = 'order_id_example' # String | ID of the order to refund
authorization = '6fbb801c-2f9b-42a3-9c44-4e57463fb3a4' # String | Auth token provided by Convictional upon account creation.
seller_order_refund = ConvictionalSeller::SellerOrderRefund.new # SellerOrderRefund | An object with refund settings

begin
  # Create refund
  result = api_instance.refund_order(order_id, authorization, seller_order_refund)
  p result
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling OrderApi->refund_order: #{e}"
end
```

#### Using the refund_order_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SellerOrderRefund>, Integer, Hash)> refund_order_with_http_info(order_id, authorization, seller_order_refund)

```ruby
begin
  # Create refund
  data, status_code, headers = api_instance.refund_order_with_http_info(order_id, authorization, seller_order_refund)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SellerOrderRefund>
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling OrderApi->refund_order_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order_id** | **String** | ID of the order to refund |  |
| **authorization** | **String** | Auth token provided by Convictional upon account creation. |  |
| **seller_order_refund** | [**SellerOrderRefund**](SellerOrderRefund.md) | An object with refund settings |  |

### Return type

[**SellerOrderRefund**](SellerOrderRefund.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_order_by_id

> <Order> update_order_by_id(order_id, order_update)

Update order

An endpoint for partially updating orders.

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

api_instance = ConvictionalSeller::OrderApi.new
order_id = 'order_id_example' # String | ID of the order to update
order_update = ConvictionalSeller::OrderUpdate.new # OrderUpdate | The order fields to update

begin
  # Update order
  result = api_instance.update_order_by_id(order_id, order_update)
  p result
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling OrderApi->update_order_by_id: #{e}"
end
```

#### Using the update_order_by_id_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Order>, Integer, Hash)> update_order_by_id_with_http_info(order_id, order_update)

```ruby
begin
  # Update order
  data, status_code, headers = api_instance.update_order_by_id_with_http_info(order_id, order_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Order>
rescue ConvictionalSeller::ApiError => e
  puts "Error when calling OrderApi->update_order_by_id_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order_id** | **String** | ID of the order to update |  |
| **order_update** | [**OrderUpdate**](OrderUpdate.md) | The order fields to update |  |

### Return type

[**Order**](Order.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

