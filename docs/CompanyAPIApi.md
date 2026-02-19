# Ninjapear.CompanyAPIApi

All URIs are relative to *https://nubela.co*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getCompanyDetails**](CompanyAPIApi.md#getCompanyDetails) | **GET** /api/v1/company/details | Company Details
[**getCompanyLogo**](CompanyAPIApi.md#getCompanyLogo) | **GET** /api/v1/company/logo | Company Logo
[**getEmployeeCount**](CompanyAPIApi.md#getEmployeeCount) | **GET** /api/v1/company/employee-count | Employee Count



## getCompanyDetails

> CompanyDetailsResponse getCompanyDetails(website, opts)

Company Details

Retrieve detailed company information including description, industry, executives, addresses, and for public companies: financials and stock info.  **Cost:** 2 credits (4 credits if include_employee_count&#x3D;true)

### Example

```javascript
import Ninjapear from 'ninjapear';
let defaultClient = Ninjapear.ApiClient.instance;
// Configure Bearer access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new Ninjapear.CompanyAPIApi();
let website = "https://www.stripe.com"; // String | The website URL of the target company
let opts = {
  'includeEmployeeCount': false // Boolean | Fetch fresh employee count data via web search. Adds 2 credits.
};
apiInstance.getCompanyDetails(website, opts, (error, data, response) => {
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
 **includeEmployeeCount** | **Boolean**| Fetch fresh employee count data via web search. Adds 2 credits. | [optional] [default to false]

### Return type

[**CompanyDetailsResponse**](CompanyDetailsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getCompanyLogo

> File getCompanyLogo(website)

Company Logo

Retrieve the logo of a company given its website URL. Returns the logo as a PNG image (128x128).  **Cost:** FREE (0 credits)

### Example

```javascript
import Ninjapear from 'ninjapear';
let defaultClient = Ninjapear.ApiClient.instance;
// Configure Bearer access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new Ninjapear.CompanyAPIApi();
let website = "https://www.stripe.com"; // String | The website URL of the target company
apiInstance.getCompanyLogo(website, (error, data, response) => {
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

### Return type

**File**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: image/png, application/json


## getEmployeeCount

> EmployeeCountResponse getEmployeeCount(website)

Employee Count

Get the employee count for a company. Uses web search to find the most recent employee count information.  **Cost:** 2 credits

### Example

```javascript
import Ninjapear from 'ninjapear';
let defaultClient = Ninjapear.ApiClient.instance;
// Configure Bearer access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new Ninjapear.CompanyAPIApi();
let website = "https://www.stripe.com"; // String | The website URL of the target company
apiInstance.getEmployeeCount(website, (error, data, response) => {
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

### Return type

[**EmployeeCountResponse**](EmployeeCountResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

