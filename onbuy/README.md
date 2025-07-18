# OnBuy API Documentation

The OnBuy API allows external applications to securely communicate with the OnBuy platform. It is based on the [REST architecture](https://en.wikipedia.org/wiki/Representational_state_transfer).

With it, you can automate many tasks such as creating products, creating & updating listings and exporting orders.

## Getting Started

The quickest way to get started with the OnBuy API is to use the endpoints documented in this collection. The API uses standard HTTP methods and JSON for data exchange.

**Key Features:**
- RESTful API design
- JSON request/response format
- OAuth-style authentication
- Comprehensive product and order management
- Real-time order processing
- Automated listing management

## Table of Contents

- [Authentication](authentication.md) - API authentication and access tokens
- [Brands](brands.md) - Brand management endpoints
- [Carriers](carriers.md) - Shipping carrier information
- [Categories](categories.md) - Product categories and classification
- [Commission Tiers](commission-tiers.md) - Commission tier management
- [Conditions](conditions.md) - Product condition management
- [Dispatches](dispatches.md) - Order dispatch and tracking
- [Orders](orders.md) - Order management and processing
- [Product Listings](product-listings.md) - Product listing management
- [Products](products.md) - Product creation and management
- [Queues](queues.md) - Queue status and processing
- [Sellers](sellers.md) - Seller account management
- [Sellers Deliveries](sellers-deliveries.md) - Delivery template management
- [Sellers Entities](sellers-entities.md) - Trading entity management
- [Sites](sites.md) - OnBuy regional site information

## API Change Log

| Date | Description |
|------|-------------|
| July 10th, 2024 | **Changes to Order Functionality:**<br>- Modified Timestamp: Previously, retrieving the order updated the modified timestamp. Now, it updates only when the order is modified.<br>- Previously Exported Flag: Fixed an issue where the first integration to pull the order set the exported flag. Now, this flag is unique to each integration. |
| May 3rd, 2024 | - Example requests added for all endpoints<br>- New section to include details for creating test products<br>- Removed documentation for GET Categories Variants: Browse<br>- Removed documentation for GET Orders: Tracking-providers |
| May 7th, 2021 | Fixed some errors in the documentation |
| August 1st, 2019 | Added 'Delete Listing By SKU' Method |
| March 20th, 2019 | - Added Products: Update<br>- Added Products: Update Batch<br>- Added new options for listings: `return_time`, `free_returns` and `warranty` |
| October 24th, 2018 | Added new endpoint: orders/tracking-providers. This will give an up to date list of tracking providers in place of the list previously provided in this document |
| October 4th, 2018 | Added quantity_dispatched per item to view/browse orders |
| July 30th, 2018 | Fixed bug that affected any rrp over £999 |
| July 20th, 2018 | - Added group_sku to product listings<br>- Added sales fee to Orders: browse/view<br>- Added refund data to Orders: browse/view<br>- Added Orders:Refund<br>- Added Orders:Cancel<br>- Updated Orders:Dispatch<br>- Updated Sellers:Deliveries |
| June 26th, 2018 | Added 'Collect+' to dispatch tracking options |
| June 6th, 2018 | Add buyer's IP address when displaying orders |
| May 17th, 2018 | Added Filter[can_list_in] for Categories:browse |
| April 19th, 2018 | Added 'RRD' to dispatch tracking options |
| March 16th, 2018 | Added product URL to browse queues and view queue |
| February 9th, 2018 | Return condition notes and handling_time when browsing listings |
| January 30th, 2018 | Added more courier services to dispatch tracking options |
| January 18th, 2018 | Added 'handling_time' option for listings. Expects number of days. Applicable to Listings: Create[/batch] and Products: Create[/batch] |
| January 17th, 2018 | - Add groups to product_data in create product<br>- Added 'GLS' to dispatch tracking options<br>- Added URL to product search result<br>- Added filter[status] for Queues: Browse<br>- Replaced 'live' flag with 'publish' in product: create<br>- Added product batch create<br>- Added listings batch create |
| November 28th, 2017 | Order dispatch method updated to support partially dispatching orders |

## Quick Start

1. **Get API Credentials**: Obtain your consumer key and secret key from the OnBuy Seller Control Panel
2. **Request Access Token**: Use the authentication endpoint to get your access token
3. **Make API Calls**: Include the access token in the Authorization header for all requests

## Base URL

- **Live API**: `https://api.onbuy.com/v2`
- **Test API**: Use test credentials for development

## Common Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{access_token}}` | Your API access token | Include in Authorization header |
| `{{site_id}}` | OnBuy regional site ID | 2000 for UK |
| `{{seller_id}}` | Your unique seller ID | Found in Seller Control Panel |
| `{{entity_id}}` | Your trading entity ID | Found in Seller Control Panel |

## Usage Limits

Each request type (POST, GET, PUT, DELETE) has daily and hourly usage limits. Monitor your usage in the Seller Control Panel.

## Support

For API support, please create a ticket through the OnBuy Seller Control Panel.
