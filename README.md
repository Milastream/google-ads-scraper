[Google Ads Scraper](https://apify.com/lexis-solutions/google-ads-scraper?fpr=data)

# Google Ads Scraper

![banner](https://images.apifyusercontent.com/fVv9CPTnW-sVY2MEPnsTB1XK8R8ujw9RTEBh1eHeTM0/w:1800/cb:1/aHR0cHM6Ly9sZXhpcy1zb2x1dGlvbnMtYXBpZnkuZnJhMS5jZG4uZGlnaXRhbG9jZWFuc3BhY2VzLmNvbS9nb29nbGUtYWRzL2JnLnN2Zw.webp)

## What is the Google Ads Scraper?

The Google Ads Scraper is designed to extract data from Google's Ads Transparency Center. It enables users to gather information about ads displayed on Google's advertising network, focusing on transparency and the details of advertisers. Users can search Google ads by company, domain, or country, and filter ads by date range and format.

🆕 This actor now scrapes all formats of ads on Google Ads - images, videos, and text.

- 🎥 Watch the [video tutorial](https://www.youtube.com/watch?v=nK_x32d-bcU) on Scraping Google Ads with this actor

## 🔄 Comparison: Lexis vs Competitor

| Feature | Competitor | Lexis Scraper |
| --- | --- | --- |
| Avg Speed (100 ads) | 81s | **39s** 🚀 |
| Ad formats | Text, Image, Video | Text, Image, Video |
| Media download | ✅ | ✅ |
| `url` (full ad link) | ❌ | ✅ |
| `firstShownAt` (first launch date) | ❌ | ✅ |
| `audienceSelections` (target audience) | ❌ | ✅ |
| Age-restricted ads | ❌ | ✅ |
| Reliability | Occasional gaps | **Error-free runs** ✅ |

# Features

- ⚡ 2× faster than competitor scrapers – scrape 100 ads in just 39 seconds
- Scrapes all ad formats: TEXT, IMAGE, and VIDEO
- Extracts variants with decoded ad text and media links
- Per-country impression ranges and per-platform impression stats
- Audience selections with include/exclude flags
- Optional media downloading to Key-Value Store with stored keys in output
- Cookie support to unlock restricted content
- Proxy support for geo-targeted results
- Supports both search URLs and direct creative detail URLs
- Pagination with `maxItems` control

✨ Exclusive fields you won’t find in competitor scrapers:

- url → full ad link
- firstShownAt → when the ad was first launched
- audienceSelections → target audience info

## What data can the Google Ads Scraper extract?

The Google Ads Scraper can extract the following data from the Ads Transparency Center:

- Advertiser name
- Advertiser ID
- Creative ID (Ad ID)
- Format (TEXT, IMAGE, VIDEO)
- Detail URL
- Preview URL (primary media link)
- First shown date
- Last shown date
- Impressions (range, if available)
- Shown countries
- Country stats (per country first/last shown, impression bounds)
- Platform stats per country (YouTube, Shopping, Search, with impression bounds)
- Audience selections (targeting categories; included/excluded flags)
- Variants (extracted ad text and media/video/image links)
- Origin URL (the source Transparency Center search URL)

## What use cases does the Google Ads Scraper have?

- 👀 Competitive analysis
- 💻 Market research
- 📊 Data journalism
- 📈 Marketing agencies tracking competitor ads
- 🎨 Creative teams analyzing ad media & formats
- 🕵️‍♂️ Compliance teams monitoring ad transparency

## How to use the Google Ads Scraper

1. Create a free Apify account
2. Open Google Ads Scraper
3. Add one or more Google Transparency Center URLs to the input
4. Click Start and wait for the results
5. Download the results in JSON, XML or CSV format or connect the actor to your backend via API

## ⚠️ Note on Ad Visibility

The number of ads retrieved depends on two key factors:

- ✅ **Authentication** – Use cookies from a logged-in Google account (preferably a test account) to access age-restricted or personalized ads. Never share your cookies to protect your privacy.
- 🌍 **Location (IP-based)** – Google shows different ads based on your region. To fetch ads from a specific country, use a proxy for that region.

Example proxy config for US:

```
{
  "proxyConfiguration": {
    "useApifyProxy": true,
    "apifyProxyGroups": ["US"]
  }
}
```

> Here is how you can integrate your cookies:
> 
> 
> 
> 
> 1. Install the [**Cookie-Editor** Chrome extension](https://chromewebstore.google.com/detail/cookie-editor/hlkenndednhfkekhgcdicdfddnkalmdm?pli=1).
> 2. Go to [Google Ads Transparency Center](https://adstransparency.google.com).
> 3. Open the **Cookie-Editor** extension and **export your cookies** in **JSON format**.
> 4. Copy the exported cookie data and **paste it into the input field** provided here.
> ![Example 1](https://images.apifyusercontent.com/fdIxoUAB1IYnNKoAuSzU5B3HQgqpzxgmpWyi4br7LOc/w:1800/cb:1/aHR0cHM6Ly9pLmliYi5jby9xTEJGM21Cay9jb29raWVzLTEucG5n.webp) ![Example 2](https://images.apifyusercontent.com/w2rsP9xPyqubac0nDC7vFbpZmqtXu1Q0AiTWFNypc94/w:1800/cb:1/aHR0cHM6Ly9pLmliYi5jby81eHJ6WEw5Ui9jb29raWVzLTIucG5n.webp) ![Example 3](https://images.apifyusercontent.com/q5ifGwXhQjy3FqAcuSxvCTynOiiNFWKhG7ZtJtzlJjA/w:1800/cb:1/aHR0cHM6Ly9pLmliYi5jby9MZDVGQ05TTS9jb29raWVzLTMucG5n.webp)

## 📥 Input

To run the actor, you'll need at least one Google Transparency Center URL.

Opening the [Google Transparency Center](https://adstransparency.google.com/) in your browser, you can see a search form like below.

![banner](https://images.apifyusercontent.com/exgy-WEEwXf_6Jas9UdhKizDfQDoVCVZ2yCipFpwVLY/w:1800/cb:1/aHR0cHM6Ly9sZXhpcy1zb2x1dGlvbnMtYXBpZnkuZnJhMS5jZG4uZGlnaXRhbG9jZWFuc3BhY2VzLmNvbS9nb29nbGUtYWRzL2Zvcm0ucG5n.webp)

Here you can use the search form to filter the ads by:

1. Dates - the date range when the ad was shown
2. Countries - the countries where the ad was shown
3. Format - the format of the ad (text, image, video)
4. Advertiser - the name of the advertiser, or the domain of the advertiser's website

Once you've set up the search form, click enter, and the URL in your browser will change. Copy this URL and paste it into the input field in the actor.

Sample URLs you can use:

- [https://adstransparency.google.com/advertiser/AR09717407487665111041?region=anywhere](https://adstransparency.google.com/advertiser/AR09717407487665111041?region=anywhere) - all ads from the advertiser "Facebook Technologies LLC", shown anywhere in the world, in any format, in any date range
- [https://adstransparency.google.com/advertiser/AR09717407487665111041?region=DE&preset-date=Last+7+days&format=TEXT](https://adstransparency.google.com/advertiser/AR09717407487665111041?region=DE&preset-date=Last+7+days&format=TEXT) - all text ads from the advertiser "Facebook Technologies LLC", shown in Germany, in the last 7 days
- [https://adstransparency.google.com/?region=anywhere&domain=facebook.com](https://adstransparency.google.com/?region=anywhere&domain=facebook.com) - all ads from Facebook domain

### 📥 Sample Input

```
{
  "startUrls": [
    {
      "url": "https://adstransparency.google.com/advertiser/AR07117872862404280321?region=US&start-date=2025-05-22&end-date=2025-05-22"
    }
  ],
  "cookies": [], // (NOT REQUIRED) used to retreive more data (age-restriction content)
  "maxItems": 40,
  "downloadMedia": false,
  "proxyConfiguration": { "useApifyProxy": true }
}
```

## 📥 Input schema

- startUrls (array of { url: string }) – required
- cookies (array) – optional; JSON from Cookie-Editor
- maxItems (integer) – optional; default 100
- proxyConfiguration (object) – optional; Apify proxy settings
- downloadMedia (boolean) – optional; default false. When true, media is downloaded to KV Store and keys are returned in `media-store`

## 📤 Output

The results are stored in the default dataset associated with the actor. Each item is an ad, having the following format:

```
{
  "id": "CR08100116008800354305",
  "advertiserId": "AR10303883279069085697",
  "creativeId": "CR08100116008800354305",
  "advertiserName": "My Jewellery B.V",
  "format": "IMAGE",
  "url": "https://adstransparency.google.com/advertiser/AR10303883279069085697/creative/CR08100116008800354305?region=DE&platform=YOUTUBE&start-date=2022-01-01&end-date=2024-12-31&format=IMAGE",
  "previewUrl": "https://encrypted-tbn2.gstatic.com/shopping?q=tbn:ANd9GcT5cZ5keol3Qh0OGy8BxONGNpoc9OeRl771pz5cN4FnyOwhmGU",
  "previewStoreKey": "CR08100116008800354305_preview_0.jpg",
  "firstShownAt": "1710421161",
  "lastShownAt": "1758540064",
  "impressions": "600000",
  "shownCountries": ["Germany"],
  "countryStats": [
    {
      "code": "DE",
      "name": "Germany",
      "firstShownAt": "2024-03-14T00:00:00.000Z",
      "lastShownAt": "2025-09-22T00:00:00.000Z",
      "impressions": {
        "lowerBound": "500000",
        "upperBound": "600000"
      },
      "platformStats": [
        {
          "name": "YouTube",
          "code": "YOUTUBE",
          "impressions": {
            "lowerBound": "8000",
            "upperBound": "9000"
          }
        },
        {
          "name": "Google Shopping",
          "code": "SHOPPING",
          "impressions": {
            "lowerBound": "3000",
            "upperBound": "4000"
          }
        },
        {
          "name": "Google Search",
          "code": "SEARCH",
          "impressions": {
            "lowerBound": "450000",
            "upperBound": "500000"
          }
        }
      ]
    }
  ],
  "audienceSelections": [
    {
      "name": "Demographic info",
      "hasIncludedCriteria": true,
      "hasExcludedCriteria": false
    },
    {
      "name": "Geographic locations",
      "hasIncludedCriteria": true,
      "hasExcludedCriteria": true
    },
    {
      "name": "Contextual signals",
      "hasIncludedCriteria": true,
      "hasExcludedCriteria": true
    }
  ],
  "variants": [
    {
      "textContent": "Handykette mit Leopardemuster | My Jewellery - My Jewellery - Bigshopper",
      "images": [
        "https://encrypted-tbn2.gstatic.com/shopping?q=tbn:ANd9GcT5cZ5keol3Qh0OGy8BxONGNpoc9OeRl771pz5cN4FnyOwhmGU"
      ],
      "imageStoreKeys": ["CR08100116008800354305_v0_0.jpg"]
    }
  ],
  "originUrl": "https://adstransparency.google.com/advertiser/AR10303883279069085697?region=DE&platform=YOUTUBE&start-date=2022-01-01&end-date=2024-12-31&format=IMAGE"
}
```

## How many Google Ads can the Google Ads Scraper extract?

The Google Ad Transparency Center Scraper uses pagination to extract all job listings from Google Ad Transparency Center. You can control the number of job listings to scrape by setting the `maxItems` input parameter. If you don't set the `maxItems` parameter, the scraper will extract all job listings available on the website.

## Why use the Google Ads Scraper?

- ⚡️ **Fast** - The scraper is fast and efficient, allowing you to scrape ads in a programmatic way.
- 🤙 **Easy to use** - The scraper is easy to use and requires no coding knowledge. All you need to do is input the companies you want to scrape and the scraper will do the rest.
- ☑️ **Well-Maintained** - The scraper is maintained by the Lexis Solutions team, ensuring that it is always up-to-date and working properly.

## FAQ

- **How to find a company's ads on Google?**

To find a company's ads on Google, you can use the Google Ads Transparency Center. This tool allows you to search for ads by advertiser name, domain, or country.
- **How to search for ads on Google?**

Google Ads Transparency Center allows you to search for ads by advertiser name, domain, or country. You can also filter ads by date range and format. If you need to obtain the data programmatically, you can use the Google Ads Scraper.
- **What is the Google Ads Transparency Center?**

The Google Ads Transparency Center is a website that allows users to view ads that are displayed on Google's advertising network. It also provides information about the advertisers who are running these ads.
- **What is the Google Ads Scraper?**

The Google Ads Scraper is a web scraping tool designed specifically for Google's Ads Transparency Center. This tool offers an effective way to mine valuable data from ads displayed on Google's advertising network.
- **Is Scraping Google Ads Legal?**

Scraping public information from Google's Ads Transparency Center is legal as long as you are not violating any terms of service or privacy policies. However, it is important to note that scraping ads can be considered a violation of the terms of service of some websites, so it is always best to check before scraping.
- **How much does it cost?**

The cost for using the Google Ads Scraper is shown on the top of this page. You can also check the Apify Store page for more information.

## Need to scrape ads from Bing?

👉 Scrape Bing ads with [Bing Ads Scraper](https://apify.com/lexis-solutions/bing-ads-scraper)

## Need to scrape ads from TikTok?

👉 Scrape TikTok ads with [TikTok Ads Scraper](https://apify.com/lexis-solutions/tiktok-ads-scraper)

## Need to scrape ads from Reddit?

👉 Scrape Reddit ads with [Reddit Ads Scraper](https://apify.com/lexis-solutions/reddit-ads-scraper)

---

👀 p.s.

Got feedback or need an extension?

Lexis Solutions is a [certified Apify Partner](https://apify.com/partners/find). We can help you with custom solutions or data extraction projects.

Contact us over [Email](mailto:scraping@lexis.solutions) or [LinkedIn](https://www.linkedin.com/company/lexis-solutions)

## Support Our Work 💝

If you're happy with our work and scrapers, you're welcome to leave us a company review [here](https://apify.com/partners/find/lexis-solutions/review) and leave a review for the scrapers you're subscribed to. It will take you less than a minute but it will mean a lot to us!

Image Credit: Google Transparency Center