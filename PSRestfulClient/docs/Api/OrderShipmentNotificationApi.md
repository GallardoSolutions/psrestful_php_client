# OpenAPI\Client\OrderShipmentNotificationApi



All URIs are relative to https://api.psrestful.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getOrderShipmentNotificationV100()**](OrderShipmentNotificationApi.md#getOrderShipmentNotificationV100) | **GET** /v1.0.0/suppliers/{supplier_code}/order-shipment-notifications | Get Order Shipment Notification V100 |
| [**getOrderShipmentNotificationV200()**](OrderShipmentNotificationApi.md#getOrderShipmentNotificationV200) | **GET** /v2.0.0/suppliers/{supplier_code}/order-shipment-notifications | Get Order Shipment Notification V200 |


## `getOrderShipmentNotificationV100()`

```php
getOrderShipmentNotificationV100($supplier_code, $query_type, $reference_number, $shipment_date_timestamp, $environment, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\GetOrderShipmentNotificationResponse
```

Get Order Shipment Notification V100

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


$apiInstance = new OpenAPI\Client\Api\OrderShipmentNotificationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_code = 'supplier_code_example'; // string
$query_type = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\OSNQueryType(); // \OpenAPI\Client\Model\OSNQueryType
$reference_number = 'reference_number_example'; // string
$shipment_date_timestamp = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime
$environment = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\Environment(); // \OpenAPI\Client\Model\Environment
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getOrderShipmentNotificationV100($supplier_code, $query_type, $reference_number, $shipment_date_timestamp, $environment, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderShipmentNotificationApi->getOrderShipmentNotificationV100: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | **string**|  | |
| **query_type** | [**\OpenAPI\Client\Model\OSNQueryType**](../Model/.md)|  | |
| **reference_number** | **string**|  | [optional] |
| **shipment_date_timestamp** | **\DateTime**|  | [optional] |
| **environment** | [**\OpenAPI\Client\Model\Environment**](../Model/.md)|  | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetOrderShipmentNotificationResponse**](../Model/GetOrderShipmentNotificationResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getOrderShipmentNotificationV200()`

```php
getOrderShipmentNotificationV200($supplier_code, $query_type, $reference_number, $shipment_date_timestamp, $environment, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\GetOrderShipmentNotificationResponse
```

Get Order Shipment Notification V200

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


$apiInstance = new OpenAPI\Client\Api\OrderShipmentNotificationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_code = 'supplier_code_example'; // string
$query_type = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\OSNQueryType(); // \OpenAPI\Client\Model\OSNQueryType
$reference_number = 'reference_number_example'; // string
$shipment_date_timestamp = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime
$environment = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\Environment(); // \OpenAPI\Client\Model\Environment
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getOrderShipmentNotificationV200($supplier_code, $query_type, $reference_number, $shipment_date_timestamp, $environment, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderShipmentNotificationApi->getOrderShipmentNotificationV200: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | **string**|  | |
| **query_type** | [**\OpenAPI\Client\Model\OSNQueryType**](../Model/.md)|  | |
| **reference_number** | **string**|  | [optional] |
| **shipment_date_timestamp** | **\DateTime**|  | [optional] |
| **environment** | [**\OpenAPI\Client\Model\Environment**](../Model/.md)|  | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetOrderShipmentNotificationResponse**](../Model/GetOrderShipmentNotificationResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
