# OpenAPI\Client\PurchaseOrderApi



All URIs are relative to https://api.psrestful.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getSupportedOrderTypes()**](PurchaseOrderApi.md#getSupportedOrderTypes) | **GET** /v1.0.0/suppliers/{supplier_code}/supported-order-types | Get Supported Order Types |
| [**sendPo()**](PurchaseOrderApi.md#sendPo) | **POST** /v1.0.0/suppliers/{supplier_code}/purchase-orders/ | Send Po |


## `getSupportedOrderTypes()`

```php
getSupportedOrderTypes($supplier_code, $environment, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\GetSupportedOrderTypesResponse
```

Get Supported Order Types

This function returns the supported Order Types the vendor accepts.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');

// Configure OAuth2 access token for authorization: OAuth2PasswordBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PurchaseOrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_code = 'supplier_code_example'; // string
$environment = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\Environment(); // \OpenAPI\Client\Model\Environment
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getSupportedOrderTypes($supplier_code, $environment, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseOrderApi->getSupportedOrderTypes: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | **string**|  | |
| **environment** | [**\OpenAPI\Client\Model\Environment**](../Model/.md)|  | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetSupportedOrderTypesResponse**](../Model/GetSupportedOrderTypesResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `sendPo()`

```php
sendPo($supplier_code, $po, $x_forwarded_for, $x_account_id): \OpenAPI\Client\Model\SendPOResponse
```

Send Po

This function will send a blank, sample, simple, or configured purchase order to a supplier. The purchase order service is designed to work in conjunction with data from PPC service

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');

// Configure OAuth2 access token for authorization: OAuth2PasswordBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PurchaseOrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_code = 'supplier_code_example'; // string
$po = new \OpenAPI\Client\Model\PO(); // \OpenAPI\Client\Model\PO
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string

try {
    $result = $apiInstance->sendPo($supplier_code, $po, $x_forwarded_for, $x_account_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseOrderApi->sendPo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | **string**|  | |
| **po** | [**\OpenAPI\Client\Model\PO**](../Model/PO.md)|  | |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\SendPOResponse**](../Model/SendPOResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
