---
title: Options
---

# Options

Options are optional extras that can be added to the product after a plan is selected.

These can be added using the [Quotes API with Options](/openapi/quotes/tag/Quote/paths/~1v1~1%7BbrandCode%7D~1quotewithoptions/post/) method.

## Available options

The following are the available options available. Note that each product offered will not support all options provided below and available options will be product dependent:

| Option Code | Description |
| ----------- | ----------- | 
| POLEXCESS   | Policy excess |
| CAREXCESS   | Rental car excess |
| SPECITEMS | Specified item excess |
| ADVENTUREACTIVITY | Adventure activity (World Nomads only) |
| SNOWSPORTS | Snow sports |
| TRIPCANX | Trip cancellation value |
| POLEXCESSPERCENT | Policy excess buy out option |
| TRIPCANXPERCENT | Trip cancellation percentage |
| CRUISE | Cruise option |

## Basic option requests

Basic options are used to configure Snow sports, policy excess buy out percentage.

  - What other options fall under basic option specification? How do we know what a basic
  - verse other option type is?

```javascript
basicOptions : [
  {
   “SNOWSPORTS”, isOptedIn : true
  },
  basicOptions : {
    “POLICYEXCESSPERCENT”, OptedInValue : 0
  }
]
```

## Specified item option requests

| Attribute | Description |
| ----------- | ----------- | 
| name   | Name of specified item (E.g. 'iphone 14') |
| itemValue | Requested value to cover the specified item option |
| itemTypeCode | The following types are available:
 - Electronic
 - Sport
 - Other|

```javascript
specifiedItemOption : {
"SPECITEMS",
specfifiedItems : [
   "iPhone 14", 
   "1000",
   "Electronic"
]
}
```

## Cancellation option requests

The following request provides ability to adjust cancellation cover limits:

```javascript
cancellationOption : {
"TRIPCANXPERCENT",
cancellationCoverLimit: 0
}
```

## Cruise ship option requests

