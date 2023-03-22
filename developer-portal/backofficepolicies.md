---
title: Backoffice integration for policies
---

# Backoffice integration for policies

This use-cases is to support any partners to fetch policies details for a partner and brand specific only.

## Use case example

This is drafted while we have a partner who would like to have this supported via powerSuite travel management application.


## Detail flow

The sequence flow for retreiving policy details for a partner and brand is typically the following. 

Between Partner & PowerSuite:
 - Partner logins to PowerSuite application
 - PowerSuite provides an ability for the logged in partner user to enter a policy number
 - PowerSuite then uses the configured partner credentials to connect to nibAPI. (the credentials will be provided by nib)

Between PowerSuite & nib APIs:
- call is made to the user API to get an access token
- use this as a bearer token to make a call to the policies end point
- on success share the policies details payload
- send 401 error response code if the partner is not a valid partner or the brand is invalid


sequence diagram goes here ......


## Error responses

| Error Response Code           | Description                 | 
| :---------                    | :-------                    |   
| 401                           | unauthorized (may be the partner code and brand are invalid)          |

## API contracts

Contract and payload sample goes here ..
