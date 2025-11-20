# OpenAPI\Client\ExtraApi



All URIs are relative to https://api.psrestful.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getBrandsExtraV1BrandsGet()**](ExtraApi.md#getBrandsExtraV1BrandsGet) | **GET** /extra/v1/brands | Get Brands |
| [**getBrandsV2()**](ExtraApi.md#getBrandsV2) | **GET** /extra/v2/brands | Get Brands |
| [**getCategoriesV2()**](ExtraApi.md#getCategoriesV2) | **GET** /extra/v2/categories | Get Categories |
| [**getClassificationsExtraV1ProductsExtraIdClassificationsGet()**](ExtraApi.md#getClassificationsExtraV1ProductsExtraIdClassificationsGet) | **GET** /extra/v1/products/{extra_id}/classifications | Get Classifications |
| [**getCombinedPpcs()**](ExtraApi.md#getCombinedPpcs) | **GET** /extra/v2/products/{product_id}/ppcs | Get Combined Ppcs |
| [**getDecorationsExtraV1SuppliersSupplierCodeDecorationsGet()**](ExtraApi.md#getDecorationsExtraV1SuppliersSupplierCodeDecorationsGet) | **GET** /extra/v1/suppliers/{supplier_code}/decorations | Get Decorations |
| [**getExtraId()**](ExtraApi.md#getExtraId) | **GET** /extra/v2/products/get-extra-id/ | Get Extra Id |
| [**getInventoryV2()**](ExtraApi.md#getInventoryV2) | **GET** /extra/v2/inventory/{supplier_code} | Get Inventory |
| [**getMetafieldsByTitle()**](ExtraApi.md#getMetafieldsByTitle) | **GET** /extra/v2/products/get-metafields-by-title/ | Get Metafields By Title |
| [**getPartIdMappingsV2()**](ExtraApi.md#getPartIdMappingsV2) | **GET** /extra/v2/part-id-mappings | Get Part Id Mappings |
| [**getProductExtraV1ProductsProductIdGet()**](ExtraApi.md#getProductExtraV1ProductsProductIdGet) | **GET** /extra/v1/products/{product_id} | Get Product |
| [**getProductMetafieldsV2()**](ExtraApi.md#getProductMetafieldsV2) | **GET** /extra/v2/products/metafields | Get Product Metafields |
| [**getProductPartsExtraV1ProductsProductIdSortedPartsGet()**](ExtraApi.md#getProductPartsExtraV1ProductsProductIdSortedPartsGet) | **GET** /extra/v1/products/{product_id}/sorted-parts | Get Product Parts |
| [**getProductV2()**](ExtraApi.md#getProductV2) | **GET** /extra/v2/products/{product_id} | Get Product |
| [**getProducts()**](ExtraApi.md#getProducts) | **GET** /extra/v1/products | Get Products |
| [**getProductsV2()**](ExtraApi.md#getProductsV2) | **GET** /extra/v2/products | Get Products |
| [**getSuppliersExtraV1SuppliersGet()**](ExtraApi.md#getSuppliersExtraV1SuppliersGet) | **GET** /extra/v1/suppliers | Get Suppliers |
| [**getSuppliersV2()**](ExtraApi.md#getSuppliersV2) | **GET** /extra/v2/suppliers | Get Suppliers |
| [**scrapeExtraV1ScrapeSupplierCodeGet()**](ExtraApi.md#scrapeExtraV1ScrapeSupplierCodeGet) | **GET** /extra/v1/scrape/{supplier_code}/ | Scrape |


## `getBrandsExtraV1BrandsGet()`

```php
getBrandsExtraV1BrandsGet($supplier_id, $supplier_code, $x_account_id, $body): \OpenAPI\Client\Model\BrandResponse
```

Get Brands

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


$apiInstance = new OpenAPI\Client\Api\ExtraApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_id = 56; // int
$supplier_code = 'supplier_code_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getBrandsExtraV1BrandsGet($supplier_id, $supplier_code, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExtraApi->getBrandsExtraV1BrandsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_id** | **int**|  | [optional] |
| **supplier_code** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\BrandResponse**](../Model/BrandResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getBrandsV2()`

```php
getBrandsV2($page, $page_size, $supplier_id, $supplier_code, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\BrandsResponseV2
```

Get Brands

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


$apiInstance = new OpenAPI\Client\Api\ExtraApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int
$page_size = 800; // int
$supplier_id = 56; // int
$supplier_code = 'supplier_code_example'; // string
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getBrandsV2($page, $page_size, $supplier_id, $supplier_code, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExtraApi->getBrandsV2: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] [default to 1] |
| **page_size** | **int**|  | [optional] [default to 800] |
| **supplier_id** | **int**|  | [optional] |
| **supplier_code** | **string**|  | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\BrandsResponseV2**](../Model/BrandsResponseV2.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCategoriesV2()`

```php
getCategoriesV2($page, $page_size, $supplier_id, $supplier_code, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\CategoriesResponseV2
```

Get Categories

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


$apiInstance = new OpenAPI\Client\Api\ExtraApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int
$page_size = 50; // int
$supplier_id = 56; // int
$supplier_code = 'supplier_code_example'; // string
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getCategoriesV2($page, $page_size, $supplier_id, $supplier_code, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExtraApi->getCategoriesV2: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] [default to 1] |
| **page_size** | **int**|  | [optional] [default to 50] |
| **supplier_id** | **int**|  | [optional] |
| **supplier_code** | **string**|  | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\CategoriesResponseV2**](../Model/CategoriesResponseV2.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getClassificationsExtraV1ProductsExtraIdClassificationsGet()`

```php
getClassificationsExtraV1ProductsExtraIdClassificationsGet($extra_id, $x_account_id, $body): \OpenAPI\Client\Model\ClassifiersResponse
```

Get Classifications

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


$apiInstance = new OpenAPI\Client\Api\ExtraApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$extra_id = 56; // int
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getClassificationsExtraV1ProductsExtraIdClassificationsGet($extra_id, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExtraApi->getClassificationsExtraV1ProductsExtraIdClassificationsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **extra_id** | **int**|  | |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ClassifiersResponse**](../Model/ClassifiersResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCombinedPpcs()`

```php
getCombinedPpcs($product_id, $fob_point_id, $currency, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\CombinedPPC
```

Get Combined Ppcs

Get combined PPC data with list, net, and customer prices for a product. This endpoint fetches PPC data concurrently for all three price types and combines them.

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


$apiInstance = new OpenAPI\Client\Api\ExtraApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$product_id = 56; // int
$fob_point_id = 'fob_point_id_example'; // string | FOB Point ID
$currency = 'USD'; // string | Currency for pricing (USD or CAD)
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getCombinedPpcs($product_id, $fob_point_id, $currency, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExtraApi->getCombinedPpcs: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **product_id** | **int**|  | |
| **fob_point_id** | **string**| FOB Point ID | |
| **currency** | **string**| Currency for pricing (USD or CAD) | [optional] [default to &#39;USD&#39;] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\CombinedPPC**](../Model/CombinedPPC.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getDecorationsExtraV1SuppliersSupplierCodeDecorationsGet()`

```php
getDecorationsExtraV1SuppliersSupplierCodeDecorationsGet($supplier_code, $currency, $x_account_id, $body): \OpenAPI\Client\Model\DecorationsResponse
```

Get Decorations

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


$apiInstance = new OpenAPI\Client\Api\ExtraApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_code = 'supplier_code_example'; // string
$currency = 'USD'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getDecorationsExtraV1SuppliersSupplierCodeDecorationsGet($supplier_code, $currency, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExtraApi->getDecorationsExtraV1SuppliersSupplierCodeDecorationsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | **string**|  | |
| **currency** | **string**|  | [optional] [default to &#39;USD&#39;] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\DecorationsResponse**](../Model/DecorationsResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getExtraId()`

```php
getExtraId($supplier_code, $product_id, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\ProductMetafields
```

Get Extra Id

Get the extra ID for a product given its supplier code and product ID.  Returns: - extra_id: The internal extra product ID - supplier_code: The supplier code - product_id: The supplier's product ID

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


$apiInstance = new OpenAPI\Client\Api\ExtraApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_code = 'supplier_code_example'; // string | Supplier code
$product_id = 'product_id_example'; // string | Product ID
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getExtraId($supplier_code, $product_id, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExtraApi->getExtraId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | **string**| Supplier code | |
| **product_id** | **string**| Product ID | |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProductMetafields**](../Model/ProductMetafields.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getInventoryV2()`

```php
getInventoryV2($supplier_code, $page, $page_size, $product_id, $part_id, $last_modified__since, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\InventoryListResponseV2
```

Get Inventory

Get inventory records for a supplier with optional filters.  Query parameters: - page: Page number (default: 1) - page_size: Items per page (default: 100, max: 500) - product_id: Filter by specific product ID - part_id: Filter by specific part ID - last_modified__since: Filter by last modified time (e.g., '1h', '30m', '2d')  Returns paginated inventory records ordered by last_modified (most recent first).

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


$apiInstance = new OpenAPI\Client\Api\ExtraApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_code = 'supplier_code_example'; // string
$page = 1; // int
$page_size = 100; // int
$product_id = 'product_id_example'; // string
$part_id = 'part_id_example'; // string
$last_modified__since = 'last_modified__since_example'; // string
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getInventoryV2($supplier_code, $page, $page_size, $product_id, $part_id, $last_modified__since, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExtraApi->getInventoryV2: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | **string**|  | |
| **page** | **int**|  | [optional] [default to 1] |
| **page_size** | **int**|  | [optional] [default to 100] |
| **product_id** | **string**|  | [optional] |
| **part_id** | **string**|  | [optional] |
| **last_modified__since** | **string**|  | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\InventoryListResponseV2**](../Model/InventoryListResponseV2.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getMetafieldsByTitle()`

```php
getMetafieldsByTitle($supplier_code, $title, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\ProductMetafields
```

Get Metafields By Title

Get product metafields given a supplier code and title.  Returns: - ProductMetafields with extra_id, supplier_code, and product_id - 404 if not found

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


$apiInstance = new OpenAPI\Client\Api\ExtraApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_code = 'supplier_code_example'; // string | Supplier code
$title = 'title_example'; // string | Product title
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getMetafieldsByTitle($supplier_code, $title, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExtraApi->getMetafieldsByTitle: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | **string**| Supplier code | |
| **title** | **string**| Product title | |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProductMetafields**](../Model/ProductMetafields.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getPartIdMappingsV2()`

```php
getPartIdMappingsV2($page, $page_size, $supplier, $supplier_code, $product_id, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\PartIDMappingListResponseV2
```

Get Part Id Mappings

Get part ID mappings for a supplier with optional product ID filter.  Query parameters: - supplier: Supplier ID - supplier_code: Supplier code - product_id: Filter by specific product ID (optional) - page: Page number (default: 1) - page_size: Items per page (default: 50, max: 200)  Returns paginated part ID mapping records with mappings for med_id, inv_id, and ppc_id.

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


$apiInstance = new OpenAPI\Client\Api\ExtraApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int
$page_size = 50; // int
$supplier = 56; // int
$supplier_code = 'supplier_code_example'; // string
$product_id = 'product_id_example'; // string
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getPartIdMappingsV2($page, $page_size, $supplier, $supplier_code, $product_id, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExtraApi->getPartIdMappingsV2: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] [default to 1] |
| **page_size** | **int**|  | [optional] [default to 50] |
| **supplier** | **int**|  | [optional] |
| **supplier_code** | **string**|  | [optional] |
| **product_id** | **string**|  | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PartIDMappingListResponseV2**](../Model/PartIDMappingListResponseV2.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getProductExtraV1ProductsProductIdGet()`

```php
getProductExtraV1ProductsProductIdGet($product_id, $expand, $currency, $country, $language, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\ExtraProduct
```

Get Product

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


$apiInstance = new OpenAPI\Client\Api\ExtraApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$product_id = 56; // int
$expand = array('expand_example'); // string[] | Fields to expand in the product response
$currency = 'USD'; // string
$country = 'US'; // string
$language = 'en'; // string
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getProductExtraV1ProductsProductIdGet($product_id, $expand, $currency, $country, $language, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExtraApi->getProductExtraV1ProductsProductIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **product_id** | **int**|  | |
| **expand** | [**string[]**](../Model/string.md)| Fields to expand in the product response | [optional] |
| **currency** | **string**|  | [optional] [default to &#39;USD&#39;] |
| **country** | **string**|  | [optional] [default to &#39;US&#39;] |
| **language** | **string**|  | [optional] [default to &#39;en&#39;] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ExtraProduct**](../Model/ExtraProduct.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getProductMetafieldsV2()`

```php
getProductMetafieldsV2($extra_id, $page, $page_size, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\ProductMetafieldsListResponseV2
```

Get Product Metafields

Get product metafields (extra_id, supplier_code, product_id) by extra IDs.  Query parameters: - extra_id: Comma-separated list of extra IDs (required), e.g., '21832,21833,21834' - page: Page number (default: 1) - page_size: Items per page (default: 100, max: 500)  Returns paginated product metafields with camelCase formatting.

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


$apiInstance = new OpenAPI\Client\Api\ExtraApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$extra_id = 'extra_id_example'; // string
$page = 1; // int
$page_size = 100; // int
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getProductMetafieldsV2($extra_id, $page, $page_size, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExtraApi->getProductMetafieldsV2: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **extra_id** | **string**|  | |
| **page** | **int**|  | [optional] [default to 1] |
| **page_size** | **int**|  | [optional] [default to 100] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProductMetafieldsListResponseV2**](../Model/ProductMetafieldsListResponseV2.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getProductPartsExtraV1ProductsProductIdSortedPartsGet()`

```php
getProductPartsExtraV1ProductsProductIdSortedPartsGet($product_id, $days, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\VariantResponse
```

Get Product Parts

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


$apiInstance = new OpenAPI\Client\Api\ExtraApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$product_id = 56; // int
$days = 60; // int | Number of days to look back
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getProductPartsExtraV1ProductsProductIdSortedPartsGet($product_id, $days, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExtraApi->getProductPartsExtraV1ProductsProductIdSortedPartsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **product_id** | **int**|  | |
| **days** | **int**| Number of days to look back | [optional] [default to 60] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\VariantResponse**](../Model/VariantResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getProductV2()`

```php
getProductV2($product_id, $expand, $currency, $country, $language, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\ExtraProductV2
```

Get Product

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


$apiInstance = new OpenAPI\Client\Api\ExtraApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$product_id = 56; // int
$expand = array('expand_example'); // string[] | Fields to expand in the product response
$currency = 'USD'; // string
$country = 'US'; // string
$language = 'en'; // string
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getProductV2($product_id, $expand, $currency, $country, $language, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExtraApi->getProductV2: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **product_id** | **int**|  | |
| **expand** | [**string[]**](../Model/string.md)| Fields to expand in the product response | [optional] |
| **currency** | **string**|  | [optional] [default to &#39;USD&#39;] |
| **country** | **string**|  | [optional] [default to &#39;US&#39;] |
| **language** | **string**|  | [optional] [default to &#39;en&#39;] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ExtraProductV2**](../Model/ExtraProductV2.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getProducts()`

```php
getProducts($supplier, $supplier_code, $product_id, $extra_id, $brand, $export, $is_caution, $is_closeout, $country_of_origin, $primary_material, $lead_time, $lead_time__range, $min_qty__range, $is_rush_service, $rush_service_lead_time, $is_on_demand, $main_category, $list_price__range, $apparel_style, $shop, $search, $ordering, $limit, $offset, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\ProductListResponse
```

Get Products

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


$apiInstance = new OpenAPI\Client\Api\ExtraApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier = 56; // int
$supplier_code = 'supplier_code_example'; // string
$product_id = 'product_id_example'; // string
$extra_id = 'extra_id_example'; // string
$brand = 56; // int
$export = True; // bool
$is_caution = True; // bool
$is_closeout = True; // bool
$country_of_origin = 'country_of_origin_example'; // string
$primary_material = 'primary_material_example'; // string
$lead_time = 56; // int
$lead_time__range = 'lead_time__range_example'; // string
$min_qty__range = 'min_qty__range_example'; // string
$is_rush_service = True; // bool
$rush_service_lead_time = 56; // int
$is_on_demand = True; // bool
$main_category = 'main_category_example'; // string
$list_price__range = 'list_price__range_example'; // string
$apparel_style = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\ApparelStyle(); // \OpenAPI\Client\Model\ApparelStyle
$shop = 56; // int
$search = 'search_example'; // string
$ordering = 'ordering_example'; // string
$limit = 10; // int
$offset = 0; // int
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getProducts($supplier, $supplier_code, $product_id, $extra_id, $brand, $export, $is_caution, $is_closeout, $country_of_origin, $primary_material, $lead_time, $lead_time__range, $min_qty__range, $is_rush_service, $rush_service_lead_time, $is_on_demand, $main_category, $list_price__range, $apparel_style, $shop, $search, $ordering, $limit, $offset, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExtraApi->getProducts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier** | **int**|  | [optional] |
| **supplier_code** | **string**|  | [optional] |
| **product_id** | **string**|  | [optional] |
| **extra_id** | **string**|  | [optional] |
| **brand** | **int**|  | [optional] |
| **export** | **bool**|  | [optional] |
| **is_caution** | **bool**|  | [optional] |
| **is_closeout** | **bool**|  | [optional] |
| **country_of_origin** | **string**|  | [optional] |
| **primary_material** | **string**|  | [optional] |
| **lead_time** | **int**|  | [optional] |
| **lead_time__range** | **string**|  | [optional] |
| **min_qty__range** | **string**|  | [optional] |
| **is_rush_service** | **bool**|  | [optional] |
| **rush_service_lead_time** | **int**|  | [optional] |
| **is_on_demand** | **bool**|  | [optional] |
| **main_category** | **string**|  | [optional] |
| **list_price__range** | **string**|  | [optional] |
| **apparel_style** | [**\OpenAPI\Client\Model\ApparelStyle**](../Model/.md)|  | [optional] |
| **shop** | **int**|  | [optional] |
| **search** | **string**|  | [optional] |
| **ordering** | **string**|  | [optional] |
| **limit** | **int**|  | [optional] [default to 10] |
| **offset** | **int**|  | [optional] [default to 0] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProductListResponse**](../Model/ProductListResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getProductsV2()`

```php
getProductsV2($page, $page_size, $supplier, $supplier_code, $product_id, $extra_id, $brand, $export, $is_caution, $is_closeout, $country_of_origin, $primary_material, $lead_time, $lead_time__range, $min_qty__range, $is_rush_service, $rush_service_lead_time, $is_on_demand, $main_category, $list_price__range, $apparel_style, $shop, $search, $ordering, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\ProductListResponseV2
```

Get Products

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


$apiInstance = new OpenAPI\Client\Api\ExtraApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int
$page_size = 10; // int
$supplier = 56; // int
$supplier_code = 'supplier_code_example'; // string
$product_id = 'product_id_example'; // string
$extra_id = 'extra_id_example'; // string
$brand = 56; // int
$export = True; // bool
$is_caution = True; // bool
$is_closeout = True; // bool
$country_of_origin = 'country_of_origin_example'; // string
$primary_material = 'primary_material_example'; // string
$lead_time = 56; // int
$lead_time__range = 'lead_time__range_example'; // string
$min_qty__range = 'min_qty__range_example'; // string
$is_rush_service = True; // bool
$rush_service_lead_time = 56; // int
$is_on_demand = True; // bool
$main_category = 'main_category_example'; // string
$list_price__range = 'list_price__range_example'; // string
$apparel_style = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\ApparelStyle(); // \OpenAPI\Client\Model\ApparelStyle
$shop = 56; // int
$search = 'search_example'; // string
$ordering = 'ordering_example'; // string
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getProductsV2($page, $page_size, $supplier, $supplier_code, $product_id, $extra_id, $brand, $export, $is_caution, $is_closeout, $country_of_origin, $primary_material, $lead_time, $lead_time__range, $min_qty__range, $is_rush_service, $rush_service_lead_time, $is_on_demand, $main_category, $list_price__range, $apparel_style, $shop, $search, $ordering, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExtraApi->getProductsV2: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] [default to 1] |
| **page_size** | **int**|  | [optional] [default to 10] |
| **supplier** | **int**|  | [optional] |
| **supplier_code** | **string**|  | [optional] |
| **product_id** | **string**|  | [optional] |
| **extra_id** | **string**|  | [optional] |
| **brand** | **int**|  | [optional] |
| **export** | **bool**|  | [optional] |
| **is_caution** | **bool**|  | [optional] |
| **is_closeout** | **bool**|  | [optional] |
| **country_of_origin** | **string**|  | [optional] |
| **primary_material** | **string**|  | [optional] |
| **lead_time** | **int**|  | [optional] |
| **lead_time__range** | **string**|  | [optional] |
| **min_qty__range** | **string**|  | [optional] |
| **is_rush_service** | **bool**|  | [optional] |
| **rush_service_lead_time** | **int**|  | [optional] |
| **is_on_demand** | **bool**|  | [optional] |
| **main_category** | **string**|  | [optional] |
| **list_price__range** | **string**|  | [optional] |
| **apparel_style** | [**\OpenAPI\Client\Model\ApparelStyle**](../Model/.md)|  | [optional] |
| **shop** | **int**|  | [optional] |
| **search** | **string**|  | [optional] |
| **ordering** | **string**|  | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProductListResponseV2**](../Model/ProductListResponseV2.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSuppliersExtraV1SuppliersGet()`

```php
getSuppliersExtraV1SuppliersGet($shopify_ready, $credentials_available, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\SuppliersResponse
```

Get Suppliers

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


$apiInstance = new OpenAPI\Client\Api\ExtraApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$shopify_ready = True; // bool | Filter by Shopify readiness
$credentials_available = True; // bool | Filter by credentials availability
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getSuppliersExtraV1SuppliersGet($shopify_ready, $credentials_available, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExtraApi->getSuppliersExtraV1SuppliersGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **shopify_ready** | **bool**| Filter by Shopify readiness | [optional] |
| **credentials_available** | **bool**| Filter by credentials availability | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\SuppliersResponse**](../Model/SuppliersResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSuppliersV2()`

```php
getSuppliersV2($page, $page_size, $shopify_ready, $credentials_available, $decorations_available, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\SuppliersResponseV2
```

Get Suppliers

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


$apiInstance = new OpenAPI\Client\Api\ExtraApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int
$page_size = 600; // int
$shopify_ready = True; // bool
$credentials_available = True; // bool
$decorations_available = True; // bool
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getSuppliersV2($page, $page_size, $shopify_ready, $credentials_available, $decorations_available, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExtraApi->getSuppliersV2: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] [default to 1] |
| **page_size** | **int**|  | [optional] [default to 600] |
| **shopify_ready** | **bool**|  | [optional] |
| **credentials_available** | **bool**|  | [optional] |
| **decorations_available** | **bool**|  | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\SuppliersResponseV2**](../Model/SuppliersResponseV2.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scrapeExtraV1ScrapeSupplierCodeGet()`

```php
scrapeExtraV1ScrapeSupplierCodeGet($supplier_code, $url, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\ScraperResponse
```

Scrape

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


$apiInstance = new OpenAPI\Client\Api\ExtraApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_code = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\ScraperSupplierCodes(); // \OpenAPI\Client\Model\ScraperSupplierCodes
$url = 'url_example'; // string
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->scrapeExtraV1ScrapeSupplierCodeGet($supplier_code, $url, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExtraApi->scrapeExtraV1ScrapeSupplierCodeGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | [**\OpenAPI\Client\Model\ScraperSupplierCodes**](../Model/.md)|  | |
| **url** | **string**|  | |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ScraperResponse**](../Model/ScraperResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
