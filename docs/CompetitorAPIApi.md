# Ninjapear.CompetitorAPIApi

All URIs are relative to *https://nubela.co*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getCompetitorListing**](CompetitorAPIApi.md#getCompetitorListing) | **GET** /api/v1/competitor/listing | Competitor Listing



## getCompetitorListing

> CompetitorListingResponse getCompetitorListing(website)

Competitor Listing

Discover direct business competitors of a target company. Competitors are identified via organic keyword overlap and AI-powered product comparison.  **Cost:** 2 credits/competitor returned. Minimum 5 credits per request.

### Example

```javascript
import Ninjapear from 'ninjapear';
let defaultClient = Ninjapear.ApiClient.instance;
// Configure Bearer access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new Ninjapear.CompetitorAPIApi();
let website = "https://www.stripe.com"; // String | The website URL or company name of the target company. A website URL (e.g. `https://www.stripe.com`) is strongly recommended for precision.
apiInstance.getCompetitorListing(website, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **website** | **String**| The website URL or company name of the target company. A website URL (e.g. &#x60;https://www.stripe.com&#x60;) is strongly recommended for precision. | 

### Return type

[**CompetitorListingResponse**](CompetitorListingResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

