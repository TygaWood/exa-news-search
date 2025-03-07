# EXA AI News
## Features

- Fetches AI-related updates using the **Exa API**.
- Searches across multiple categories: general search, domain-specific search, news, tweets, and blog posts.
- Filters out duplicate results.
- Saves **unique results** and **duplicate results** in JSON files.
- Criteria-based filtering for AI updates useful for developers and business owners.

## Installation

### Prerequisites

- **Node.js** (v14+ recommended)
- **NPM or Yarn**
- **Exa API Key** (Required for fetching data)

### Steps

1. Clone the repository:

   ```sh
   git clone https://github.com/TygaWood/exa-news-search.git
   cd exa-news-search
   ```

2. Install dependencies:

   ```sh
   npm install
   ```

3. Create a **.env** file in the root directory and add your Exa API key:

   ```sh
   EXA_API_KEY=your_api_key_here
   ```

## Usage

Run the script to fetch AI updates and filter them:

```sh
node test.js
```

## How It Works

The script performs **five types of searches** to retrieve AI-related content:

1. **Full Search:** General AI news search.
2. **Domain-Specific Search:** Fetches AI news from **trusted sources** (e.g., The Verge, TechCrunch, HackerRead, Dev.to).
3. **News Search:** Searches AI updates **excluding** domain-specific sites.
4. **Tweet Search:** Searches for AI-related tweets.
5. **Blog Post Search:** Finds AI-related blog posts.

After gathering results, it:

- Filters **duplicates**.
- Saves **unique results** in `unique_results.json`.
- Saves **duplicates** in `duplicates.json`.
- Ensures AI updates are **useful** for business owners and developers.

## Filtering Criteria

The script applies **strict filtering rules** to keep only relevant AI updates:

✔️ **Must be related to AI tools or updates.**  
✔️ **Should be useful for business owners and developers.**  
✔️ **Should not include unrelated AI news (e.g., AI in entertainment, politics, etc.).**

## JSON Output Schema

The filtered results are restructured into a **refined JSON schema**:

```json
[
  {
    "url": "https://www.example.com/article1",
    "title of update": "Article 1",
    "headline of the update": "The Key Takeaway of the AI Update",
    "summary": [
      "Key point 1",
      "Key point 2",
      "Key point 3"
    ],
    "developer/non developer": "developer",
    "pricing": "Free / Paid / Subscription-based",
    "helpful for work professionals": "Yes / No",
    "availability": "Beta / Public / Waitlist"
  }
]
```

## File Output

- **`unique_results.json`** → Contains refined AI updates.
- **`duplicates.json`** → Stores duplicate results.

## Error Handling

The script ensures that any API failures or parsing issues are handled gracefully by logging errors instead of crashing.

## Contributing

Feel free to open issues or submit pull requests!

---

This README provides a clear explanation of how the script works, how to use it, and what to expect from its output. You can update the **GitHub repo link** and **author details** as needed. 🚀
