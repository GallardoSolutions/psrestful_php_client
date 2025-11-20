# OpenAPI\Client\PSMEDxApi



All URIs are relative to https://api.psrestful.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**classifyPsmedxV1ClassifyGet()**](PSMEDxApi.md#classifyPsmedxV1ClassifyGet) | **GET** /psmedx/v1/classify/ | Classify |
| [**decoratePsmedxV1DecorateGet()**](PSMEDxApi.md#decoratePsmedxV1DecorateGet) | **GET** /psmedx/v1/decorate/ | Decorate |
| [**drawBoundingBoxesPsmedxV1ShowBoundingBoxesGet()**](PSMEDxApi.md#drawBoundingBoxesPsmedxV1ShowBoundingBoxesGet) | **GET** /psmedx/v1/show-bounding-boxes/ | Draw Bounding Boxes |
| [**findAndShowBboxPsmedxV1FindAndShowBoundingBoxGet()**](PSMEDxApi.md#findAndShowBboxPsmedxV1FindAndShowBoundingBoxGet) | **GET** /psmedx/v1/find-and-show-bounding-box/ | Find And Show Bbox |
| [**findBboxPsmedxV1FindBoundingBoxGet()**](PSMEDxApi.md#findBboxPsmedxV1FindBoundingBoxGet) | **GET** /psmedx/v1/find-bounding-box/ | Find Bbox |
| [**getTopColorsPsmedxV1ImageColorsGet()**](PSMEDxApi.md#getTopColorsPsmedxV1ImageColorsGet) | **GET** /psmedx/v1/image/colors/ | Get Top Colors |
| [**imageInfoPsmedxV1ImageInfoGet()**](PSMEDxApi.md#imageInfoPsmedxV1ImageInfoGet) | **GET** /psmedx/v1/image-info/ | Image Info |
| [**nearestPantonePsmedxV1NearestPantoneGet()**](PSMEDxApi.md#nearestPantonePsmedxV1NearestPantoneGet) | **GET** /psmedx/v1/nearest-pantone/ | Nearest Pantone |
| [**pantoneToHexPsmedxV1PantoneToHexGet()**](PSMEDxApi.md#pantoneToHexPsmedxV1PantoneToHexGet) | **GET** /psmedx/v1/pantone-to-hex/ | Pantone To Hex |
| [**removeBgViewPsmedxV1RemoveBackgroundGet()**](PSMEDxApi.md#removeBgViewPsmedxV1RemoveBackgroundGet) | **GET** /psmedx/v1/remove-background/ | Remove Bg View |
| [**vectorizeImagePsmedxV1VectorizeGet()**](PSMEDxApi.md#vectorizeImagePsmedxV1VectorizeGet) | **GET** /psmedx/v1/vectorize/ | Vectorize Image |


## `classifyPsmedxV1ClassifyGet()`

```php
classifyPsmedxV1ClassifyGet($image_url, $part_colors_json, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\ClassificationResult
```

Classify

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


$apiInstance = new OpenAPI\Client\Api\PSMEDxApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$image_url = 'image_url_example'; // string
$part_colors_json = 'part_colors_json_example'; // string
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->classifyPsmedxV1ClassifyGet($image_url, $part_colors_json, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PSMEDxApi->classifyPsmedxV1ClassifyGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **image_url** | **string**|  | |
| **part_colors_json** | **string**|  | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ClassificationResult**](../Model/ClassificationResult.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `decoratePsmedxV1DecorateGet()`

```php
decoratePsmedxV1DecorateGet($blank_url, $artwork_url, $bounding_box_json, $placement, $emboss, $quality, $max_width, $max_height, $x_forwarded_for, $x_account_id, $body)
```

Decorate

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


$apiInstance = new OpenAPI\Client\Api\PSMEDxApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$blank_url = 'blank_url_example'; // string
$artwork_url = 'artwork_url_example'; // string
$bounding_box_json = 'bounding_box_json_example'; // string
$placement = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\PlacementOptions(); // \OpenAPI\Client\Model\PlacementOptions
$emboss = false; // bool
$quality = 85; // int | Image compression quality (1-100)
$max_width = 2000; // int | Maximum width in pixels
$max_height = 2000; // int | Maximum height in pixels
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $apiInstance->decoratePsmedxV1DecorateGet($blank_url, $artwork_url, $bounding_box_json, $placement, $emboss, $quality, $max_width, $max_height, $x_forwarded_for, $x_account_id, $body);
} catch (Exception $e) {
    echo 'Exception when calling PSMEDxApi->decoratePsmedxV1DecorateGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **blank_url** | **string**|  | |
| **artwork_url** | **string**|  | |
| **bounding_box_json** | **string**|  | |
| **placement** | [**\OpenAPI\Client\Model\PlacementOptions**](../Model/.md)|  | [optional] |
| **emboss** | **bool**|  | [optional] [default to false] |
| **quality** | **int**| Image compression quality (1-100) | [optional] [default to 85] |
| **max_width** | **int**| Maximum width in pixels | [optional] [default to 2000] |
| **max_height** | **int**| Maximum height in pixels | [optional] [default to 2000] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

void (empty response body)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `image/png`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `drawBoundingBoxesPsmedxV1ShowBoundingBoxesGet()`

```php
drawBoundingBoxesPsmedxV1ShowBoundingBoxesGet($image_url, $bounding_boxes_json, $x_forwarded_for, $x_account_id, $body)
```

Draw Bounding Boxes

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


$apiInstance = new OpenAPI\Client\Api\PSMEDxApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$image_url = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\ImageUrl(); // \OpenAPI\Client\Model\ImageUrl
$bounding_boxes_json = 'bounding_boxes_json_example'; // string
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $apiInstance->drawBoundingBoxesPsmedxV1ShowBoundingBoxesGet($image_url, $bounding_boxes_json, $x_forwarded_for, $x_account_id, $body);
} catch (Exception $e) {
    echo 'Exception when calling PSMEDxApi->drawBoundingBoxesPsmedxV1ShowBoundingBoxesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **image_url** | [**\OpenAPI\Client\Model\ImageUrl**](../Model/.md)|  | |
| **bounding_boxes_json** | **string**|  | |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

void (empty response body)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `image/png`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `findAndShowBboxPsmedxV1FindAndShowBoundingBoxGet()`

```php
findAndShowBboxPsmedxV1FindAndShowBoundingBoxGet($blank_url, $decorated_url, $x_forwarded_for, $x_account_id, $body)
```

Find And Show Bbox

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


$apiInstance = new OpenAPI\Client\Api\PSMEDxApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$blank_url = 'blank_url_example'; // string
$decorated_url = 'decorated_url_example'; // string
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $apiInstance->findAndShowBboxPsmedxV1FindAndShowBoundingBoxGet($blank_url, $decorated_url, $x_forwarded_for, $x_account_id, $body);
} catch (Exception $e) {
    echo 'Exception when calling PSMEDxApi->findAndShowBboxPsmedxV1FindAndShowBoundingBoxGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **blank_url** | **string**|  | |
| **decorated_url** | **string**|  | |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

void (empty response body)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `image/png`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `findBboxPsmedxV1FindBoundingBoxGet()`

```php
findBboxPsmedxV1FindBoundingBoxGet($blank_url, $decorated_url, $x_forwarded_for, $x_account_id, $body)
```

Find Bbox

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


$apiInstance = new OpenAPI\Client\Api\PSMEDxApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$blank_url = 'blank_url_example'; // string
$decorated_url = 'decorated_url_example'; // string
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $apiInstance->findBboxPsmedxV1FindBoundingBoxGet($blank_url, $decorated_url, $x_forwarded_for, $x_account_id, $body);
} catch (Exception $e) {
    echo 'Exception when calling PSMEDxApi->findBboxPsmedxV1FindBoundingBoxGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **blank_url** | **string**|  | |
| **decorated_url** | **string**|  | |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

void (empty response body)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `image/png`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTopColorsPsmedxV1ImageColorsGet()`

```php
getTopColorsPsmedxV1ImageColorsGet($image_url, $top_n_colors, $remove_bg, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\ColorsResponse
```

Get Top Colors

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


$apiInstance = new OpenAPI\Client\Api\PSMEDxApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$image_url = 'image_url_example'; // string
$top_n_colors = 56; // int
$remove_bg = True; // bool
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getTopColorsPsmedxV1ImageColorsGet($image_url, $top_n_colors, $remove_bg, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PSMEDxApi->getTopColorsPsmedxV1ImageColorsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **image_url** | **string**|  | |
| **top_n_colors** | **int**|  | [optional] |
| **remove_bg** | **bool**|  | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ColorsResponse**](../Model/ColorsResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `imageInfoPsmedxV1ImageInfoGet()`

```php
imageInfoPsmedxV1ImageInfoGet($image_url, $original_width_in, $original_height_in, $x_forwarded_for, $x_account_id, $body): mixed
```

Image Info

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


$apiInstance = new OpenAPI\Client\Api\PSMEDxApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$image_url = 'image_url_example'; // string
$original_width_in = 3.4; // float | Original width in inches
$original_height_in = 3.4; // float | Original height in inches
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->imageInfoPsmedxV1ImageInfoGet($image_url, $original_width_in, $original_height_in, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PSMEDxApi->imageInfoPsmedxV1ImageInfoGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **image_url** | **string**|  | |
| **original_width_in** | **float**| Original width in inches | [optional] |
| **original_height_in** | **float**| Original height in inches | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

**mixed**

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `nearestPantonePsmedxV1NearestPantoneGet()`

```php
nearestPantonePsmedxV1NearestPantoneGet($hex_color, $x_forwarded_for, $x_account_id, $body): mixed
```

Nearest Pantone

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


$apiInstance = new OpenAPI\Client\Api\PSMEDxApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$hex_color = array('hex_color_example'); // string[]
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->nearestPantonePsmedxV1NearestPantoneGet($hex_color, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PSMEDxApi->nearestPantonePsmedxV1NearestPantoneGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **hex_color** | [**string[]**](../Model/string.md)|  | |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

**mixed**

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pantoneToHexPsmedxV1PantoneToHexGet()`

```php
pantoneToHexPsmedxV1PantoneToHexGet($pantone, $x_forwarded_for, $x_account_id, $body): mixed
```

Pantone To Hex

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


$apiInstance = new OpenAPI\Client\Api\PSMEDxApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$pantone = array('pantone_example'); // string[]
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->pantoneToHexPsmedxV1PantoneToHexGet($pantone, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PSMEDxApi->pantoneToHexPsmedxV1PantoneToHexGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **pantone** | [**string[]**](../Model/string.md)|  | |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

**mixed**

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `removeBgViewPsmedxV1RemoveBackgroundGet()`

```php
removeBgViewPsmedxV1RemoveBackgroundGet($image_url, $quality, $max_width, $max_height, $x_forwarded_for, $x_account_id, $body)
```

Remove Bg View

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


$apiInstance = new OpenAPI\Client\Api\PSMEDxApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$image_url = 'image_url_example'; // string
$quality = 85; // int | Image compression quality (1-100)
$max_width = 2000; // int | Maximum width in pixels
$max_height = 2000; // int | Maximum height in pixels
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $apiInstance->removeBgViewPsmedxV1RemoveBackgroundGet($image_url, $quality, $max_width, $max_height, $x_forwarded_for, $x_account_id, $body);
} catch (Exception $e) {
    echo 'Exception when calling PSMEDxApi->removeBgViewPsmedxV1RemoveBackgroundGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **image_url** | **string**|  | |
| **quality** | **int**| Image compression quality (1-100) | [optional] [default to 85] |
| **max_width** | **int**| Maximum width in pixels | [optional] [default to 2000] |
| **max_height** | **int**| Maximum height in pixels | [optional] [default to 2000] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

void (empty response body)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `image/png`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `vectorizeImagePsmedxV1VectorizeGet()`

```php
vectorizeImagePsmedxV1VectorizeGet($image_url, $colormode, $hierarchical, $mode, $filter_speckle, $color_precision, $layer_difference, $corner_threshold, $length_threshold, $max_iterations, $splice_threshold, $path_precision, $x_forwarded_for, $x_account_id, $body): mixed
```

Vectorize Image

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


$apiInstance = new OpenAPI\Client\Api\PSMEDxApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$image_url = 'image_url_example'; // string
$colormode = 'color'; // string
$hierarchical = 'stacked'; // string
$mode = 'spline'; // string
$filter_speckle = 4; // int
$color_precision = 6; // int
$layer_difference = 16; // int
$corner_threshold = 60; // int
$length_threshold = 4.0; // float
$max_iterations = 10; // int
$splice_threshold = 45; // int
$path_precision = 3; // int
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->vectorizeImagePsmedxV1VectorizeGet($image_url, $colormode, $hierarchical, $mode, $filter_speckle, $color_precision, $layer_difference, $corner_threshold, $length_threshold, $max_iterations, $splice_threshold, $path_precision, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PSMEDxApi->vectorizeImagePsmedxV1VectorizeGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **image_url** | **string**|  | |
| **colormode** | **string**|  | [optional] [default to &#39;color&#39;] |
| **hierarchical** | **string**|  | [optional] [default to &#39;stacked&#39;] |
| **mode** | **string**|  | [optional] [default to &#39;spline&#39;] |
| **filter_speckle** | **int**|  | [optional] [default to 4] |
| **color_precision** | **int**|  | [optional] [default to 6] |
| **layer_difference** | **int**|  | [optional] [default to 16] |
| **corner_threshold** | **int**|  | [optional] [default to 60] |
| **length_threshold** | **float**|  | [optional] [default to 4.0] |
| **max_iterations** | **int**|  | [optional] [default to 10] |
| **splice_threshold** | **int**|  | [optional] [default to 45] |
| **path_precision** | **int**|  | [optional] [default to 3] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

**mixed**

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
