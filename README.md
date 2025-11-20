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

## Installation

### Requirements

- PHP 8.1 or later
- Composer

### Install via Composer

Add this repository to your `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/YOUR_ORG/psrestful_php_client.git"
    }
  ],
  "require": {
    "YOUR_ORG/psrestful_php_client": "*@dev"
  }
}
```

Then run:

```bash
composer install
```

### Manual Installation

1. Download or clone this repository
2. Include the autoloader in your project:

```php
<?php
require_once('/path/to/psrestful_php_client/PSRestfulClient/vendor/autoload.php');
```

## Usage

### Authentication

PSRESTful API supports two authentication methods:

#### API Key (Recommended for server-to-server)

```php
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()
    ->setApiKey('X-API-Key', 'YOUR_API_KEY');
```

#### OAuth2 Password Bearer

```php
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');
```

### Common Examples

#### Get Product Information

```php
$productApi = new OpenAPI\Client\Api\ProductDataApi(
    new GuzzleHttp\Client(),
    $config
);

$product = $productApi->getProductV200('SUPPLIER_CODE', 'PRODUCT_ID');
```

#### Check Inventory Levels

```php
$inventoryApi = new OpenAPI\Client\Api\InventoryApi(
    new GuzzleHttp\Client(),
    $config
);

$inventory = $inventoryApi->getInventoryByProductV200('SUPPLIER_CODE', 'PRODUCT_ID');
```

#### Get Pricing and Configuration

```php
$ppcApi = new OpenAPI\Client\Api\ProductPriceAndConfigurationApi(
    new GuzzleHttp\Client(),
    $config
);

$pricing = $ppcApi->getConfigurationAndPricing('SUPPLIER_CODE', 'PRODUCT_ID');
```

#### Submit Purchase Order

```php
$poApi = new OpenAPI\Client\Api\PurchaseOrderApi(
    new GuzzleHttp\Client(),
    $config
);

$po = new OpenAPI\Client\Model\PO([
    // ... PO details
]);

$response = $poApi->sendPo('SUPPLIER_CODE', $po);
```

## Documentation

📚 **Detailed API Documentation**: See [PSRestfulClient/README.md](PSRestfulClient/README.md) for:
- Complete list of all API endpoints
- Request/response models
- Method signatures
- Authentication details
- Error handling

The detailed documentation is auto-generated from the OpenAPI specification and provides comprehensive information about every available endpoint and model.

## Testing

To run the test suite:

```bash
cd PSRestfulClient
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
2. Clone your fork: `git clone https://github.com/YOUR_USERNAME/psrestful_php_client.git`
3. Install dependencies: `cd PSRestfulClient && composer install`
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

### Regenerating the Client

If you need to regenerate the client code from the latest OpenAPI specification:

```bash
openapi-generator-cli generate \
  -i https://api.psrestful.com/openapi.json \
  -g php \
  -o PSRestfulClient
```

**Note**: The `PSRestfulClient/` directory contains auto-generated code. Manual changes to files in that directory will be overwritten when regenerating.

## Community & Support

### Get Help

- **API Documentation**: [https://docs.psrestful.com](https://docs.psrestful.com)
- **API Reference**: [https://api.psrestful.com/docs](https://api.psrestful.com/docs)
- **PromoStandards Specification**: [https://docs.psrestful.com/standards](https://docs.psrestful.com/standards)
- **Original PromoStandards Specification**: [https://www.promostandards.org](https://www.promostandards.org)
- **GitHub Issues**: [Report bugs or request features](../../issues)
- **Discussions**: Ask questions and share your experiences with the community
- **Email Support**: devs@psrestful.com
- **Website**: [https://psrestful.com/contact-us/](https://psrestful.com/contact-us/)

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
- Batch operation support
- Caching strategies for common queries

Your feedback helps shape our roadmap!

## Project Structure

```
psrestful_php_client/
├── README.md                    # This file - main documentation
├── PSRestfulClient/             # Auto-generated SDK code
│   ├── README.md               # API reference documentation
│   ├── composer.json           # Package dependencies
│   ├── lib/                    # Source code
│   │   ├── Api/               # API endpoint classes
│   │   ├── Model/             # Data models
│   │   └── Configuration.php  # SDK configuration
│   ├── docs/                   # Detailed documentation
│   └── test/                   # Unit tests
└── openapitools.json           # Generator configuration
```

## Troubleshooting

### Common Issues

**"Class not found" errors**
- Ensure you've run `composer install` in the PSRestfulClient directory
- Check that your autoloader path is correct

**Authentication failures**
- Verify your API key is correct
- Ensure you're using the right authentication method (API Key vs OAuth2)
- Check that your API key has the necessary permissions

**Rate limiting**
- PSRESTful API has rate limits. Implement exponential backoff for retries
- Consider caching responses for frequently accessed data

**SSL/TLS errors**
- Ensure your PHP installation has up-to-date CA certificates
- Check that cURL is properly configured

For more help, see our [troubleshooting guide](https://psrestful.com/docs/troubleshooting) or contact support.

## Version History

- **v0.0.1** - Initial release
  - Support for all PromoStandards services
  - PHP 8.1+ compatibility
  - OAuth2 and API Key authentication

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

---

*Made with ❤️ for the promotional products industry*
