# Bitcoin News

## Introduction

**Bitcoin News API** retrieves all the latest news of Bitcoin around the world from all the major websites.

## Authentication

The URL you need to use is the following: `https://bitcoin-news1.p.rapidapi.com/`
The API requires the headers listed below:

- **`x-rapidapi-host`**: `bitcoin-news1.p.rapidapi.com`
- **`x-rapidapi-key`**: `YOUR_API_KEY`

Make sure to replace `YOUR_API_KEY` with your API key. You can register one [here](https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/bitcoin-news1/pricing).
Some frameworks automatically add extra headers, you have to make sure to remove them in order to get a response from the API.

## Endpoints

The API is configured to accept only **GET** requests. Below are the available endpoints with their descriptions and required parameters.

### 1. **`GET /news`**

- **Description**: Retrieves a list of all available news articles in the system.

Example request:

```javascript
fetch('https://bitcoin-news1.p.rapidapi.com/news', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'bitcoin-news1.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
[
  {
    "title": "Bitcoin Offerings",
    "url": "https://www.coindesk.comhttps://www.coindesk.com/indices/bitcoin",
    "source": "coindesk"
  },
  {
    "title": "Bitcoin",
    "url": "https://www.coindesk.com/tag/bitcoin/",
    "source": "coindesk"
  },
  {
    "title": "Bitcoin Prices Take Breather as BTC ETFs Record Another Day of Monster Inflows",
    "url": "https://www.coindesk.com/markets/2024/10/31/bitcoin-prices-take-breather-as-btc-etfs-record-another-day-of-monster-inflows/",
    "source": "coindesk"
  },
  {
    "title": "Bitcoin",
    "url": "https://www.coindesk.com/tag/bitcoin/",
    "source": "coindesk"
  },
  {
    "title": "Bitcoin Surges Above $71K as Wild Crypto Market Pump Sees $175M in Shorts Liquidated",
    "url": "https://www.coindesk.com/markets/2024/10/29/bitcoin-surges-above-71k-as-wild-crypto-market-pump-sees-175m-in-shorts-liquidated/",
    "source": "coindesk"
  },
  {
    "title": "Bitcoin Has a Lot Going for It, Except the Persistent Slide in Copper-Gold Ratio",
    "url": "https://www.coindesk.com/markets/2024/10/28/bitcoin-has-a-lot-going-for-it-except-the-persistent-slide-in-copper-gold-ratio/",
    "source": "coindesk"
    ...
```

### 2. **`GET /news/:newspaperId`**

- **Description**: Retrieves articles from a specific newspaper.

| Path Parameter | Type   | Default | Description                                                 | Required |
|----------------|--------|---------|-------------------------------------------------------------|----------|
| `newspaperId`  | string | -       | The ID of the newspaper from which to retrieve the articles | Yes      |

Example request:

```javascript
fetch('https://bitcoin-news1.p.rapidapi.com/news/IndiaTimes', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'bitcoin-news1.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
[
  {
    "title": "How did the Bitcoin whitepaper shape the crypto world we see today?",
    "url": "https://economictimes.indiatimes.com/news/bitcoinhttps://economictimes.indiatimes.com/markets/cryptocurrency/how-did-the-bitcoin-whitepaper-shape-the-crypto-world-we-see-today/articleshow/114804472.cms",
    "source": "IndiaTimes"
  },
  {
    "title": "Bitcoin prices surge past $71,000 amid speculation around US election",
    "url": "https://economictimes.indiatimes.com/news/bitcoinhttps://economictimes.indiatimes.com/markets/cryptocurrency/bitcoin-prices-surge-past-71000-amid-speculation-around-us-election/articleshow/114715494.cms",
    "source": "IndiaTimes"
  },
  {
    "title": "Bitcoin surges past $73,500 as US election speculation fuels demand",
    "url": "https://economictimes.indiatimes.com/news/bitcoinhttps://economictimes.indiatimes.com/markets/cryptocurrency/bitcoin-surges-past-73500-as-us-election-speculation-fuels-demand/articleshow/114763504.cms",
    "source": "IndiaTimes"
  },
  {
    "title": "Bitcoin approaches all-time highs: Is an altcoin season on the horizon?",
    "url": "https://economictimes.indiatimes.com/news/bitcoinhttps://economictimes.indiatimes.com/markets/cryptocurrency/bitcoin-approaches-all-time-highs-is-an-altcoin-season-on-the-horizon/articleshow/114804568.cms",
    "source": "IndiaTimes"
  },
  {
    "title": "Cryptocurrency prices on October 24: Bitcoin holds above $67,300; Altcoins trade mixed",
    "url": "https://economictimes.indiatimes.com/news/bitcoinhttps://economictimes.indiatimes.com/markets/cryptocurrency/cryptocurrency-prices-on-october-24-bitcoin-holds-above-67300-altcoins-trade-mixed/articleshow/114538565.cms",
    "source": "IndiaTimes"
  },
  {
    "title": "Bitcoin jumps above $69,000, reaching 3-month high as Trump's election odds increase",
    "url": "https://economictimes.indiatimes.com/news/bitcoinhttps://economictimes.indiatimes.com/markets/cryptocurrency/bitcoin-jumps-above-69000-reaching-3-month-high-as-trumps-election-odds-increase/articleshow/114420024.cms",
    "source": "IndiaTimes"
    ...
```

