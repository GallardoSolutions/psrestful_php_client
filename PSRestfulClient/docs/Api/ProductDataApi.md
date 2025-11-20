# OpenAPI\Client\ProductDataApi



All URIs are relative to https://api.psrestful.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAllSellableProductIds()**](ProductDataApi.md#getAllSellableProductIds) | **GET** /v{api_version}/suppliers/{supplier_code}/sellable-product-ids | Get All Sellable Product Ids |
| [**getAllSellables()**](ProductDataApi.md#getAllSellables) | **GET** /v{api_version}/suppliers/{supplier_code}/sellables | Get All Sellables |
| [**getProductCloseoutV100()**](ProductDataApi.md#getProductCloseoutV100) | **GET** /v1.0.0/suppliers/{supplier_code}/products-closeout | Get Product Closeout V100 |
| [**getProductCloseoutV200()**](ProductDataApi.md#getProductCloseoutV200) | **GET** /v2.0.0/suppliers/{supplier_code}/products-closeout | Get Product Closeout V200 |
| [**getProductDateModifiedV100()**](ProductDataApi.md#getProductDateModifiedV100) | **GET** /v1.0.0/suppliers/{supplier_code}/products-modified-since | Get Product Date Modified V100 |
| [**getProductDateModifiedV200()**](ProductDataApi.md#getProductDateModifiedV200) | **GET** /v2.0.0/suppliers/{supplier_code}/products-modified-since | Get Product Date Modified V200 |
| [**getProductSellableV100()**](ProductDataApi.md#getProductSellableV100) | **GET** /v1.0.0/suppliers/{supplier_code}/sellable-products | Get Sellables V100 |
| [**getProductSellableV200()**](ProductDataApi.md#getProductSellableV200) | **GET** /v2.0.0/suppliers/{supplier_code}/sellable-products | Get Sellables V200 |
| [**getProductV100()**](ProductDataApi.md#getProductV100) | **GET** /v1.0.0/suppliers/{supplier_code}/products/{product_id} | Get Product V100 |
| [**getProductV200()**](ProductDataApi.md#getProductV200) | **GET** /v2.0.0/suppliers/{supplier_code}/products/{product_id} | Get Product V200 |


## `getAllSellableProductIds()`

```php
getAllSellableProductIds($supplier_code, $api_version, $line_name, $is_sellable, $environment, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\ProductIdsResponse
```

Get All Sellable Product Ids

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


$apiInstance = new OpenAPI\Client\Api\ProductDataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_code = 'supplier_code_example'; // string
$api_version = 'api_version_example'; // string
$line_name = 'line_name_example'; // string
$is_sellable = true; // bool
$environment = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\Environment(); // \OpenAPI\Client\Model\Environment
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getAllSellableProductIds($supplier_code, $api_version, $line_name, $is_sellable, $environment, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductDataApi->getAllSellableProductIds: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | **string**|  | |
| **api_version** | **string**|  | |
| **line_name** | **string**|  | [optional] |
| **is_sellable** | **bool**|  | [optional] [default to true] |
| **environment** | [**\OpenAPI\Client\Model\Environment**](../Model/.md)|  | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProductIdsResponse**](../Model/ProductIdsResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAllSellables()`

```php
getAllSellables($supplier_code, $api_version, $line_name, $is_sellable, $environment, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\AllSellablesFastResponse
```

Get All Sellables

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


$apiInstance = new OpenAPI\Client\Api\ProductDataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_code = 'supplier_code_example'; // string
$api_version = 'api_version_example'; // string
$line_name = 'line_name_example'; // string
$is_sellable = true; // bool
$environment = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\Environment(); // \OpenAPI\Client\Model\Environment
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getAllSellables($supplier_code, $api_version, $line_name, $is_sellable, $environment, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductDataApi->getAllSellables: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | **string**|  | |
| **api_version** | **string**|  | |
| **line_name** | **string**|  | [optional] |
| **is_sellable** | **bool**|  | [optional] [default to true] |
| **environment** | [**\OpenAPI\Client\Model\Environment**](../Model/.md)|  | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\AllSellablesFastResponse**](../Model/AllSellablesFastResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getProductCloseoutV100()`

```php
getProductCloseoutV100($supplier_code, $environment, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\ProductCloseOutResponseV100
```

Get Product Closeout V100

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


$apiInstance = new OpenAPI\Client\Api\ProductDataApi(
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
    $result = $apiInstance->getProductCloseoutV100($supplier_code, $environment, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductDataApi->getProductCloseoutV100: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\ProductCloseOutResponseV100**](../Model/ProductCloseOutResponseV100.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getProductCloseoutV200()`

```php
getProductCloseoutV200($supplier_code, $environment, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\ProductCloseOutResponseV200
```

Get Product Closeout V200

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


$apiInstance = new OpenAPI\Client\Api\ProductDataApi(
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
    $result = $apiInstance->getProductCloseoutV200($supplier_code, $environment, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductDataApi->getProductCloseoutV200: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\ProductCloseOutResponseV200**](../Model/ProductCloseOutResponseV200.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getProductDateModifiedV100()`

```php
getProductDateModifiedV100($supplier_code, $since, $environment, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\ProductDateModifiedResponseV100
```

Get Product Date Modified V100

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


$apiInstance = new OpenAPI\Client\Api\ProductDataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_code = 'supplier_code_example'; // string
$since = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime
$environment = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\Environment(); // \OpenAPI\Client\Model\Environment
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getProductDateModifiedV100($supplier_code, $since, $environment, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductDataApi->getProductDateModifiedV100: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | **string**|  | |
| **since** | **\DateTime**|  | |
| **environment** | [**\OpenAPI\Client\Model\Environment**](../Model/.md)|  | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProductDateModifiedResponseV100**](../Model/ProductDateModifiedResponseV100.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getProductDateModifiedV200()`

```php
getProductDateModifiedV200($supplier_code, $since, $environment, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\ProductDateModifiedResponseV200
```

Get Product Date Modified V200

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


$apiInstance = new OpenAPI\Client\Api\ProductDataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_code = 'supplier_code_example'; // string
$since = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime
$environment = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\Environment(); // \OpenAPI\Client\Model\Environment
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getProductDateModifiedV200($supplier_code, $since, $environment, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductDataApi->getProductDateModifiedV200: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | **string**|  | |
| **since** | **\DateTime**|  | |
| **environment** | [**\OpenAPI\Client\Model\Environment**](../Model/.md)|  | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProductDateModifiedResponseV200**](../Model/ProductDateModifiedResponseV200.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getProductSellableV100()`

```php
getProductSellableV100($supplier_code, $line_name, $is_sellable, $environment, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\GetProductSellableResponseV100
```

Get Sellables V100

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


$apiInstance = new OpenAPI\Client\Api\ProductDataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_code = 'supplier_code_example'; // string
$line_name = 'line_name_example'; // string
$is_sellable = true; // bool
$environment = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\Environment(); // \OpenAPI\Client\Model\Environment
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getProductSellableV100($supplier_code, $line_name, $is_sellable, $environment, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductDataApi->getProductSellableV100: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | **string**|  | |
| **line_name** | **string**|  | [optional] |
| **is_sellable** | **bool**|  | [optional] [default to true] |
| **environment** | [**\OpenAPI\Client\Model\Environment**](../Model/.md)|  | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetProductSellableResponseV100**](../Model/GetProductSellableResponseV100.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getProductSellableV200()`

```php
getProductSellableV200($supplier_code, $line_name, $is_sellable, $environment, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\GetProductSellableResponseV200
```

Get Sellables V200

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


$apiInstance = new OpenAPI\Client\Api\ProductDataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_code = 'supplier_code_example'; // string
$line_name = 'line_name_example'; // string
$is_sellable = true; // bool
$environment = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\Environment(); // \OpenAPI\Client\Model\Environment
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getProductSellableV200($supplier_code, $line_name, $is_sellable, $environment, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductDataApi->getProductSellableV200: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | **string**|  | |
| **line_name** | **string**|  | [optional] |
| **is_sellable** | **bool**|  | [optional] [default to true] |
| **environment** | [**\OpenAPI\Client\Model\Environment**](../Model/.md)|  | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetProductSellableResponseV200**](../Model/GetProductSellableResponseV200.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getProductV100()`

```php
getProductV100($supplier_code, $product_id, $localization_country, $localization_language, $environment, $real_product_id, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\ProductResponseV100
```

Get Product V100

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


$apiInstance = new OpenAPI\Client\Api\ProductDataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_code = 'supplier_code_example'; // string
$product_id = 'product_id_example'; // string
$localization_country = 'US'; // string
$localization_language = 'en'; // string
$environment = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\Environment(); // \OpenAPI\Client\Model\Environment
$real_product_id = 'real_product_id_example'; // string | Used when product id contains / character
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getProductV100($supplier_code, $product_id, $localization_country, $localization_language, $environment, $real_product_id, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductDataApi->getProductV100: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | **string**|  | |
| **product_id** | **string**|  | |
| **localization_country** | **string**|  | [optional] [default to &#39;US&#39;] |
| **localization_language** | **string**|  | [optional] [default to &#39;en&#39;] |
| **environment** | [**\OpenAPI\Client\Model\Environment**](../Model/.md)|  | [optional] |
| **real_product_id** | **string**| Used when product id contains / character | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProductResponseV100**](../Model/ProductResponseV100.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getProductV200()`

```php
getProductV200($supplier_code, $product_id, $localization_country, $localization_language, $environment, $real_product_id, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\ProductResponseV200
```

Get Product V200

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


$apiInstance = new OpenAPI\Client\Api\ProductDataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_code = 'supplier_code_example'; // string
$product_id = 'product_id_example'; // string
$localization_country = 'US'; // string
$localization_language = 'en'; // string
$environment = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\Environment(); // \OpenAPI\Client\Model\Environment
$real_product_id = 'real_product_id_example'; // string | Used when product id contains / character
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getProductV200($supplier_code, $product_id, $localization_country, $localization_language, $environment, $real_product_id, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductDataApi->getProductV200: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | **string**|  | |
| **product_id** | **string**|  | |
| **localization_country** | **string**|  | [optional] [default to &#39;US&#39;] |
| **localization_language** | **string**|  | [optional] [default to &#39;en&#39;] |
| **environment** | [**\OpenAPI\Client\Model\Environment**](../Model/.md)|  | [optional] |
| **real_product_id** | **string**| Used when product id contains / character | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProductResponseV200**](../Model/ProductResponseV200.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
