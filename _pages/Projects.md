---
layout: single
title: "Projects"
permalink: /projects/
author_profile: true
---

## 🧠 Highlighted Projects

### 🔍 Web Scraping Bot – Python + BeautifulSoup

**Repository:** [GitHub - Web Scraping Tool](https://github.com/Wabirus/web-scraper-bot)

**Overview:**

A Python-based script that scrapes article titles and URLs from a news website. Designed for simplicity, this tool demonstrates web automation fundamentals and HTML parsing using `requests` and `BeautifulSoup`.

**Key Features:**
- Extracts headline text and links from any given news site.
- Outputs clean data into CSV or JSON formats.
- Supports basic error handling and user-agent rotation.

**Tech Stack:**
- Python 3
- Requests
- BeautifulSoup 4
- CSV / JSON

**Sample Code:**

```python
import requests
from bs4 import BeautifulSoup

url = "https://example.com/news"
headers = {"User-Agent": "Mozilla/5.0"}

response = requests.get(url, headers=headers)
soup = BeautifulSoup(response.content, "html.parser")

for article in soup.select("h2.headline a"):
    title = article.get_text(strip=True)
    link = article["href"]
    print(f"{title} - {link}")

