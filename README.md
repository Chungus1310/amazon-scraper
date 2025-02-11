# Amazon Product Scraper 🛍️

A friendly Python script that helps you fetch product information from Amazon search results! This scraper gets the top 20 non-sponsored products for any search query and saves them in a neat JSON file.

## Features ✨

- Scrapes top 20 non-sponsored products from Amazon search results
- Extracts detailed product information:
  - Product title
  - Price
  - Rating
  - Number of reviews
  - Product image URL
  - Product page URL
- Uses random delays and rotating user agents to be gentle with Amazon's servers
- Handles various error scenarios gracefully
- Saves results in a clean JSON format

## Requirements 📋

```
beautifulsoup4
requests
fake-useragent
```

## Installation 🚀

1. Clone this repository:
```bash
git clone https://github.com/Chungus1310/amazon-scraper.git
cd amazon-scraper
```

2. Install the required packages:
```bash
pip install beautifulsoup4 requests fake-useragent
```

## Usage 💻

1. Import the scraper in your Python script:
```python
from amazon_scraper import scrape_amazon_products
```

2. Call the function with your search query:
```python
products = scrape_amazon_products("sea pink gel nail polish")
```

Or run the script directly:
```bash
python amazon_scraper.py
```

The results will be saved in `amazon_products.json` in the following format:
```json
[
  {
    "title": "Product Name",
    "price": "$XX.XX",
    "rating": "4.5",
    "reviews_count": "1234",
    "image_url": "https://...",
    "product_url": "https://..."
  },
  ...
]
```

## Error Handling 🛠️

The scraper includes robust error handling for common scenarios:
- CAPTCHA detection
- Rate limiting (503 errors)
- Network issues
- Invalid product data

When encountering issues, the script provides helpful suggestions for resolving them.

## Important Notes ⚠️

1. Be mindful of Amazon's terms of service and rate limits
2. Use reasonable delays between requests (the script includes random delays)
3. Consider using a VPN or proxy if you encounter frequent blocks
4. The script filters out sponsored products to ensure organic search results

## Troubleshooting 🔍

If you encounter blocks or CAPTCHAs:
1. Try increasing the delay between requests
2. Use a VPN or proxy service
3. Ensure your headers are up to date
4. Clear your browser cookies and try accessing Amazon normally first

## Contributing 🤝

Feel free to open issues or submit pull requests! We appreciate any contributions to improve the scraper.

## Author 👨‍💻

Created by [Chun](https://github.com/Chungus1310)

## License 📝

This project is licensed under the Apache 2.0 License - see the LICENSE file for details.

## Disclaimer ⚖️

This scraper is for educational purposes only. Make sure to comply with Amazon's terms of service and robots.txt when using this tool.
