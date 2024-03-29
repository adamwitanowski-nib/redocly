---
title: Quote and Purchase flows
---

# Quote and purchase flows

This section documents use-cases about embedding quote and purchase paths and providing a more tightly integrated user experience, allow for improved user experience and increased conversion rates.
## Quote and purchase flow

The sequence flow for retreiving a quote is typically the following. The sequence is the following:

 - Retrieve a quote based on supplied parameters including trip dates, destination country, country of residence. (If applicable to the brand) A list of available products with detailed pricing information will be returned. [Quotes API](/openapi/quotes/tag/Quote/paths/~1v1~1%7BbrandCode%7D~1quote/post/)
 - Add options to the quote and retrieve the updated pricing information [Options](/developer-portal/options.md)
 - Credit card tokenisation flow to the card token API [Credit card tokenisation API](/developer-portal/creditcards.md)
 - Purchase request utilising the tokenised credit card information.[Purchase API](/openapi/quotes/tag/Purchase/paths/~1v1~1%7BbrandCode%7D~1purchase/post/)

```mermaid
sequenceDiagram
    Client->>+Quotes API: Retrieve a quote (1)
    Quotes API->>+Client: Quote with prices 1)
    Client->>+Quotes API: Retrieve a quote with options (2)
    Quotes API->>+Client: Quote with prices, plus options (2)
    Client->>+Card Token API: Tokenise credit card input data (3)
    Card Token API->>+Client: Card token (3)
    Client->>+Quotes API: Purchase request including tokenised credit card information (4)
````

## Retrieving product benefits

The following sequence can be used to retrieve product benefits. It can include the following information:

 - Benefit name
 - Benefit description
 - Benefit limit and sub-limits

To access plan benefits it is recommend using the [Product benefits by Plan API](/openapi/products/tag/Plan/paths/~1v1~1%7BbrandCode%7D~1plans~1%7BplanId%7D~1benefits/get/). The plan ID parameter is passed back from the Quote response and applies to the individual plan documenting the detailed benefit and limits available.

 This can be used to avoid hard coding benefit limits in integrated purchase paths.
```mermaid
sequenceDiagram
    Client->>+Products API: Retrieve a list of benefits for a product (Plan Id)
    Products API->>+Client: Benefits with limits, description
````

## Policy documentation

To provide detailed policy specific documentation, including product disclosure statements, the Products API can be used to provide contextual links to display to the customer. To access policy wording for a choosen insurance contract you can access it by going to [PDS](/openapi/products/tag/InsuranceContract/paths/~1v1~1%7BbrandCode%7D~1insuranceContract~1%7BinsuranceContractId%7D~1pds/get/) link.

## Medical screening

It is recommended that a URL redirect be introduced to support medical screening of pre-existing conditions if this capability is required.
