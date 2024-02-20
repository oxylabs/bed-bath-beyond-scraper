# Bed-Bath-Beyond Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Bed-Bath-Beyond Scraper](https://oxylabs.io/products/scraper-api/ecommerce/bed-bath-beyond?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Bed-Bath-Beyond website effortlessly. This brief guide showcases how Bed-Bath-Beyond Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Bed-Bath-Beyond results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Bed-Bath-Beyond page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.bedbathandbeyond.com/c/furniture/living-room-furniture?t=24359'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/bed-bath-beyond-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en\"><head><meta charSet=\"utf-8\"/><meta http-equiv=\"X-UA-Compatible\" conte ... </html>",
      "created_at": "2024-02-20 12:49:39",
      "updated_at": "2024-02-20 12:49:43",
      "page": 1,
      "url": "https://www.bedbathandbeyond.com/c/furniture/living-room-furniture?t=24359",
      "job_id": "7165688959106814977",
      "status_code": 200
    }
  ]
}
```
With our Bed-Bath-Beyond Scraper, you can efficiently pull public data from your desired Bed-Bath-Beyond web page. Gather essential product details, like the UPC, SKU, or availability status, to maintain up-to-date inventory and stay a step ahead of your competitors. If you require assistance, don't hesitate to reach out to our support team through live chat or shoot us an email at hello@oxylabs.io.