# convictional_seller

ConvictionalSeller - the Ruby gem for the Seller API

This API reference documents endpoints that are exclusive to sellers.

This SDK is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: v2021-01-01
- Package version: 2021.1.1
- Build package: org.openapitools.codegen.languages.RubyClientCodegen
For more information, please visit [https://support.convictional.com](https://support.convictional.com)

## Installation

### Build a gem

To build the Ruby code into a gem:

```shell
gem build convictional_seller.gemspec
```

Then either install the gem locally:

```shell
gem install ./convictional_seller-2021.1.1.gem
```

(for development, run `gem install --dev ./convictional_seller-2021.1.1.gem` to install the development dependencies)

or publish the gem to a gem hosting service, e.g. [RubyGems](https://rubygems.org/).

Finally add this to the Gemfile:

    gem 'convictional_seller', '~> 2021.1.1'

### Install from Git

If the Ruby gem is hosted at a git repository: https://github.com/GIT_USER_ID/GIT_REPO_ID, then add the following in the Gemfile:

    gem 'convictional_seller', :git => 'https://github.com/GIT_USER_ID/GIT_REPO_ID.git'

### Include the Ruby code directly

Include the Ruby code directly using `-I` as follows:

```shell
ruby -Ilib script.rb
```

## Getting Started

Please follow the [installation](#installation) procedure and then run the following code:

```ruby
# Load the gem
require 'convictional_seller'

# Setup authorization
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
  #Cancel order
  result = api_instance.cancel_order(order_id, authorization, order_cancellation)
  p result
rescue ConvictionalSeller::ApiError => e
  puts "Exception when calling OrderApi->cancel_order: #{e}"
end

```

## Documentation for API Endpoints

All URIs are relative to *https://api.convictional.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ConvictionalSeller::OrderApi* | [**cancel_order**](docs/OrderApi.md#cancel_order) | **POST** /orders/{orderId}/cancel | Cancel order
*ConvictionalSeller::OrderApi* | [**cancel_order_item**](docs/OrderApi.md#cancel_order_item) | **POST** /orders/{orderId}/items/{itemId}/cancel | Cancel order item
*ConvictionalSeller::OrderApi* | [**get_order_by_id**](docs/OrderApi.md#get_order_by_id) | **GET** /orders/{orderId} | Get order
*ConvictionalSeller::OrderApi* | [**get_orders**](docs/OrderApi.md#get_orders) | **GET** /orders | List orders
*ConvictionalSeller::OrderApi* | [**invoice_order**](docs/OrderApi.md#invoice_order) | **POST** /orders/{orderId}/invoices | Create invoice
*ConvictionalSeller::OrderApi* | [**post_fulfillment**](docs/OrderApi.md#post_fulfillment) | **POST** /orders/{orderId}/fulfillments | Create fulfillment
*ConvictionalSeller::OrderApi* | [**refund_order**](docs/OrderApi.md#refund_order) | **POST** /orders/{orderId}/refund | Create refund
*ConvictionalSeller::OrderApi* | [**update_order_by_id**](docs/OrderApi.md#update_order_by_id) | **PATCH** /orders/{orderId} | Update order
*ConvictionalSeller::PriceListApi* | [**delete_price_list_by_id**](docs/PriceListApi.md#delete_price_list_by_id) | **DELETE** /prices/{priceId} | Delete price list
*ConvictionalSeller::PriceListApi* | [**get_price_list_by_id**](docs/PriceListApi.md#get_price_list_by_id) | **GET** /prices/{priceId} | Get price list
*ConvictionalSeller::PriceListApi* | [**get_price_list_template**](docs/PriceListApi.md#get_price_list_template) | **GET** /templates/price | Get price list template
*ConvictionalSeller::PriceListApi* | [**post_price_list**](docs/PriceListApi.md#post_price_list) | **POST** /prices | Create price list
*ConvictionalSeller::PriceListApi* | [**post_price_list_csv**](docs/PriceListApi.md#post_price_list_csv) | **POST** /prices/upload | Upload price list
*ConvictionalSeller::PriceListApi* | [**put_price_list_by_id**](docs/PriceListApi.md#put_price_list_by_id) | **PUT** /prices/{priceId} | Update price list
*ConvictionalSeller::ProductApi* | [**delete_product_by_id**](docs/ProductApi.md#delete_product_by_id) | **DELETE** /products/{productId} | Delete product
*ConvictionalSeller::ProductApi* | [**delete_product_image_by_id**](docs/ProductApi.md#delete_product_image_by_id) | **DELETE** /products/{productId}/images/{imageId} | Delete image
*ConvictionalSeller::ProductApi* | [**get_product_by_id**](docs/ProductApi.md#get_product_by_id) | **GET** /products/{productId} | Get product
*ConvictionalSeller::ProductApi* | [**get_products**](docs/ProductApi.md#get_products) | **GET** /products | List products
*ConvictionalSeller::ProductApi* | [**patch_product_by_id**](docs/ProductApi.md#patch_product_by_id) | **PATCH** /products/{productId} | Update product
*ConvictionalSeller::ProductApi* | [**post_products**](docs/ProductApi.md#post_products) | **POST** /products | Create product
*ConvictionalSeller::VariantApi* | [**patch_variant_by_id**](docs/VariantApi.md#patch_variant_by_id) | **PATCH** /products/{productId}/variants/{variantId} | Update variant


## Documentation for Models

 - [ConvictionalSeller::Address](docs/Address.md)
 - [ConvictionalSeller::Dimensions](docs/Dimensions.md)
 - [ConvictionalSeller::EmptyError](docs/EmptyError.md)
 - [ConvictionalSeller::ErrorMessage](docs/ErrorMessage.md)
 - [ConvictionalSeller::GoogleProductCategory](docs/GoogleProductCategory.md)
 - [ConvictionalSeller::Image](docs/Image.md)
 - [ConvictionalSeller::InlineResponse200](docs/InlineResponse200.md)
 - [ConvictionalSeller::InlineResponse2001](docs/InlineResponse2001.md)
 - [ConvictionalSeller::InlineResponse2002](docs/InlineResponse2002.md)
 - [ConvictionalSeller::InlineResponse2003](docs/InlineResponse2003.md)
 - [ConvictionalSeller::InlineResponse400](docs/InlineResponse400.md)
 - [ConvictionalSeller::InlineResponse4001](docs/InlineResponse4001.md)
 - [ConvictionalSeller::InlineResponse401](docs/InlineResponse401.md)
 - [ConvictionalSeller::InlineResponse404](docs/InlineResponse404.md)
 - [ConvictionalSeller::InlineResponse415](docs/InlineResponse415.md)
 - [ConvictionalSeller::InlineResponse500](docs/InlineResponse500.md)
 - [ConvictionalSeller::Invoice](docs/Invoice.md)
 - [ConvictionalSeller::Order](docs/Order.md)
 - [ConvictionalSeller::OrderCancellation](docs/OrderCancellation.md)
 - [ConvictionalSeller::OrderFulfillment](docs/OrderFulfillment.md)
 - [ConvictionalSeller::OrderFulfillmentItems](docs/OrderFulfillmentItems.md)
 - [ConvictionalSeller::OrderItem](docs/OrderItem.md)
 - [ConvictionalSeller::OrderItemCancellation](docs/OrderItemCancellation.md)
 - [ConvictionalSeller::OrderUpdate](docs/OrderUpdate.md)
 - [ConvictionalSeller::PatchImage](docs/PatchImage.md)
 - [ConvictionalSeller::PatchOption](docs/PatchOption.md)
 - [ConvictionalSeller::PatchProduct](docs/PatchProduct.md)
 - [ConvictionalSeller::PatchVariant](docs/PatchVariant.md)
 - [ConvictionalSeller::PatchVariantImages](docs/PatchVariantImages.md)
 - [ConvictionalSeller::Price](docs/Price.md)
 - [ConvictionalSeller::PriceList](docs/PriceList.md)
 - [ConvictionalSeller::PriceUpdate](docs/PriceUpdate.md)
 - [ConvictionalSeller::PriceUpdateList](docs/PriceUpdateList.md)
 - [ConvictionalSeller::Product](docs/Product.md)
 - [ConvictionalSeller::ProductOptions](docs/ProductOptions.md)
 - [ConvictionalSeller::ResponseMetaData](docs/ResponseMetaData.md)
 - [ConvictionalSeller::SellerInvoiceItem](docs/SellerInvoiceItem.md)
 - [ConvictionalSeller::SellerInvoiceResponse](docs/SellerInvoiceResponse.md)
 - [ConvictionalSeller::SellerOrderInvoiceTax](docs/SellerOrderInvoiceTax.md)
 - [ConvictionalSeller::SellerOrderRefund](docs/SellerOrderRefund.md)
 - [ConvictionalSeller::SellerOrderRefundItem](docs/SellerOrderRefundItem.md)
 - [ConvictionalSeller::SellerTax](docs/SellerTax.md)
 - [ConvictionalSeller::Variant](docs/Variant.md)
 - [ConvictionalSeller::VariantImages](docs/VariantImages.md)


## Documentation for Authorization


### ApiKeyAuth


- **Type**: API key
- **API key parameter name**: Authorization
- **Location**: HTTP header

