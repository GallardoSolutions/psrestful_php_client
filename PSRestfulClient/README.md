# PSRESTful PHP SDK

A modern PHP client for the PSRESTful API - Transform PromoStandards SOAP complexity into simple REST calls.

[![PHP Version](https://img.shields.io/badge/php-%3E%3D8.1-blue.svg)](https://php.net/)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

## Overview

The PSRESTful PHP SDK provides a powerful, easy-to-use interface for integrating PromoStandards data into your PHP applications. Instead of wrestling with SOAP protocols and XML parsing, you can now access promotional product data, inventory, pricing, orders, and more through a clean, RESTful API.

**Why This Matters:** The promotional products industry has long relied on SOAP-based PromoStandards. PSRESTful modernizes this by converting SOAP to REST, and this SDK makes it even easier for PHP developers to build integrations.

For more information, please visit [https://psrestful.com/contact-us/](https://psrestful.com/contact-us/).

## Why Use This SDK?

- **Save Development Time**: Pre-built models and API clients mean you can start integrating in minutes, not weeks
- **Type Safety**: Full PHP 8.1+ type hints help catch errors before runtime
- **Comprehensive Coverage**: Access all PSRESTful API endpoints including Product Data, Inventory, Pricing, Orders, Media Content, and more
- **Well Documented**: Auto-generated documentation for every endpoint, model, and parameter
- **Industry Standard**: Built using OpenAPI/Swagger specifications
- **Active Maintenance**: Regular updates to match API changes
- **Production Ready**: Used by distributors and suppliers across the promotional products industry

## Quick Start

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure your API credentials
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()
    ->setApiKey('X-API-Key', 'YOUR_API_KEY');

// Create an API instance
$productApi = new OpenAPI\Client\Api\ProductDataApi(
    new GuzzleHttp\Client(),
    $config
);

// Fetch product data
try {
    $product = $productApi->getProductV200('SUPPLIER_CODE', 'PRODUCT_ID');
    echo "Product Name: " . $product->getProductName() . "\n";
    echo "Price: $" . $product->getPrice() . "\n";
} catch (Exception $e) {
    echo "Error: " . $e->getMessage() . "\n";
}
```

That's it! You're now pulling real PromoStandards data with just a few lines of code.

## Who Should Use This SDK?

### Distributors
- Build custom e-commerce platforms
- Integrate supplier data into your ERP/CRM
- Create automated inventory sync systems
- Develop mobile apps for sales teams

### Suppliers
- Connect your systems to distributor platforms
- Automate order processing
- Provide real-time inventory updates
- Streamline product data distribution

### Developers & Agencies
- Rapidly build promotional products integrations
- Create custom solutions for clients in the industry
- Prototype new ideas quickly
- Reduce development and maintenance costs

### Technology Vendors
- Add PromoStandards support to your platform
- Offer seamless supplier integrations
- Differentiate your product with modern API access
- Scale your integrations efficiently

## Installation & Usage

### Requirements

PHP 8.1 and later.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure API key authorization: APIKeyHeader
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');

// Configure OAuth2 access token for authorization: OAuth2PasswordBearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_account_id = 'x_account_id_example'; // string
$body = 'body_example'; // string

try {
    $result = $apiInstance->getCurrentAccountInfoMeGet($x_account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->getCurrentAccountInfoMeGet: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *https://api.psrestful.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AccountApi* | [**getCurrentAccountInfoMeGet**](docs/Api/AccountApi.md#getcurrentaccountinfomeget) | **GET** /me | Get Current Account Info
*DefaultApi* | [**getServiceCodes**](docs/Api/DefaultApi.md#getservicecodes) | **GET** /service-codes | Get Service Codes
*DefaultApi* | [**getServices**](docs/Api/DefaultApi.md#getservices) | **GET** /services/{supplier_code} | Get Services
*ExtraApi* | [**getBrandsExtraV1BrandsGet**](docs/Api/ExtraApi.md#getbrandsextrav1brandsget) | **GET** /extra/v1/brands | Get Brands
*ExtraApi* | [**getBrandsV2**](docs/Api/ExtraApi.md#getbrandsv2) | **GET** /extra/v2/brands | Get Brands
*ExtraApi* | [**getCategoriesV2**](docs/Api/ExtraApi.md#getcategoriesv2) | **GET** /extra/v2/categories | Get Categories
*ExtraApi* | [**getClassificationsExtraV1ProductsExtraIdClassificationsGet**](docs/Api/ExtraApi.md#getclassificationsextrav1productsextraidclassificationsget) | **GET** /extra/v1/products/{extra_id}/classifications | Get Classifications
*ExtraApi* | [**getCombinedPpcs**](docs/Api/ExtraApi.md#getcombinedppcs) | **GET** /extra/v2/products/{product_id}/ppcs | Get Combined Ppcs
*ExtraApi* | [**getDecorationsExtraV1SuppliersSupplierCodeDecorationsGet**](docs/Api/ExtraApi.md#getdecorationsextrav1supplierssuppliercodedecorationsget) | **GET** /extra/v1/suppliers/{supplier_code}/decorations | Get Decorations
*ExtraApi* | [**getExtraId**](docs/Api/ExtraApi.md#getextraid) | **GET** /extra/v2/products/get-extra-id/ | Get Extra Id
*ExtraApi* | [**getInventoryV2**](docs/Api/ExtraApi.md#getinventoryv2) | **GET** /extra/v2/inventory/{supplier_code} | Get Inventory
*ExtraApi* | [**getMetafieldsByTitle**](docs/Api/ExtraApi.md#getmetafieldsbytitle) | **GET** /extra/v2/products/get-metafields-by-title/ | Get Metafields By Title
*ExtraApi* | [**getPartIdMappingsV2**](docs/Api/ExtraApi.md#getpartidmappingsv2) | **GET** /extra/v2/part-id-mappings | Get Part Id Mappings
*ExtraApi* | [**getProductExtraV1ProductsProductIdGet**](docs/Api/ExtraApi.md#getproductextrav1productsproductidget) | **GET** /extra/v1/products/{product_id} | Get Product
*ExtraApi* | [**getProductMetafieldsV2**](docs/Api/ExtraApi.md#getproductmetafieldsv2) | **GET** /extra/v2/products/metafields | Get Product Metafields
*ExtraApi* | [**getProductPartsExtraV1ProductsProductIdSortedPartsGet**](docs/Api/ExtraApi.md#getproductpartsextrav1productsproductidsortedpartsget) | **GET** /extra/v1/products/{product_id}/sorted-parts | Get Product Parts
*ExtraApi* | [**getProductV2**](docs/Api/ExtraApi.md#getproductv2) | **GET** /extra/v2/products/{product_id} | Get Product
*ExtraApi* | [**getProducts**](docs/Api/ExtraApi.md#getproducts) | **GET** /extra/v1/products | Get Products
*ExtraApi* | [**getProductsV2**](docs/Api/ExtraApi.md#getproductsv2) | **GET** /extra/v2/products | Get Products
*ExtraApi* | [**getSuppliersExtraV1SuppliersGet**](docs/Api/ExtraApi.md#getsuppliersextrav1suppliersget) | **GET** /extra/v1/suppliers | Get Suppliers
*ExtraApi* | [**getSuppliersV2**](docs/Api/ExtraApi.md#getsuppliersv2) | **GET** /extra/v2/suppliers | Get Suppliers
*ExtraApi* | [**scrapeExtraV1ScrapeSupplierCodeGet**](docs/Api/ExtraApi.md#scrapeextrav1scrapesuppliercodeget) | **GET** /extra/v1/scrape/{supplier_code}/ | Scrape
*InventoryApi* | [**getFilterValues**](docs/Api/InventoryApi.md#getfiltervalues) | **GET** /v{api_version}/suppliers/{supplier_code}/inventory/filter-values/{product_id} | Get Filter Values
*InventoryApi* | [**getInventoryByProductV121**](docs/Api/InventoryApi.md#getinventorybyproductv121) | **GET** /v1.2.1/suppliers/{supplier_code}/inventory/{product_id} | Get Inventory By Product V121
*InventoryApi* | [**getInventoryByProductV200**](docs/Api/InventoryApi.md#getinventorybyproductv200) | **GET** /v2.0.0/suppliers/{supplier_code}/inventory/{product_id} | Get Inventory By Product V200
*InvoiceApi* | [**getInvoices**](docs/Api/InvoiceApi.md#getinvoices) | **GET** /v1.0.0/suppliers/{supplier_code}/invoices | Get Invoices
*InvoiceApi* | [**getVoidedInvoices**](docs/Api/InvoiceApi.md#getvoidedinvoices) | **GET** /v1.0.0/suppliers/{supplier_code}/voided-invoices | Get Voided Invoices
*MediaContentApi* | [**getMediaContentV100**](docs/Api/MediaContentApi.md#getmediacontentv100) | **GET** /v1.0.0/suppliers/{supplier_code}/medias/{product_id} | Get Media Content V100
*MediaContentApi* | [**getMediaContentV110**](docs/Api/MediaContentApi.md#getmediacontentv110) | **GET** /v1.1.0/suppliers/{supplier_code}/medias/{product_id} | Get Media Content V110
*MediaContentApi* | [**getMediaDateModified**](docs/Api/MediaContentApi.md#getmediadatemodified) | **GET** /v1.1.0/suppliers/{supplier_code}/media-modified-since | Get Media Date Modified
*OrderShipmentNotificationApi* | [**getOrderShipmentNotificationV100**](docs/Api/OrderShipmentNotificationApi.md#getordershipmentnotificationv100) | **GET** /v1.0.0/suppliers/{supplier_code}/order-shipment-notifications | Get Order Shipment Notification V100
*OrderShipmentNotificationApi* | [**getOrderShipmentNotificationV200**](docs/Api/OrderShipmentNotificationApi.md#getordershipmentnotificationv200) | **GET** /v2.0.0/suppliers/{supplier_code}/order-shipment-notifications | Get Order Shipment Notification V200
*OrderStatusApi* | [**getIssueV200**](docs/Api/OrderStatusApi.md#getissuev200) | **GET** /v2.0.0/suppliers/{supplier_code}/issues/{issue_id} | Get Issue
*OrderStatusApi* | [**getOrderStatusDetailsV100**](docs/Api/OrderStatusApi.md#getorderstatusdetailsv100) | **GET** /v1.0.0/suppliers/{supplier_code}/order-status-details | Get Order Status Details
*OrderStatusApi* | [**getOrderStatusTypesV100**](docs/Api/OrderStatusApi.md#getorderstatustypesv100) | **GET** /v1.0.0/suppliers/{supplier_code}/order-status-types | Get Order Status Types
*OrderStatusApi* | [**getOrderStatusV200**](docs/Api/OrderStatusApi.md#getorderstatusv200) | **GET** /v2.0.0/suppliers/{supplier_code}/order-status | Get Order Status
*OrderStatusApi* | [**getServiceMethodsV200**](docs/Api/OrderStatusApi.md#getservicemethodsv200) | **GET** /v2.0.0/suppliers/{supplier_code}/service-methods | Get Service Methods
*PSMEDxApi* | [**classifyPsmedxV1ClassifyGet**](docs/Api/PSMEDxApi.md#classifypsmedxv1classifyget) | **GET** /psmedx/v1/classify/ | Classify
*PSMEDxApi* | [**decoratePsmedxV1DecorateGet**](docs/Api/PSMEDxApi.md#decoratepsmedxv1decorateget) | **GET** /psmedx/v1/decorate/ | Decorate
*PSMEDxApi* | [**drawBoundingBoxesPsmedxV1ShowBoundingBoxesGet**](docs/Api/PSMEDxApi.md#drawboundingboxespsmedxv1showboundingboxesget) | **GET** /psmedx/v1/show-bounding-boxes/ | Draw Bounding Boxes
*PSMEDxApi* | [**findAndShowBboxPsmedxV1FindAndShowBoundingBoxGet**](docs/Api/PSMEDxApi.md#findandshowbboxpsmedxv1findandshowboundingboxget) | **GET** /psmedx/v1/find-and-show-bounding-box/ | Find And Show Bbox
*PSMEDxApi* | [**findBboxPsmedxV1FindBoundingBoxGet**](docs/Api/PSMEDxApi.md#findbboxpsmedxv1findboundingboxget) | **GET** /psmedx/v1/find-bounding-box/ | Find Bbox
*PSMEDxApi* | [**getTopColorsPsmedxV1ImageColorsGet**](docs/Api/PSMEDxApi.md#gettopcolorspsmedxv1imagecolorsget) | **GET** /psmedx/v1/image/colors/ | Get Top Colors
*PSMEDxApi* | [**imageInfoPsmedxV1ImageInfoGet**](docs/Api/PSMEDxApi.md#imageinfopsmedxv1imageinfoget) | **GET** /psmedx/v1/image-info/ | Image Info
*PSMEDxApi* | [**nearestPantonePsmedxV1NearestPantoneGet**](docs/Api/PSMEDxApi.md#nearestpantonepsmedxv1nearestpantoneget) | **GET** /psmedx/v1/nearest-pantone/ | Nearest Pantone
*PSMEDxApi* | [**pantoneToHexPsmedxV1PantoneToHexGet**](docs/Api/PSMEDxApi.md#pantonetohexpsmedxv1pantonetohexget) | **GET** /psmedx/v1/pantone-to-hex/ | Pantone To Hex
*PSMEDxApi* | [**removeBgViewPsmedxV1RemoveBackgroundGet**](docs/Api/PSMEDxApi.md#removebgviewpsmedxv1removebackgroundget) | **GET** /psmedx/v1/remove-background/ | Remove Bg View
*PSMEDxApi* | [**vectorizeImagePsmedxV1VectorizeGet**](docs/Api/PSMEDxApi.md#vectorizeimagepsmedxv1vectorizeget) | **GET** /psmedx/v1/vectorize/ | Vectorize Image
*ProductDataApi* | [**getAllSellableProductIds**](docs/Api/ProductDataApi.md#getallsellableproductids) | **GET** /v{api_version}/suppliers/{supplier_code}/sellable-product-ids | Get All Sellable Product Ids
*ProductDataApi* | [**getAllSellables**](docs/Api/ProductDataApi.md#getallsellables) | **GET** /v{api_version}/suppliers/{supplier_code}/sellables | Get All Sellables
*ProductDataApi* | [**getProductCloseoutV100**](docs/Api/ProductDataApi.md#getproductcloseoutv100) | **GET** /v1.0.0/suppliers/{supplier_code}/products-closeout | Get Product Closeout V100
*ProductDataApi* | [**getProductCloseoutV200**](docs/Api/ProductDataApi.md#getproductcloseoutv200) | **GET** /v2.0.0/suppliers/{supplier_code}/products-closeout | Get Product Closeout V200
*ProductDataApi* | [**getProductDateModifiedV100**](docs/Api/ProductDataApi.md#getproductdatemodifiedv100) | **GET** /v1.0.0/suppliers/{supplier_code}/products-modified-since | Get Product Date Modified V100
*ProductDataApi* | [**getProductDateModifiedV200**](docs/Api/ProductDataApi.md#getproductdatemodifiedv200) | **GET** /v2.0.0/suppliers/{supplier_code}/products-modified-since | Get Product Date Modified V200
*ProductDataApi* | [**getProductSellableV100**](docs/Api/ProductDataApi.md#getproductsellablev100) | **GET** /v1.0.0/suppliers/{supplier_code}/sellable-products | Get Sellables V100
*ProductDataApi* | [**getProductSellableV200**](docs/Api/ProductDataApi.md#getproductsellablev200) | **GET** /v2.0.0/suppliers/{supplier_code}/sellable-products | Get Sellables V200
*ProductDataApi* | [**getProductV100**](docs/Api/ProductDataApi.md#getproductv100) | **GET** /v1.0.0/suppliers/{supplier_code}/products/{product_id} | Get Product V100
*ProductDataApi* | [**getProductV200**](docs/Api/ProductDataApi.md#getproductv200) | **GET** /v2.0.0/suppliers/{supplier_code}/products/{product_id} | Get Product V200
*ProductPriceAndConfigurationApi* | [**getAvailableCharges**](docs/Api/ProductPriceAndConfigurationApi.md#getavailablecharges) | **GET** /v1.0.0/suppliers/{supplier_code}/available-charges/{product_id} | Get Available Charges
*ProductPriceAndConfigurationApi* | [**getAvailableLocations**](docs/Api/ProductPriceAndConfigurationApi.md#getavailablelocations) | **GET** /v1.0.0/suppliers/{supplier_code}/available-locations/{product_id} | Get Available Locations
*ProductPriceAndConfigurationApi* | [**getConfigurationAndPricing**](docs/Api/ProductPriceAndConfigurationApi.md#getconfigurationandpricing) | **GET** /v1.0.0/suppliers/{supplier_code}/pricing-and-configuration/{product_id} | Get Configuration And Pricing
*ProductPriceAndConfigurationApi* | [**getDecorationColors**](docs/Api/ProductPriceAndConfigurationApi.md#getdecorationcolors) | **GET** /v1.0.0/suppliers/{supplier_code}/decoration-colors/{product_id} | Get Decoration Colors
*ProductPriceAndConfigurationApi* | [**getFobPoints**](docs/Api/ProductPriceAndConfigurationApi.md#getfobpoints) | **GET** /v1.0.0/suppliers/{supplier_code}/fob-points/{product_id} | Get Fob Points
*PurchaseOrderApi* | [**getSupportedOrderTypes**](docs/Api/PurchaseOrderApi.md#getsupportedordertypes) | **GET** /v1.0.0/suppliers/{supplier_code}/supported-order-types | Get Supported Order Types
*PurchaseOrderApi* | [**sendPo**](docs/Api/PurchaseOrderApi.md#sendpo) | **POST** /v1.0.0/suppliers/{supplier_code}/purchase-orders/ | Send Po

## Models

- [APPOptions](docs/Model/APPOptions.md)
- [AccountInfo](docs/Model/AccountInfo.md)
- [AccountInfoBasic](docs/Model/AccountInfoBasic.md)
- [AccountInfoExtended](docs/Model/AccountInfoExtended.md)
- [Address](docs/Model/Address.md)
- [AllSellablesFastResponse](docs/Model/AllSellablesFastResponse.md)
- [AllServicesResponse](docs/Model/AllServicesResponse.md)
- [ApparelSize](docs/Model/ApparelSize.md)
- [ApparelStyle](docs/Model/ApparelStyle.md)
- [ArrayOfLabelSize](docs/Model/ArrayOfLabelSize.md)
- [ArrayOfPartColor](docs/Model/ArrayOfPartColor.md)
- [ArrayOfPartId](docs/Model/ArrayOfPartId.md)
- [Artwork](docs/Model/Artwork.md)
- [ArtworkFile](docs/Model/ArtworkFile.md)
- [ArtworkFileArray](docs/Model/ArtworkFileArray.md)
- [ArtworkType](docs/Model/ArtworkType.md)
- [AttributeFlex](docs/Model/AttributeFlex.md)
- [AttributeFlexArray](docs/Model/AttributeFlexArray.md)
- [AvailableCharge](docs/Model/AvailableCharge.md)
- [AvailableChargeArray](docs/Model/AvailableChargeArray.md)
- [AvailableChargesResponse](docs/Model/AvailableChargesResponse.md)
- [AvailableLocationArray](docs/Model/AvailableLocationArray.md)
- [AvailableLocationsResponse](docs/Model/AvailableLocationsResponse.md)
- [BlankOrDecoratedProb](docs/Model/BlankOrDecoratedProb.md)
- [BoundingBox](docs/Model/BoundingBox.md)
- [BrandResponse](docs/Model/BrandResponse.md)
- [BrandSchema](docs/Model/BrandSchema.md)
- [BrandsResponseV2](docs/Model/BrandsResponseV2.md)
- [CategoriesResponseV2](docs/Model/CategoriesResponseV2.md)
- [Category](docs/Model/Category.md)
- [CategorySchema](docs/Model/CategorySchema.md)
- [ChargeArrayInput](docs/Model/ChargeArrayInput.md)
- [ChargeArrayOutput](docs/Model/ChargeArrayOutput.md)
- [ChargeInput](docs/Model/ChargeInput.md)
- [ChargeOutput](docs/Model/ChargeOutput.md)
- [ChargePrice](docs/Model/ChargePrice.md)
- [ChargePriceArray](docs/Model/ChargePriceArray.md)
- [ChargeTypeInput](docs/Model/ChargeTypeInput.md)
- [ChargeTypeOutput](docs/Model/ChargeTypeOutput.md)
- [ClassType](docs/Model/ClassType.md)
- [ClassTypeArray](docs/Model/ClassTypeArray.md)
- [ClassificationResult](docs/Model/ClassificationResult.md)
- [ClassifiersResponse](docs/Model/ClassifiersResponse.md)
- [ColorArray](docs/Model/ColorArray.md)
- [ColorSystem](docs/Model/ColorSystem.md)
- [ColorsResponse](docs/Model/ColorsResponse.md)
- [CombinedCharge](docs/Model/CombinedCharge.md)
- [CombinedChargeArray](docs/Model/CombinedChargeArray.md)
- [CombinedChargePrice](docs/Model/CombinedChargePrice.md)
- [CombinedChargePriceArray](docs/Model/CombinedChargePriceArray.md)
- [CombinedDecoration](docs/Model/CombinedDecoration.md)
- [CombinedDecorationArray](docs/Model/CombinedDecorationArray.md)
- [CombinedLocation](docs/Model/CombinedLocation.md)
- [CombinedLocationArray](docs/Model/CombinedLocationArray.md)
- [CombinedPPC](docs/Model/CombinedPPC.md)
- [CombinedPart](docs/Model/CombinedPart.md)
- [CombinedPartArray](docs/Model/CombinedPartArray.md)
- [CombinedPartPrice](docs/Model/CombinedPartPrice.md)
- [CombinedPartPriceArray](docs/Model/CombinedPartPriceArray.md)
- [ConfigurationAndPricingResponse](docs/Model/ConfigurationAndPricingResponse.md)
- [ConfigurationInput](docs/Model/ConfigurationInput.md)
- [ConfigurationOutput](docs/Model/ConfigurationOutput.md)
- [ConfigurationType](docs/Model/ConfigurationType.md)
- [ContactDetailsInput](docs/Model/ContactDetailsInput.md)
- [ContactDetailsOutput](docs/Model/ContactDetailsOutput.md)
- [ContactInput](docs/Model/ContactInput.md)
- [ContactOutput](docs/Model/ContactOutput.md)
- [ContactTypeInput](docs/Model/ContactTypeInput.md)
- [ContactTypeOutput](docs/Model/ContactTypeOutput.md)
- [CountryIso2](docs/Model/CountryIso2.md)
- [Currency](docs/Model/Currency.md)
- [CurrencySupported](docs/Model/CurrencySupported.md)
- [CurrencySupportedArray](docs/Model/CurrencySupportedArray.md)
- [DecorationArrayInput](docs/Model/DecorationArrayInput.md)
- [DecorationColorResponse](docs/Model/DecorationColorResponse.md)
- [DecorationColors](docs/Model/DecorationColors.md)
- [DecorationGeometryType](docs/Model/DecorationGeometryType.md)
- [DecorationInput](docs/Model/DecorationInput.md)
- [DecorationMethod](docs/Model/DecorationMethod.md)
- [DecorationMethodArray](docs/Model/DecorationMethodArray.md)
- [DecorationNameOut](docs/Model/DecorationNameOut.md)
- [DecorationUomType](docs/Model/DecorationUomType.md)
- [DecorationsResponse](docs/Model/DecorationsResponse.md)
- [Diameter](docs/Model/Diameter.md)
- [DigitalProof](docs/Model/DigitalProof.md)
- [DigitalProofAddress](docs/Model/DigitalProofAddress.md)
- [DigitalProofAddressArray](docs/Model/DigitalProofAddressArray.md)
- [DigitalProofType](docs/Model/DigitalProofType.md)
- [DimUOM](docs/Model/DimUOM.md)
- [Dimension](docs/Model/Dimension.md)
- [DimensionUoMInput](docs/Model/DimensionUoMInput.md)
- [DimensionUoMOutput](docs/Model/DimensionUoMOutput.md)
- [Dimensions](docs/Model/Dimensions.md)
- [Environment](docs/Model/Environment.md)
- [ErrorMessage](docs/Model/ErrorMessage.md)
- [Errormessage](docs/Model/Errormessage.md)
- [Extendedprice](docs/Model/Extendedprice.md)
- [ExtraProduct](docs/Model/ExtraProduct.md)
- [ExtraProductV2](docs/Model/ExtraProductV2.md)
- [Filter](docs/Model/Filter.md)
- [FilterValues](docs/Model/FilterValues.md)
- [FilterValuesResponseV200](docs/Model/FilterValuesResponseV200.md)
- [Fob](docs/Model/Fob.md)
- [FobArray](docs/Model/FobArray.md)
- [FobPointsResponse](docs/Model/FobPointsResponse.md)
- [Fontsize](docs/Model/Fontsize.md)
- [FreightDetails](docs/Model/FreightDetails.md)
- [FutureAvailability](docs/Model/FutureAvailability.md)
- [FutureAvailabilityArray](docs/Model/FutureAvailabilityArray.md)
- [GeometryType](docs/Model/GeometryType.md)
- [GetInvoiceResponse](docs/Model/GetInvoiceResponse.md)
- [GetIssueResponseV200](docs/Model/GetIssueResponseV200.md)
- [GetMediaDateModifiedResponse](docs/Model/GetMediaDateModifiedResponse.md)
- [GetOrderShipmentNotificationResponse](docs/Model/GetOrderShipmentNotificationResponse.md)
- [GetOrderStatusResponseV200](docs/Model/GetOrderStatusResponseV200.md)
- [GetProductSellableResponseV100](docs/Model/GetProductSellableResponseV100.md)
- [GetProductSellableResponseV200](docs/Model/GetProductSellableResponseV200.md)
- [GetServiceMethodsResponseV200](docs/Model/GetServiceMethodsResponseV200.md)
- [GetSupportedOrderTypesResponse](docs/Model/GetSupportedOrderTypesResponse.md)
- [GetVoidedResponse](docs/Model/GetVoidedResponse.md)
- [HTTPValidationError](docs/Model/HTTPValidationError.md)
- [Height](docs/Model/Height.md)
- [INVCQueryType](docs/Model/INVCQueryType.md)
- [Id](docs/Model/Id.md)
- [ImageUrl](docs/Model/ImageUrl.md)
- [Inventory](docs/Model/Inventory.md)
- [Inventory1](docs/Model/Inventory1.md)
- [InventoryByLocation](docs/Model/InventoryByLocation.md)
- [InventoryLevelsResponseV121](docs/Model/InventoryLevelsResponseV121.md)
- [InventoryLevelsResponseV200](docs/Model/InventoryLevelsResponseV200.md)
- [InventoryListResponseV2](docs/Model/InventoryListResponseV2.md)
- [InventoryLocation](docs/Model/InventoryLocation.md)
- [InventoryLocationArray](docs/Model/InventoryLocationArray.md)
- [InventorySchema](docs/Model/InventorySchema.md)
- [Invoice](docs/Model/Invoice.md)
- [InvoiceArray](docs/Model/InvoiceArray.md)
- [InvoiceLineItem](docs/Model/InvoiceLineItem.md)
- [Issue](docs/Model/Issue.md)
- [IssueArray](docs/Model/IssueArray.md)
- [IssueStatus](docs/Model/IssueStatus.md)
- [Item](docs/Model/Item.md)
- [ItemArray](docs/Model/ItemArray.md)
- [LayerOrStop](docs/Model/LayerOrStop.md)
- [LayerOrStopArray](docs/Model/LayerOrStopArray.md)
- [Layers](docs/Model/Layers.md)
- [LineItem](docs/Model/LineItem.md)
- [LineItemArray](docs/Model/LineItemArray.md)
- [LineType](docs/Model/LineType.md)
- [Lineitemtotal](docs/Model/Lineitemtotal.md)
- [LocationArrayInput](docs/Model/LocationArrayInput.md)
- [LocationDecoration](docs/Model/LocationDecoration.md)
- [LocationDecorationArray](docs/Model/LocationDecorationArray.md)
- [LocationId](docs/Model/LocationId.md)
- [LocationIdArray](docs/Model/LocationIdArray.md)
- [LocationInput](docs/Model/LocationInput.md)
- [Locationid](docs/Model/Locationid.md)
- [MediaContent](docs/Model/MediaContent.md)
- [MediaContentArray](docs/Model/MediaContentArray.md)
- [MediaContentDetailsResponse](docs/Model/MediaContentDetailsResponse.md)
- [MediaDateModified](docs/Model/MediaDateModified.md)
- [MediaDateModifiedArray](docs/Model/MediaDateModifiedArray.md)
- [MediaType](docs/Model/MediaType.md)
- [OSNQueryType](docs/Model/OSNQueryType.md)
- [OSQueryType](docs/Model/OSQueryType.md)
- [OrderContactArrayInput](docs/Model/OrderContactArrayInput.md)
- [OrderContactArrayOutput](docs/Model/OrderContactArrayOutput.md)
- [OrderShipmentNotification](docs/Model/OrderShipmentNotification.md)
- [OrderShipmentNotificationArray](docs/Model/OrderShipmentNotificationArray.md)
- [OrderStatusDetailsResponse](docs/Model/OrderStatusDetailsResponse.md)
- [OrderStatusTypesResponse](docs/Model/OrderStatusTypesResponse.md)
- [OrderType](docs/Model/OrderType.md)
- [PO](docs/Model/PO.md)
- [Package](docs/Model/Package.md)
- [PackageArray](docs/Model/PackageArray.md)
- [PantoneColor](docs/Model/PantoneColor.md)
- [PartArrayInput](docs/Model/PartArrayInput.md)
- [PartArrayOutput](docs/Model/PartArrayOutput.md)
- [PartIDMappingListResponseV2](docs/Model/PartIDMappingListResponseV2.md)
- [PartIDMappingSchema](docs/Model/PartIDMappingSchema.md)
- [PartInput](docs/Model/PartInput.md)
- [PartInventory](docs/Model/PartInventory.md)
- [PartInventoryArray](docs/Model/PartInventoryArray.md)
- [PartOutput](docs/Model/PartOutput.md)
- [PartPrice](docs/Model/PartPrice.md)
- [PartPriceArray](docs/Model/PartPriceArray.md)
- [PlacementOptions](docs/Model/PlacementOptions.md)
- [PriceType](docs/Model/PriceType.md)
- [PrimaryColor](docs/Model/PrimaryColor.md)
- [Product](docs/Model/Product.md)
- [ProductArray](docs/Model/ProductArray.md)
- [ProductCategory](docs/Model/ProductCategory.md)
- [ProductCategoryArray](docs/Model/ProductCategoryArray.md)
- [ProductCloseOut](docs/Model/ProductCloseOut.md)
- [ProductCloseOutArray](docs/Model/ProductCloseOutArray.md)
- [ProductCloseOutResponseV100](docs/Model/ProductCloseOutResponseV100.md)
- [ProductCloseOutResponseV200](docs/Model/ProductCloseOutResponseV200.md)
- [ProductDateModified](docs/Model/ProductDateModified.md)
- [ProductDateModifiedArray](docs/Model/ProductDateModifiedArray.md)
- [ProductDateModifiedResponseV100](docs/Model/ProductDateModifiedResponseV100.md)
- [ProductDateModifiedResponseV200](docs/Model/ProductDateModifiedResponseV200.md)
- [ProductIDType](docs/Model/ProductIDType.md)
- [ProductIdsResponse](docs/Model/ProductIdsResponse.md)
- [ProductKeyword](docs/Model/ProductKeyword.md)
- [ProductKeywordArray](docs/Model/ProductKeywordArray.md)
- [ProductListResponse](docs/Model/ProductListResponse.md)
- [ProductListResponseV2](docs/Model/ProductListResponseV2.md)
- [ProductMarketingPoint](docs/Model/ProductMarketingPoint.md)
- [ProductMarketingPointArray](docs/Model/ProductMarketingPointArray.md)
- [ProductMetafields](docs/Model/ProductMetafields.md)
- [ProductMetafieldsListResponseV2](docs/Model/ProductMetafieldsListResponseV2.md)
- [ProductMetafieldsV2](docs/Model/ProductMetafieldsV2.md)
- [ProductPackage](docs/Model/ProductPackage.md)
- [ProductPackagingArray](docs/Model/ProductPackagingArray.md)
- [ProductPart](docs/Model/ProductPart.md)
- [ProductPartArray](docs/Model/ProductPartArray.md)
- [ProductPrice](docs/Model/ProductPrice.md)
- [ProductPriceArray](docs/Model/ProductPriceArray.md)
- [ProductPriceGroup](docs/Model/ProductPriceGroup.md)
- [ProductPriceGroupArray](docs/Model/ProductPriceGroupArray.md)
- [ProductResponseV100](docs/Model/ProductResponseV100.md)
- [ProductResponseV200](docs/Model/ProductResponseV200.md)
- [ProductSellable](docs/Model/ProductSellable.md)
- [ProductSellableArray](docs/Model/ProductSellableArray.md)
- [ProductV100](docs/Model/ProductV100.md)
- [ProductV200](docs/Model/ProductV200.md)
- [ProductVariationInventory](docs/Model/ProductVariationInventory.md)
- [ProductVariationInventoryArray](docs/Model/ProductVariationInventoryArray.md)
- [Program](docs/Model/Program.md)
- [PsDomainModelExtraSlimProduct](docs/Model/PsDomainModelExtraSlimProduct.md)
- [PsDomainModelResponsesSlimProduct](docs/Model/PsDomainModelResponsesSlimProduct.md)
- [PsEntrypointsFastApiSerializersColor](docs/Model/PsEntrypointsFastApiSerializersColor.md)
- [PsdomainModelMediaContentDecoration](docs/Model/PsdomainModelMediaContentDecoration.md)
- [PsdomainModelMediaContentDecorationArray](docs/Model/PsdomainModelMediaContentDecorationArray.md)
- [PsdomainModelMediaContentLocation](docs/Model/PsdomainModelMediaContentLocation.md)
- [PsdomainModelMediaContentLocationArray](docs/Model/PsdomainModelMediaContentLocationArray.md)
- [PsdomainModelOrderStatusV100OrderStatus](docs/Model/PsdomainModelOrderStatusV100OrderStatus.md)
- [PsdomainModelOrderStatusV100OrderStatusArray](docs/Model/PsdomainModelOrderStatusV100OrderStatusArray.md)
- [PsdomainModelOrderStatusV100OrderStatusDetail](docs/Model/PsdomainModelOrderStatusV100OrderStatusDetail.md)
- [PsdomainModelOrderStatusV100OrderStatusDetailArray](docs/Model/PsdomainModelOrderStatusV100OrderStatusDetailArray.md)
- [PsdomainModelOrderStatusV200OrderStatus](docs/Model/PsdomainModelOrderStatusV200OrderStatus.md)
- [PsdomainModelOrderStatusV200OrderStatusArray](docs/Model/PsdomainModelOrderStatusV200OrderStatusArray.md)
- [PsdomainModelOrderStatusV200OrderStatusDetail](docs/Model/PsdomainModelOrderStatusV200OrderStatusDetail.md)
- [PsdomainModelOrderStatusV200OrderStatusDetailArray](docs/Model/PsdomainModelOrderStatusV200OrderStatusDetailArray.md)
- [PsdomainModelPpcDecoration](docs/Model/PsdomainModelPpcDecoration.md)
- [PsdomainModelPpcDecorationArray](docs/Model/PsdomainModelPpcDecorationArray.md)
- [PsdomainModelPpcFobPoint](docs/Model/PsdomainModelPpcFobPoint.md)
- [PsdomainModelPpcFobPointArray](docs/Model/PsdomainModelPpcFobPointArray.md)
- [PsdomainModelPpcLocation](docs/Model/PsdomainModelPpcLocation.md)
- [PsdomainModelPpcLocationArray](docs/Model/PsdomainModelPpcLocationArray.md)
- [PsdomainModelProductDataCommonColor](docs/Model/PsdomainModelProductDataCommonColor.md)
- [PsdomainModelProductDataCommonFobPoint](docs/Model/PsdomainModelProductDataCommonFobPoint.md)
- [PsdomainModelProductDataCommonFobPointArray](docs/Model/PsdomainModelProductDataCommonFobPointArray.md)
- [PsdomainModelProductDataCommonLocation](docs/Model/PsdomainModelProductDataCommonLocation.md)
- [QuantityAvailable](docs/Model/QuantityAvailable.md)
- [QuantityInput](docs/Model/QuantityInput.md)
- [QuantityOutput](docs/Model/QuantityOutput.md)
- [QuantityUoM](docs/Model/QuantityUoM.md)
- [ReferenceNuberType](docs/Model/ReferenceNuberType.md)
- [RelatedProduct](docs/Model/RelatedProduct.md)
- [RelatedProductArray](docs/Model/RelatedProductArray.md)
- [RelationTye](docs/Model/RelationTye.md)
- [RespondTo](docs/Model/RespondTo.md)
- [ResponseGetCurrentAccountInfoMeGet](docs/Model/ResponseGetCurrentAccountInfoMeGet.md)
- [ResponseToArray](docs/Model/ResponseToArray.md)
- [SalesOrder](docs/Model/SalesOrder.md)
- [SalesOrderArray](docs/Model/SalesOrderArray.md)
- [SalesOrderNumber](docs/Model/SalesOrderNumber.md)
- [SalesOrderNumbersArray](docs/Model/SalesOrderNumbersArray.md)
- [ScraperResponse](docs/Model/ScraperResponse.md)
- [ScraperSupplierCodes](docs/Model/ScraperSupplierCodes.md)
- [SendPOResponse](docs/Model/SendPOResponse.md)
- [ServiceEntry](docs/Model/ServiceEntry.md)
- [ServiceMessage](docs/Model/ServiceMessage.md)
- [ServiceMessageArray](docs/Model/ServiceMessageArray.md)
- [ServiceMethod](docs/Model/ServiceMethod.md)
- [ServiceMethodArray](docs/Model/ServiceMethodArray.md)
- [ServiceVersionModel](docs/Model/ServiceVersionModel.md)
- [Severity](docs/Model/Severity.md)
- [ShipTo](docs/Model/ShipTo.md)
- [Shipment](docs/Model/Shipment.md)
- [ShipmentArray](docs/Model/ShipmentArray.md)
- [ShipmentDestinationType](docs/Model/ShipmentDestinationType.md)
- [ShipmentLink](docs/Model/ShipmentLink.md)
- [ShipmentLinkArray](docs/Model/ShipmentLinkArray.md)
- [ShipmentLocation](docs/Model/ShipmentLocation.md)
- [ShipmentLocationArray](docs/Model/ShipmentLocationArray.md)
- [ShippingPackage](docs/Model/ShippingPackage.md)
- [ShippingPackageArray](docs/Model/ShippingPackageArray.md)
- [SimpleColor](docs/Model/SimpleColor.md)
- [SinglePartOrGroupProb](docs/Model/SinglePartOrGroupProb.md)
- [SlimProductV2](docs/Model/SlimProductV2.md)
- [Specification](docs/Model/Specification.md)
- [SpecificationArray](docs/Model/SpecificationArray.md)
- [SpecificationType](docs/Model/SpecificationType.md)
- [Status](docs/Model/Status.md)
- [StatusArray](docs/Model/StatusArray.md)
- [SupplierSchema](docs/Model/SupplierSchema.md)
- [SuppliersResponse](docs/Model/SuppliersResponse.md)
- [SuppliersResponseV2](docs/Model/SuppliersResponseV2.md)
- [SupportedOrderType](docs/Model/SupportedOrderType.md)
- [Tax](docs/Model/Tax.md)
- [TaxInformationArray](docs/Model/TaxInformationArray.md)
- [TaxTypeInput](docs/Model/TaxTypeInput.md)
- [TaxTypeOutput](docs/Model/TaxTypeOutput.md)
- [Taxamount](docs/Model/Taxamount.md)
- [TexInformation](docs/Model/TexInformation.md)
- [ThirdPartyAccount](docs/Model/ThirdPartyAccount.md)
- [ToleranceDetails](docs/Model/ToleranceDetails.md)
- [ToleranceType](docs/Model/ToleranceType.md)
- [ToleranceUoM](docs/Model/ToleranceUoM.md)
- [Totalamount](docs/Model/Totalamount.md)
- [TransportMechanism](docs/Model/TransportMechanism.md)
- [Typeset](docs/Model/Typeset.md)
- [UOM](docs/Model/UOM.md)
- [Unitprice](docs/Model/Unitprice.md)
- [ValidationError](docs/Model/ValidationError.md)
- [ValidationErrorLocInner](docs/Model/ValidationErrorLocInner.md)
- [Value](docs/Model/Value.md)
- [Variant](docs/Model/Variant.md)
- [VariantResponse](docs/Model/VariantResponse.md)
- [VoidedInvoice](docs/Model/VoidedInvoice.md)
- [VoidedInvoiceArray](docs/Model/VoidedInvoiceArray.md)
- [WeightUOM](docs/Model/WeightUOM.md)
- [WeightUoM](docs/Model/WeightUoM.md)
- [Width](docs/Model/Width.md)

## Authorization

Authentication schemes defined for the API:
### OAuth2PasswordBearer

- **Type**: `OAuth`
- **Flow**: `password`
- **Authorization URL**: ``
- **Scopes**: N/A

### APIKeyHeader

- **Type**: API key
- **API key parameter name**: X-API-Key
- **Location**: HTTP header


## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Contributing

We welcome contributions from the community! Whether you're a distributor, supplier, developer, or just passionate about improving the promotional products industry, your input is valuable.

### How You Can Help

- **Report Issues**: Found a bug? Have a feature request? [Open an issue](../../issues)
- **Improve Documentation**: Help us make the docs clearer with examples, tutorials, or corrections
- **Submit Pull Requests**: Fix bugs, add features, or optimize code
- **Share Your Use Cases**: Let us know how you're using the SDK - it helps us improve
- **Spread the Word**: Star the repository and tell others in the industry

### Development Setup

1. Fork the repository
2. Clone your fork: `git clone https://github.com/YOUR_USERNAME/REPO_NAME.git`
3. Install dependencies: `composer install`
4. Make your changes
5. Run tests: `vendor/bin/phpunit`
6. Submit a pull request

### Coding Standards

- Follow PSR-12 coding standards
- Add tests for new features
- Update documentation as needed
- Keep commits focused and write clear commit messages

### Feature Requests

Have an idea for a new feature? We'd love to hear it! Please open an issue describing:
- The problem you're trying to solve
- Your proposed solution
- Any alternative approaches you've considered
- How it would benefit other users

## Community & Support

### Get Help

- **Documentation**: Check the `/docs` folder for detailed API documentation
- **Email Support**: devs@psrestful.com
- **Website**: [https://psrestful.com/contact-us/](https://psrestful.com/contact-us/)
- **Issues**: [GitHub Issues](../../issues) for bug reports and feature requests

### For Companies

**Using this SDK in production?** We'd love to feature your success story! Contact us at devs@psrestful.com

**Enterprise Support Available**: Need dedicated support, custom features, or SLA guarantees? Reach out to discuss enterprise options.

### Stay Updated

- Watch this repository for updates
- Check the [API changelog](https://api.psrestful.com/docs) for breaking changes
- Subscribe to PSRESTful announcements

## Roadmap

We're continuously improving this SDK. Upcoming priorities include:

- Enhanced error handling and retry logic
- Webhook support for real-time updates
- Additional code examples and tutorials
- Performance optimizations
- Expanded test coverage

Your feedback helps shape our roadmap!

## Author

devs@psrestful.com

## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `0.0.1`
- Generator version: `7.17.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`

## License

This SDK is available under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Acknowledgments

- Built on the [OpenAPI Generator](https://openapi-generator.tech) project
- Powered by [PSRESTful API](https://psrestful.com)
- Serving the promotional products industry
- Special thanks to all contributors and early adopters

---

**Ready to modernize your PromoStandards integration?** [Get your API key](https://psrestful.com/contact-us/) and start building today!

**Questions or feedback?** We're here to help: devs@psrestful.com
