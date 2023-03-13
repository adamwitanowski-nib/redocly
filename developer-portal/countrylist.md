---
title: Country list
---

# Country list

The country list configured for a selected brand is available in quoteCountriesConfig endpoint.

## API format specification

You can pass in the quote type into the endpoint for quoteCountries configuration:

 - SINGLETRIP 
 - MULTITRIP

The homeCountries attribute describes which countries the product is available for sale.

### Available country list

The destinationCountries describes the current available countries and destinations. This includes no product, unsafe and sanctioned country codes which are filtered out separately.

The country list returned includes 3 digit codes which are sent in the quote API request, name and country aliases.

Country aliases can be used to define common alternative names to the country names.

```javascript
    {
      "code": "ARG",
      "name": "Argentina",
      "sentenceName": "Argentina",
      "isTravelActivity": false,
      "effectiveToDate": "1970-01-01T00:00:00Z",
      "effectiveFromDate": "1970-01-01T00:00:00Z",
      "aliases": [
        "Argentina",
        "Buenos Aires",
        "Patagonia"
      ]
    }
```

The following is an example of AMT region configuration, which are listed out separately:

```javascript
    {
      "code": "WWD",
      "name": "Worldwide",
      "sentenceName": "Worldwide",
      "isTravelActivity": false,
      "effectiveToDate": "1970-01-01T00:00:00Z",
      "effectiveFromDate": "1970-01-01T00:00:00Z",
      "aliases": [
        "Worldwide"
      ]
    }
```

### Country restrictions

To retrieve the list of no products offered to this country, unsafe and sanctioned countries utilise the baseQuoteConfig endpoint. The following information is available for each home country:

 - noProductCountryCodes
 - unsafeCountryCodes
 - sanctionedCountryCodes 