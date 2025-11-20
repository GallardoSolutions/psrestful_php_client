# OpenAPI\Client\InvoiceApi



All URIs are relative to https://api.psrestful.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getInvoices()**](InvoiceApi.md#getInvoices) | **GET** /v1.0.0/suppliers/{supplier_code}/invoices | Get Invoices |
| [**getVoidedInvoices()**](InvoiceApi.md#getVoidedInvoices) | **GET** /v1.0.0/suppliers/{supplier_code}/voided-invoices | Get Voided Invoices |


## `getInvoices()`

```php
getInvoices($supplier_code, $query_type, $reference_number, $requested_date, $available_timestamp, $environment, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\GetInvoiceResponse
```

Get Invoices

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


$apiInstance = new OpenAPI\Client\Api\InvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_code = 'supplier_code_example'; // string
$query_type = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\INVCQueryType(); // \OpenAPI\Client\Model\INVCQueryType
$reference_number = 'reference_number_example'; // string
$requested_date = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime
$available_timestamp = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime
$environment = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\Environment(); // \OpenAPI\Client\Model\Environment
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getInvoices($supplier_code, $query_type, $reference_number, $requested_date, $available_timestamp, $environment, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoiceApi->getInvoices: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | **string**|  | |
| **query_type** | [**\OpenAPI\Client\Model\INVCQueryType**](../Model/.md)|  | |
| **reference_number** | **string**|  | [optional] |
| **requested_date** | **\DateTime**|  | [optional] |
| **available_timestamp** | **\DateTime**|  | [optional] |
| **environment** | [**\OpenAPI\Client\Model\Environment**](../Model/.md)|  | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetInvoiceResponse**](../Model/GetInvoiceResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getVoidedInvoices()`

```php
getVoidedInvoices($supplier_code, $query_type, $reference_number, $requested_date, $available_timestamp, $environment, $x_forwarded_for, $x_account_id, $body): \OpenAPI\Client\Model\GetVoidedResponse
```

Get Voided Invoices

This endpoint is used to retrieve a list of voided invoices. When QueryType=1(PO_NUMBER_SEARCH) or 2(INVOICE_NUMBER_SEARCH) reference_number must be filled in.

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


$apiInstance = new OpenAPI\Client\Api\InvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_code = 'supplier_code_example'; // string
$query_type = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\INVCQueryType(); // \OpenAPI\Client\Model\INVCQueryType
$reference_number = 'reference_number_example'; // string
$requested_date = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime
$available_timestamp = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime
$environment = new \OpenAPI\Client\Model\\OpenAPI\Client\Model\Environment(); // \OpenAPI\Client\Model\Environment
$x_forwarded_for = 'x_forwarded_for_example'; // string
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getVoidedInvoices($supplier_code, $query_type, $reference_number, $requested_date, $available_timestamp, $environment, $x_forwarded_for, $x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvoiceApi->getVoidedInvoices: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_code** | **string**|  | |
| **query_type** | [**\OpenAPI\Client\Model\INVCQueryType**](../Model/.md)|  | |
| **reference_number** | **string**|  | [optional] |
| **requested_date** | **\DateTime**|  | [optional] |
| **available_timestamp** | **\DateTime**|  | [optional] |
| **environment** | [**\OpenAPI\Client\Model\Environment**](../Model/.md)|  | [optional] |
| **x_forwarded_for** | **string**|  | [optional] |
| **x_account_id** | **string**|  | [optional] |
| **body** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetVoidedResponse**](../Model/GetVoidedResponse.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader), [OAuth2PasswordBearer](../../README.md#OAuth2PasswordBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