### 3. **`GET /newsv2`**

- **Description**: Retrieves stock-related news articles.

Example request:

```javascript
fetch('https://bitcoin-news1.p.rapidapi.com/newsv2', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'bitcoin-news1.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
[
  {
    "source": {
      "id": "wired",
      "name": "Wired"
    },
    "author": "Andy Greenberg",
    "title": "Meet ZachXBT, the Masked Vigilante Tracking Down Billions in Crypto Scams and Thefts",
    "description": "He just untangled a $243 million bitcoin theft, what may be the biggest-ever crypto heist to target a single victim. And he has never shown his face.",
    "url": "https://www.wired.com/story/meet-zachxbt-243-million-crypto-theft/",
    "urlToImage": "https://media.wired.com/photos/671803d2124551b4eaed68ad/191:100/w_1280,c_limit/security_zachxbt_crypto_vigilante.jpg",
    "publishedAt": "2024-10-24T09:00:00Z",
    "content": "As ZachXBT has pursued that career as a crypto vigilante, he has also kept his mask firmly in place. Online, he appears only as his avatar, a kind of platypus cartoon figure in a detective's trench c… [+3865 chars]"
  },
  {
    "source": {
      "id": "wired",
      "name": "Wired"
    },
    "author": "Joel Khalili",
    "title": "Peter Todd Was ‘Unmasked’ As Bitcoin Creator Satoshi Nakamoto. Now He’s In Hiding",
    "description": "Peter Todd has gone underground after an HBO documentary named him as the creator of Bitcoin, Satoshi Nakamoto, whose real identity has long remained a mystery.",
    "url": "https://www.wired.com/story/peter-todd-was-unmasked-as-bitcoin-creator-satoshi-nakamoto-now-hes-in-hiding/",
    "urlToImage": "https://media.wired.com/photos/6716870e6874cb5feda0798e/191:100/w_1280,c_limit/102124-bitcoin-satoshi-an.jpg",
    "publishedAt": "2024-10-22T11:33:59Z",
    "content": "In the week before the documentary was released, online betting markets had Len Sassaman, a cryptographer who moved in similar online circles to Satoshi, as the most likely candidate to be revealed a… [+2075 chars]"
  },
  {
    "source": {
      "id": "wired",
      ...
```

## Error Handling

The  API returns standard HTTP status codes to indicate the success or failure of API requests. Below are common errors and suggestions for handling them.

|Status Code|Message|Description|Suggested Handling|
|--|--|--|--|
| **400** | Bad Request | The request was malformed or missing required parameters (e.g., `domain` parameter not provided). | Verify that all required parameters are included and correctly formatted. |
| **401** | Unauthorized | Invalid or missing API key in the request headers. | Check that a valid API key is included in `x-rapidapi-key`. |
| **403** | Forbidden | Access to the requested resource is denied, possibly due to rate limits or restricted access. | Review rate limits and ensure API permissions. Retry after a delay if rate limit exceeded. |
| **404** | Not Found | The requested domain information could not be found (e.g., domain does not exist). | Check the spelling or availability of the domain. |
| **429** | Too Many Requests | The API rate limit has been exceeded. | Implement rate-limiting logic and retry after the specified rate limit reset time. |
| **500** | Internal Server Error | A server error occurred while processing the request. | Retry the request after a few seconds. If the error persists, contact API support. |
| **503** | Service Unavailable | The API service is temporarily unavailable (e.g., due to maintenance). | Retry the request later or check the API status page for maintenance alerts. |

