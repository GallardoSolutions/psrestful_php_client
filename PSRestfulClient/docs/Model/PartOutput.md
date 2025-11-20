# # PartOutput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**part_id** | **string** |  |
**part_description** | **string** |  |
**part_price_array** | [**\OpenAPI\Client\Model\PartPriceArray**](PartPriceArray.md) |  |
**part_group** | **int** | A numeric identifier grouping mutually exclusive parts together. When configuring data, always start with part group “1” |
**next_part_group** | **int** |  | [optional]
**part_group_required** | **bool** | A boolean value specifying if this partGroup is required for the product configuration. If set to TRUE, a selection in the partGroup is required for ordering |
**part_group_description** | **string** |  |
**ratio** | **string** | Describes how the amount of partIds that need to be added to the order based on the number of products ordered |
**default_part** | **bool** |  |
**location_id_array** | [**\OpenAPI\Client\Model\LocationIdArray**](LocationIdArray.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
