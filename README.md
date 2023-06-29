# Open Projects Data

## Overview

In this repository one can find data for crypto projects.
When a submitted PR is accepted and merged it automatically updates the Santiment database.
The updated data will be available in the Santiment API and it can be used in the computation of metrics.

## Data

The data includes, but is not limited to:
- General data:
  - Slug
  - Name
  - Ticker
  - Ecosystem
  - Website
  - Description
  - Market Segment
- Development data:
  - Github organizatoins
- Social data:
  - Twitter 
  - Discord
  - Slack
  - Telegram
  - Reddit
  - Blog
- Blockchain data:
  - Contracts - address, decimals, description

### Data example

The following is an example of the data for the Santiment project:

```json
{
  "general": {
    "slug": "santiment",
    "ecosystem": "/Ethereum",
    "name": "Santiment",
    "ticker": "SAN",
    "description": "Data feeds, insights and crowd sentiment",
    "website": "https://santiment.net/"
  },
  "social": {
    "twitter": "https://twitter.com/santimentfeed",
    "telegram": "https://t.me/santiment_network",
    "discord": "https://santiment.net/discord",
    "reddit": "https://www.reddit.com/r/santiment/"
  },
  "development": {
    "github_organizations": ["santiment"]
  },
  "blockchain": {
    "contracts": [
      {
        "address": "0x7c5a0ce9267ed19b22f8cae653f198e3e8daf098",
        "label": "main",
        "blockchain": "ethereum",
        "decimals": 18
      }
    ]
  }
}
```
### Updating the data

To update the data for a project, one should submit a PR with the proposed changes.

An example of a change that adds a new github organization:
```diff
  "development": {
    "github_organizations": [
-      "santiment"
+      "santiment", "santiment_new_organization"
    ]
  },
```
If this change is accepted and merged, the Santiment database will be updated and the new organization will be added to the list of organizations for the Santiment project.
This will be reflected in the Development Activity metrics of the project.