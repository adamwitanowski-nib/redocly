---
title: Backoffice integration for policies
---

# Backoffice integration for policies

This use-cases is to support any partners to fetch policies details for a partner and brand specific only.


## Detail flow

The sequence flow for retreiving policy details for a partner and brand is typically the following. 

- call is made to the user API to get an access token using user credentials
- use this as a bearer token to make a call to the policies end point
- on success share the policies details payload
- send 401 error response code if the partner is not a valid partner or the brand is invalid



## Error responses

| Error Response Code           | Description                 | 
| :---------                    | :-------                    |   
| 401                           | unauthorized (may be the partner code and brand are invalid)          |

## API contracts


