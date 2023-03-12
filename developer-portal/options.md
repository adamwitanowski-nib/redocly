---
title: Options
---

# Options

Options are optional extras that can be added to the product after a plan is selected.

## Available options

The following are the available options available. Note that each product offered will not support all options provided below.

| Option Code | Description |
| ----------- | ----------- | 
| POLEXCESS   | Policy excess |
| CAREXCESS   | Rental car excess |
| SPECITEMS | Specified item excess |
| ADVENTUREACTIVITY | Adventure activity (World Nomads only) |
| SNOWSPORTS | Snow sports |
| TRIPCANX | Trip cancellation value |
| POLEXCESSPERCENT | Policy excess buy out percentage |
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

name - Name of specified item (E.g. 'iphone 14')
itemValue - Requested value to cover the specified item option. Needs to be below the individual item limit on the policy.
itemTypeCode - TBC, how do get the value of the individual itemTypeCodes? Where this is configured in the API definition?

```javascript
specifiedItemOption : {
optionType
specfifiedItems : [
   "name", 
   "itemValue",
   "itemTypeCode"
]
}
```

## Cancellation option requests

```javascript
cancellationOption : {
optionType,
cancellationCoverLimit: 0
}
```

## Cruise ship option requests

