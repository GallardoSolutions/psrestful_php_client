# OpenAPI\Client\ProductPriceAndConfigurationApi



All URIs are relative to https://api.psrestful.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAvailableCharges()**](ProductPriceAndConfigurationApi.md#getAvailableCharges) | **GET** /v1.0.0/suppliers/{supplier_code}/available-charges/{product_id} | Get Available Charges |
| [**getAvailableLocations()**](ProductPriceAndConfigurationApi.md#getAvailableLocations) | **GET** /v1.0.0/suppliers/{supplier_code}/available-locations/{product_id} | Get Available Locations |
| [**getConfigurationAndPricing()**](ProductPriceAndConfigurationApi.md#getConfigurationAndPricing) | **GET** /v1.0.0/suppliers/{supplier_code}/pricing-and-configuration/{product_id} | Get Configuration And Pricing |
| [**getDecorationColors()**](ProductPriceAndConfigurationApi.md#getDecorationColors) | **GET** /v1.0.0/suppliers/{supplier_code}/decoration-colors/{product_id} | Get Decoration Colors |
| [**getFobPoints()**](ProductPriceAndConfigurationApi.md#getFobPoints) | **GET** /v1.0.0/suppliers/{supplier_code}/fob-points/{product_id} | Get Fob Points |


## `getAvailableCharges()`

```php
getAvailableCharges($supplier_code, $product_id, $localization_country, $localization_language, $environment, $real_product_id, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\AvailableChargesResponse
```

Get Available Charges

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


$apiInstance = new OpenAPI\Client\Api\ProductPriceAndConfigurationApi(
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
    $result = $apiInstance->getAvailableCharges($supplier_code, $product_id, $localization_country, $localization_language, $environment, $real_product_id, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductPriceAndConfigurationApi->getAvailableCharges: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\AvailableChargesResponse**](../Model/AvailableChargesResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAvailableLocations()`

```php
getAvailableLocations($supplier_code, $product_id, $localization_country, $localization_language, $environment, $real_product_id, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\AvailableLocationsResponse
```

Get Available Locations

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


$apiInstance = new OpenAPI\Client\Api\ProductPriceAndConfigurationApi(
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
    $result = $apiInstance->getAvailableLocations($supplier_code, $product_id, $localization_country, $localization_language, $environment, $real_product_id, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductPriceAndConfigurationApi->getAvailableLocations: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\AvailableLocationsResponse**](../Model/AvailableLocationsResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getConfigurationAndPricing()`

```php
getConfigurationAndPricing($supplier_code, $product_id, $currency, $fob_id, $price_type, $configuration_type, $part_id, $localization_country, $localization_language, $environment, $real_product_id, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\ConfigurationAndPricingResponse
```

Get Configuration And Pricing

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


$apiInstance = new OpenAPI\Client\Api\ProductPriceAndConfigurationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_code = 'supplier_code_example'; // string
$product_id = 'product_id_example'; // string
$currency = 'currency_example'; // string
$fob_id = 'fob_id_example'; // string
$price_type = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\PriceType(); // \OpenAPI\Client\Model\PriceType
$configuration_type = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\ConfigurationType(); // \OpenAPI\Client\Model\ConfigurationType
$part_id = 'part_id_example'; // string
$localization_country = 'US'; // string
$localization_language = 'en'; // string
$environment = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\Environment(); // \OpenAPI\Client\Model\Environment
$real_product_id = 'real_product_id_example'; // string | Used when product id contains / character
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getConfigurationAndPricing($supplier_code, $product_id, $currency, $fob_id, $price_type, $configuration_type, $part_id, $localization_country, $localization_language, $environment, $real_product_id, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductPriceAndConfigurationApi->getConfigurationAndPricing: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | **string**|  | |
| **product_id** | **string**|  | |
| **currency** | **string**|  | |
| **fob_id** | **string**|  | |
| **price_type** | [**\OpenAPI\Client\Model\PriceType**](../Model/.md)|  | |
| **configuration_type** | [**\OpenAPI\Client\Model\ConfigurationType**](../Model/.md)|  | [optional] |
| **part_id** | **string**|  | [optional] |
| **localization_country** | **string**|  | [optional] [default to &#39;US&#39;] |
| **localization_language** | **string**|  | [optional] [default to &#39;en&#39;] |
| **environment** | [**\OpenAPI\Client\Model\Environment**](../Model/.md)|  | [optional] |
| **real_product_id** | **string**| Used when product id contains / character | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ConfigurationAndPricingResponse**](../Model/ConfigurationAndPricingResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getDecorationColors()`

```php
getDecorationColors($supplier_code, $product_id, $location_id, $decoration_id, $localization_country, $localization_language, $environment, $real_product_id, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\DecorationColorResponse
```

Get Decoration Colors

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


$apiInstance = new OpenAPI\Client\Api\ProductPriceAndConfigurationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_code = 'supplier_code_example'; // string
$product_id = 'product_id_example'; // string
$location_id = 56; // int
$decoration_id = 56; // int
$localization_country = 'US'; // string
$localization_language = 'en'; // string
$environment = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\Environment(); // \OpenAPI\Client\Model\Environment
$real_product_id = 'real_product_id_example'; // string | Used when product id contains / character
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getDecorationColors($supplier_code, $product_id, $location_id, $decoration_id, $localization_country, $localization_language, $environment, $real_product_id, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductPriceAndConfigurationApi->getDecorationColors: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | **string**|  | |
| **product_id** | **string**|  | |
| **location_id** | **int**|  | |
| **decoration_id** | **int**|  | [optional] |
| **localization_country** | **string**|  | [optional] [default to &#39;US&#39;] |
| **localization_language** | **string**|  | [optional] [default to &#39;en&#39;] |
| **environment** | [**\OpenAPI\Client\Model\Environment**](../Model/.md)|  | [optional] |
| **real_product_id** | **string**| Used when product id contains / character | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\DecorationColorResponse**](../Model/DecorationColorResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getFobPoints()`

```php
getFobPoints($supplier_code, $product_id, $localization_country, $localization_language, $environment, $real_product_id, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\FobPointsResponse
```

Get Fob Points

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


$apiInstance = new OpenAPI\Client\Api\ProductPriceAndConfigurationApi(
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
    $result = $apiInstance->getFobPoints($supplier_code, $product_id, $localization_country, $localization_language, $environment, $real_product_id, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductPriceAndConfigurationApi->getFobPoints: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\FobPointsResponse**](../Model/FobPointsResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
