# OpenAPI\Client\InventoryApi



All URIs are relative to https://api.psrestful.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getFilterValues()**](InventoryApi.md#getFilterValues) | **GET** /v{api_version}/suppliers/{supplier_code}/inventory/filter-values/{product_id} | Get Filter Values |
| [**getInventoryByProductV121()**](InventoryApi.md#getInventoryByProductV121) | **GET** /v1.2.1/suppliers/{supplier_code}/inventory/{product_id} | Get Inventory By Product V121 |
| [**getInventoryByProductV200()**](InventoryApi.md#getInventoryByProductV200) | **GET** /v2.0.0/suppliers/{supplier_code}/inventory/{product_id} | Get Inventory By Product V200 |


## `getFilterValues()`

```php
getFilterValues($supplier_code, $api_version, $product_id, $product_id_type, $environment, $real_product_id, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\FilterValuesResponseV200
```

Get Filter Values

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


$apiInstance = new OpenAPI\Client\Api\InventoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_code = 'supplier_code_example'; // string
$api_version = 'api_version_example'; // string
$product_id = 'product_id_example'; // string
$product_id_type = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\ProductIDType(); // \OpenAPI\Client\Model\ProductIDType
$environment = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\Environment(); // \OpenAPI\Client\Model\Environment
$real_product_id = 'real_product_id_example'; // string | Used when product id contains / character
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getFilterValues($supplier_code, $api_version, $product_id, $product_id_type, $environment, $real_product_id, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InventoryApi->getFilterValues: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | **string**|  | |
| **api_version** | **string**|  | |
| **product_id** | **string**|  | |
| **product_id_type** | [**\OpenAPI\Client\Model\ProductIDType**](../Model/.md)|  | [optional] |
| **environment** | [**\OpenAPI\Client\Model\Environment**](../Model/.md)|  | [optional] |
| **real_product_id** | **string**| Used when product id contains / character | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\FilterValuesResponseV200**](../Model/FilterValuesResponseV200.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getInventoryByProductV121()`

```php
getInventoryByProductV121($supplier_code, $product_id, $environment, $color, $size, $real_product_id, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\InventoryLevelsResponseV121
```

Get Inventory By Product V121

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


$apiInstance = new OpenAPI\Client\Api\InventoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_code = 'supplier_code_example'; // string
$product_id = 'product_id_example'; // string
$environment = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\Environment(); // \OpenAPI\Client\Model\Environment
$color = array('color_example'); // string[]
$size = array('size_example'); // string[]
$real_product_id = 'real_product_id_example'; // string | Used when product id contains / character
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getInventoryByProductV121($supplier_code, $product_id, $environment, $color, $size, $real_product_id, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InventoryApi->getInventoryByProductV121: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | **string**|  | |
| **product_id** | **string**|  | |
| **environment** | [**\OpenAPI\Client\Model\Environment**](../Model/.md)|  | [optional] |
| **color** | [**string[]**](../Model/string.md)|  | [optional] |
| **size** | [**string[]**](../Model/string.md)|  | [optional] |
| **real_product_id** | **string**| Used when product id contains / character | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\InventoryLevelsResponseV121**](../Model/InventoryLevelsResponseV121.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getInventoryByProductV200()`

```php
getInventoryByProductV200($supplier_code, $product_id, $environment, $part_id, $color, $size, $real_product_id, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\InventoryLevelsResponseV200
```

Get Inventory By Product V200

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


$apiInstance = new OpenAPI\Client\Api\InventoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_code = 'supplier_code_example'; // string
$product_id = 'product_id_example'; // string
$environment = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\Environment(); // \OpenAPI\Client\Model\Environment
$part_id = array('part_id_example'); // string[]
$color = array('color_example'); // string[]
$size = array('size_example'); // string[]
$real_product_id = 'real_product_id_example'; // string | Used when product id contains / character
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getInventoryByProductV200($supplier_code, $product_id, $environment, $part_id, $color, $size, $real_product_id, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InventoryApi->getInventoryByProductV200: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | **string**|  | |
| **product_id** | **string**|  | |
| **environment** | [**\OpenAPI\Client\Model\Environment**](../Model/.md)|  | [optional] |
| **part_id** | [**string[]**](../Model/string.md)|  | [optional] |
| **color** | [**string[]**](../Model/string.md)|  | [optional] |
| **size** | [**string[]**](../Model/string.md)|  | [optional] |
| **real_product_id** | **string**| Used when product id contains / character | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\InventoryLevelsResponseV200**](../Model/InventoryLevelsResponseV200.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
