# OpenAPI\Client\MediaContentApi



All URIs are relative to https://api.psrestful.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getMediaContentV100()**](MediaContentApi.md#getMediaContentV100) | **GET** /v1.0.0/suppliers/{supplier_code}/medias/{product_id} | Get Media Content V100 |
| [**getMediaContentV110()**](MediaContentApi.md#getMediaContentV110) | **GET** /v1.1.0/suppliers/{supplier_code}/medias/{product_id} | Get Media Content V110 |
| [**getMediaDateModified()**](MediaContentApi.md#getMediaDateModified) | **GET** /v1.1.0/suppliers/{supplier_code}/media-modified-since | Get Media Date Modified |


## `getMediaContentV100()`

```php
getMediaContentV100($supplier_code, $product_id, $media_type, $culture_name, $part_id, $class_type, $environment, $real_product_id, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\MediaContentDetailsResponse
```

Get Media Content V100

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


$apiInstance = new OpenAPI\Client\Api\MediaContentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_code = 'supplier_code_example'; // string
$product_id = 'product_id_example'; // string
$media_type = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\MediaType(); // \OpenAPI\Client\Model\MediaType
$culture_name = 'culture_name_example'; // string | The language culture name.  This tailors the response to a specific culture. i.e. language, units of measure, etc. Null assumes en-US. Valid values follows `ISO 639x`, ex: en-US, en-GB, fr-FR, etc.
$part_id = 'part_id_example'; // string
$class_type = array(56); // int[]
$environment = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\Environment(); // \OpenAPI\Client\Model\Environment
$real_product_id = 'real_product_id_example'; // string | Used when product id contains / character
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getMediaContentV100($supplier_code, $product_id, $media_type, $culture_name, $part_id, $class_type, $environment, $real_product_id, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaContentApi->getMediaContentV100: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | **string**|  | |
| **product_id** | **string**|  | |
| **media_type** | [**\OpenAPI\Client\Model\MediaType**](../Model/.md)|  | [optional] |
| **culture_name** | **string**| The language culture name.  This tailors the response to a specific culture. i.e. language, units of measure, etc. Null assumes en-US. Valid values follows &#x60;ISO 639x&#x60;, ex: en-US, en-GB, fr-FR, etc. | [optional] |
| **part_id** | **string**|  | [optional] |
| **class_type** | [**int[]**](../Model/int.md)|  | [optional] |
| **environment** | [**\OpenAPI\Client\Model\Environment**](../Model/.md)|  | [optional] |
| **real_product_id** | **string**| Used when product id contains / character | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\MediaContentDetailsResponse**](../Model/MediaContentDetailsResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getMediaContentV110()`

```php
getMediaContentV110($supplier_code, $product_id, $media_type, $culture_name, $part_id, $class_type, $environment, $real_product_id, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\MediaContentDetailsResponse
```

Get Media Content V110

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


$apiInstance = new OpenAPI\Client\Api\MediaContentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_code = 'supplier_code_example'; // string
$product_id = 'product_id_example'; // string
$media_type = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\MediaType(); // \OpenAPI\Client\Model\MediaType
$culture_name = 'culture_name_example'; // string | The language culture name.  This tailors the response to a specific culture. i.e. language, units of measure, etc. Null assumes en-US. Valid values follows `ISO 639x`, ex: en-US, en-GB, fr-FR, etc.
$part_id = 'part_id_example'; // string
$class_type = array(56); // int[]
$environment = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\Environment(); // \OpenAPI\Client\Model\Environment
$real_product_id = 'real_product_id_example'; // string | Used when product id contains / character
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getMediaContentV110($supplier_code, $product_id, $media_type, $culture_name, $part_id, $class_type, $environment, $real_product_id, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaContentApi->getMediaContentV110: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | **string**|  | |
| **product_id** | **string**|  | |
| **media_type** | [**\OpenAPI\Client\Model\MediaType**](../Model/.md)|  | [optional] |
| **culture_name** | **string**| The language culture name.  This tailors the response to a specific culture. i.e. language, units of measure, etc. Null assumes en-US. Valid values follows &#x60;ISO 639x&#x60;, ex: en-US, en-GB, fr-FR, etc. | [optional] |
| **part_id** | **string**|  | [optional] |
| **class_type** | [**int[]**](../Model/int.md)|  | [optional] |
| **environment** | [**\OpenAPI\Client\Model\Environment**](../Model/.md)|  | [optional] |
| **real_product_id** | **string**| Used when product id contains / character | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\MediaContentDetailsResponse**](../Model/MediaContentDetailsResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getMediaDateModified()`

```php
getMediaDateModified($supplier_code, $since, $culture_name, $environment, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\GetMediaDateModifiedResponse
```

Get Media Date Modified

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


$apiInstance = new OpenAPI\Client\Api\MediaContentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_code = 'supplier_code_example'; // string
$since = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime
$culture_name = 'culture_name_example'; // string | The language culture name.
$environment = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\Environment(); // \OpenAPI\Client\Model\Environment
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getMediaDateModified($supplier_code, $since, $culture_name, $environment, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaContentApi->getMediaDateModified: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | **string**|  | |
| **since** | **\DateTime**|  | |
| **culture_name** | **string**| The language culture name. | [optional] |
| **environment** | [**\OpenAPI\Client\Model\Environment**](../Model/.md)|  | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetMediaDateModifiedResponse**](../Model/GetMediaDateModifiedResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
