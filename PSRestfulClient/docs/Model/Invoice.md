# # Invoice

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**invoice_number** | **string** |  |
**invoice_type** | **string** |  |
**invoice_date** | **\DateTime** |  |
**purchase_order_number** | **string** |  |
**purchase_order_version** | **string** |  |
**bill_to** | [**\OpenAPI\Client\Model\AccountInfo**](AccountInfo.md) |  |
**sold_to** | [**\OpenAPI\Client\Model\AccountInfo**](AccountInfo.md) |  |
**invoice_comments** | **string** |  |
**payment_terms** | **string** |  |
**payment_due_date** | **\DateTime** |  |
**currency** | **string** |  |
**fob_id** | **string** |  |
**sales_amount** | **float** |  |
**shipping_amount** | **float** |  |
**handling_amount** | **float** |  |
**tax_amount** | **float** |  |
**invoice_amount** | **float** |  |
**advance_payment_amount** | **float** |  |
**invoice_amount_due** | **float** |  |
**invoice_document_url** | **string** |  |
**invoice_line_items_array** | [**\OpenAPI\Client\Model\InvoiceLineItem[]**](InvoiceLineItem.md) |  |
**sales_order_numbers_array** | [**\OpenAPI\Client\Model\SalesOrderNumbersArray**](SalesOrderNumbersArray.md) |  |
**tax_array** | [**\OpenAPI\Client\Model\Tax[]**](Tax.md) |  |
**invoice_payment_url** | **string** |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
