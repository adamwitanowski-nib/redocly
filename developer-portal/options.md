---
title: Options
---

# Options

Options are optional extras that can be added to the product after a plan is selected.

## Available options

The following are the available options available. Note that each product offered will not support all options provided below.

| Code        | Description |
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

## Sample option requests

The following shows the structure of the option request:

```javascript
basicOptions : [
  {
   “SNOWSPORTS”, isOptedIn : true
  },
  basicOptions : {
    “POLICYEXCESSPERCENT”, OptedInValue : 0
  }
]

specifiedItemOption : {
optionType
specfifiedItems : [
   "name", 
   "itemValue",
   "itemTypeCode"
]
}

cancellationOption : {
optionType,
cancellationCoverLimit: 0
}
````

