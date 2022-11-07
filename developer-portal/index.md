---
title: Introduction
---
# Overview

This developer portal is designed to let you utilise nib Travel APIs. These APIs provide the ability to provide
integrated experiences around customised quote and purchase flows.

# Environment access

To access the environments utilise the following URL for staging and production environments respectively:

| Environment  | URL |
| ------------- | ------------- |
| Staging  | https://api-staging.nibtravelinsurance.com  |
| Production  | https://api.nibtravelinsurance.com |

# API access conventions

APIs will be required to include a brand code parameter as part of the URL parameters passed in. This will typically be set to the brand instance. Example brand codes for nib Travel brands include:

| BrandCode  | Brand |
| ------------- | ------------- |
| WN  | World Nomads  |
| TIDAU  | Travel Insurance Direct Australia |
| NIBAU  | NIB Travel Insurance (Australia) |

Individual APIs are accessed via top level URL prefix, for example:

| API  | URL |
| ------------- | ------------- |
| Quotes API  | https://api.nibtravelinsurance.com/quotes  |
| Products API  | https://api.nibtravelinsurance.com/products |
 
# Error handling

nib Travel APIs have the following HTTP status codes returned for error handling:

| HTTP Status code  | Details |
| ------------- | ------------- |
| 200  | Successful request - Individual responses are documented in Swagger  |
| 400  | Client error - see { error } property returned in JSON format. |
| 401  | Unauthorised request |
| 500  | Server error |

# Authentication

nib Travel API access is access via a Bearer token authorization set in the HTTP Header. 

```
Authorization: Bearer <BearerToken>
```

Access details and mechanisms can be supplied by the nib Travel partnerships team as part of the onboarding process.

