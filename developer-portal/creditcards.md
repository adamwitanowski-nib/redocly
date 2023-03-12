---
title: Credit card tokenisation
---

# Overview

nib travel insurance is PCI-DSS certified and supports been the merchant of record.

nib has a tokenisation endpoint, to support scenarios such as fail over between multiple payment gateways used for redundancy and to support different tender types. This separation is to enforce strict security boundaries and avoid core APIs been involved in PCI scope.

# Tokenisation request

To tokenise the request you need to send the card information to the Card tokenisation endpoint. This provides a one-time use token endpoint for any purchase transactions.

To support this you can pass in the following request to the card token API. This returns a token that can be used in the Quote API Booking request:

```javascript
{
"source": "string",
"pan": "string",
"expiryMonth": 1,
"expiryYear": 2018,
"cardHolderName": "string"
}
```

