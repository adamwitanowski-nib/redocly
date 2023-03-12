---
title: External Membership numbers
---

# External Membership numbers

nib travel insurance system supports storing external membership numbers associated to the policy information.

There is optional membership API validation based on integration with specific membership number types. These are validated against other details entered as part of the quote and booking flow, such as first name, last name and date of birth. (For example)

# API format specification

```javascript
externalIdentifiers : {
"externalMembershipNumber" : 12345678
}
```

