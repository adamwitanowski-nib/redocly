---
title: Country list
---

# Country list

The country list configured for a selected brand is avialable in quoteCountriesConfig endpoint.

# API format specification

You can pass in the quote type into the endpoint for quoteCountries configuration:

 - SINGLETRIP 
 - MULTITRIP

The homeCountries attribute describes which countries the product is available for sale.

The destinationCountries describes the current available sale countries 
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

To retrieve the list of no products offered to this country, unsafe and sanctioned countries utilise the baseQuoteConfig endpoint. The following information is available for each home country:

 - noProductCountryCodes
 - unsafeCountryCodes
 - sanctionedCountryCodes 