# OpenAPI\Client\DefaultApi



All URIs are relative to https://api.psrestful.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getServiceCodes()**](DefaultApi.md#getServiceCodes) | **GET** /service-codes | Get Service Codes |
| [**getServices()**](DefaultApi.md#getServices) | **GET** /services/{supplier_code} | Get Services |


## `getServiceCodes()`

```php
getServiceCodes(): mixed
```

Get Service Codes

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getServiceCodes();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->getServiceCodes: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**mixed**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getServices()`

```php
getServices($supplier_code): \OpenAPI\Client\Model\AllServicesResponse
```

Get Services

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$supplier_code = 'supplier_code_example'; // string

try {
    $result = $apiInstance->getServices($supplier_code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->getServices: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\AllServicesResponse**](../Model/AllServicesResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
