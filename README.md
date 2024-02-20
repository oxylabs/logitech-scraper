# Logitech Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Logitech Scraper](https://oxylabs.io/products/scraper-api/ecommerce/logitech?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Logitech website effortlessly. This brief guide showcases how Logitech Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Logitech results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Logitech page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.logitech.com/en-us/products/headsets.html'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/logitech-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "\n<!DOCTYPE HTML>\n<html lang=\"en-US\" data-i18n-dictionary-src=\"https://www.logitech.com/en-us.i18n.js ... </html>",
      "created_at": "2024-02-20 12:54:58",
      "updated_at": "2024-02-20 12:54:59",
      "page": 1,
      "url": "https://www.logitech.com/en-us/products/headsets.html",
      "job_id": "7165690295286259713",
      "status_code": 200
    }
  ]
}
```
With our Logitech Scraper, you can effortlessly extract public data from any Logitech web page. Gather essential product details like specifications, warranty periods, or user manuals to understand the market space better and outperform your rivals. If you're uncertain or have inquiries, feel free to connect with our support team through live chat or email us at hello@oxylabs.io.