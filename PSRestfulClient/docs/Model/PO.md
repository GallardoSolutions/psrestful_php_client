# # PO

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**environment** | [**\OpenAPI\Client\Model\Environment**](Environment.md) |  | [optional]
**order_type** | [**\OpenAPI\Client\Model\OrderType**](OrderType.md) |  |
**order_number** | **string** |  |
**order_date** | **\DateTime** |  |
**last_modified** | **\DateTime** |  |
**total_amount** | [**\OpenAPI\Client\Model\Totalamount**](Totalamount.md) |  |
**payment_terms** | **string** | ie. NET15, NET30, etc. |
**rush** | **bool** | Used to indicate a rush on the purchase order | [optional] [default to false]
**currency** | [**\OpenAPI\Client\Model\Currency**](Currency.md) | The currency the purchase order is transacted in ISO4217 format. ie. USD, CAD, EUR, JPY, GBP, etc. |
**digital_proof** | [**\OpenAPI\Client\Model\DigitalProof**](DigitalProof.md) |  |
**order_contact_array** | [**\OpenAPI\Client\Model\OrderContactArrayInput**](OrderContactArrayInput.md) |  |
**shipment_array** | [**\OpenAPI\Client\Model\ShipmentArray**](ShipmentArray.md) |  |
**line_item_array** | [**\OpenAPI\Client\Model\LineItemArray**](LineItemArray.md) |  |
**terms_and_conditions** | **string** | The terms and conditions of the purchase order |
**sales_channel** | **string** |  |
**promo_code** | **string** |  | [optional]
**tax_information_array** | [**\OpenAPI\Client\Model\TaxInformationArray**](TaxInformationArray.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
