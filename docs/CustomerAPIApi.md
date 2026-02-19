# Ninjapear.CustomerAPIApi

All URIs are relative to *https://nubela.co*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getCustomerListing**](CustomerAPIApi.md#getCustomerListing) | **GET** /api/v1/customer/listing | Customer Listing



## getCustomerListing

> CustomerListingResponse getCustomerListing(website, opts)

Customer Listing

Get a list of highly-probable customers, investors, and partners/platforms of a target company, categorized by relationship type.  **Cost:** 1 credit/request + 2 credits/company returned. Credits are charged even when the request returns an empty result.

### Example

```javascript
import Ninjapear from 'ninjapear';
let defaultClient = Ninjapear.ApiClient.instance;
// Configure Bearer access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new Ninjapear.CustomerAPIApi();
let website = "https://www.stripe.com"; // String | The website URL of the target company
let opts = {
  'cursor': "cursor_example", // String | Pagination cursor from `next_page` in a previous response
  'pageSize': 200, // Number | Number of results per page (1-200, default 200)
  'qualityFilter': true // Boolean | Filter out low-quality results (junk TLDs and unreachable websites)
};
apiInstance.getCustomerListing(website, opts, (error, data, response) => {
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
 **website** | **String**| The website URL of the target company | 
 **cursor** | **String**| Pagination cursor from &#x60;next_page&#x60; in a previous response | [optional] 
 **pageSize** | **Number**| Number of results per page (1-200, default 200) | [optional] [default to 200]
 **qualityFilter** | **Boolean**| Filter out low-quality results (junk TLDs and unreachable websites) | [optional] [default to true]

### Return type

[**CustomerListingResponse**](CustomerListingResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

