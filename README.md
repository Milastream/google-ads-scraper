[Google Ads Scraper](https://apify.com/madeingermany/google-ads-scraper?fpr=data)

# Google Ads Scraper (2X Faster, More Data)

**Google Ads Scraper** is designed to quickly and efficiently extract detailed data from Google's Ads Transparency Center. Instead of using a slow, resource-heavy browser automation tool, this scraper directly mimics the internal Google API behavior.

It is capable of fetching ads 2× faster than standard scrapers while returning exclusive inner metrics that aren't natively exposed on the page.

![Banner](https://images.apifyusercontent.com/mAstcpRvvNT-zbRxPl1I02Z7pTUI6dGHRlHxJ1yJFZE/w:1800/cb:1/aHR0cHM6Ly91cGxvYWQud2lraW1lZGlhLm9yZy93aWtpcGVkaWEvY29tbW9ucy90aHVtYi9jL2M3L0dvb2dsZV9BZHNfbG9nby5zdmcvMTAyNHB4LUdvb2dsZV9BZHNfbG9nby5zdmcucG5n.webp)

## 🔄 Comparison vs Competitors

| Feature | Competitor | This Scraper |
| --- | --- | --- |
| Avg Speed (100 ads) | ~81s | **39s** 🚀 |
| Ad formats | Text, Image, Video | Text, Image, Video |
| Media download | ✅ | ✅ |
| `url` (full ad link) | ❌ | ✅ |
| `firstShownAt` | ❌ | ✅ |
| `audienceSelections` | ❌ | ✅ |
| Age-restricted ads | ❌ | ✅ *(via cookies)* |
| Reliability | Occasional gaps | **Error-free API runs** ✅ |

## ✨ Features

- ⚡ **2× faster API bypassing:** We scrape the data exactly like the native App does, cutting overhead by up to 90%.
- **Scrapes all ad formats:** Extract TEXT, IMAGE, and VIDEO seamlessly.
- **Country Stats & Demographics:** Fetches total arrays of impression bounds and demographics (perfect for permitted political ads).
- **Cross-Platform Mapping:** Tracks specific impression ranges mapped accurately across YouTube, App Networks, Shopping, and Google Search.
- **Detailed Cookie Integration:** Instantly unlock gambling, alcohol, or age-restricted content by safely injecting a JSON cookie sequence.
- **Media Sync:** Optionally download the target advertiser's assets directly to Apify's Key-Value Store logic!

## 📥 Getting Started & Input

You will need at least one Google Transparency Center Search URL to get started. Navigate to [Google Ads Transparency Center](https://adstransparency.google.com/), construct your filter (Date, Region, Format), and simply copy the URL.

### Sample Input JSON

```
{
  "startUrls": [
    {
      "url": "https://adstransparency.google.com/advertiser/AR07117872862404280321?region=US&start-date=2025-05-22&end-date=2025-05-22"
    }
  ],
  "cookies": [], 
  "maxItems": 100,
  "downloadMedia": false,
  "proxyConfiguration": { "useApifyProxy": true }
}
```

## 📤 Output Structure

The data will be seamlessly generated inside your default dataset associated with the actor. Every item retains exhaustive insight structure:

```
{
  "id": "CR08100116008800354305",
  "advertiserId": "AR10303883279069085697",
  "creativeId": "CR08100116008800354305",
  "advertiserName": "My Jewellery B.V",
  "format": "IMAGE",
  "url": "https://adstransparency.google.com/advertiser/AR.../creative/...",
  "previewUrl": "https://encrypted-tbn2.gstatic.com/shopping?q=tbn:...",
  "firstShownAt": "2024-03-14T00:00:00.000Z",
  "lastShownAt": "2025-10-26T00:00:00.000Z",
  "impressions": "600000",
  "shownCountries": ["Germany"],
  "countryStats": [
    {
      "code": "DE",
      "name": "Germany",
      "impressions": {
        "lowerBound": "500000",
        "upperBound": "600000"
      },
      "platformStats": [
        {
          "name": "YouTube",
          "code": "YOUTUBE",
          "impressions": { "lowerBound": "8000", "upperBound": "9000" }
        }
      ]
    }
  ],
  "audienceSelections": [
    {
      "name": "Demographic info",
      "hasIncludedCriteria": true,
      "hasExcludedCriteria": false
    }
  ],
  "variants": [
    {
      "textContent": "Handykette mit Leopardemuster...",
      "images": [
        "https://encrypted-tbn2.gstatic.com/shopping?q=tbn:..."
      ]
    }
  ]
}
```

### ⚠️ Note on Private Authenticated Searches

If you choose to search for alcohol/gambling or other highly sensitive restricted ad domains, populate the `cookies` array using the export produced by the official [Cookie-Editor Extension](https://cookie-editor.com/).

Ensure you have browsed Google transparency tools first using that browser, export the JSON format natively, and paste it into the array field.

### Usage Legality Notice

Scraping public information from Google's Ads Transparency Center is broadly considered legal data consumption as the registry operates under mandatory government guidelines for public advertisement transparency. However, respect terms of services explicitly where appropriate to your jurisdiction!