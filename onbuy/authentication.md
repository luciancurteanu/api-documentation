# Authentication

The OnBuy API uses token-based authentication. You need to obtain an access token before making any API calls.

## Overview

- **Access tokens** are valid for 15 minutes
- **Tokens are IP-restricted** - can only be used from the same IP address where they were generated
- **All API endpoints** (except token request) require authentication
- **Include token** in the `Authorization` header for all authenticated requests

## API Settings

Access your API credentials from the [API settings page](https://seller.onbuy.com/inventory/integrations/onbuy-api/) in your Seller Control Panel. This page provides:

- Consumer Key and Secret Key (Live and Test)
- API URL endpoints
- Daily usage statistics
- Integration settings

## Connection Details

There are two sets of keys available:

- **Test Keys**: Use for development and testing (separate data environment)
- **Live Keys**: Use for production (real data)

## Auth: request token

Request an access token using your API credentials.

**Method:** `POST`

**URL:** `{{host}}/auth/request-token`

**Headers:**
```
Content-Type: application/x-www-form-urlencoded
```

**Parameters:**

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| secret_key | string | Yes | Your secret key from the API settings |
| consumer_key | string | Yes | Your consumer key from the API settings |

**Example Request:**
```bash
curl -X POST "https://api.onbuy.com/v2/auth/request-token" \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -d "secret_key=YOUR_SECRET_KEY&consumer_key=YOUR_CONSUMER_KEY"
```

**Example Response:**
```json
{
    "access_token": "4E7DREERR2189-A943-4697-C295-fCA434558518",
    "expires_at": 1514764800
}
```

## Using the Access Token

Include the access token in the `Authorization` header for all subsequent API requests:

```bash
curl -X GET "https://api.onbuy.com/v2/products" \
  -H "Authorization: YOUR_ACCESS_TOKEN"
```

## Error Responses

| Status Code | Description |
|-------------|-------------|
| 401 | Unauthorized - Missing or invalid credentials |
| 403 | Forbidden - Account doesn't have permission |
| 429 | Too Many Requests - Rate limit exceeded |

---

