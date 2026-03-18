# Ninjapear.CompanyAPIApi

All URIs are relative to *https://nubela.co*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getCompanyDetails**](CompanyAPIApi.md#getCompanyDetails) | **GET** /api/v1/company/details | Company Details
[**getCompanyFunding**](CompanyAPIApi.md#getCompanyFunding) | **GET** /api/v1/company/funding | Company Funding
[**getCompanyLogo**](CompanyAPIApi.md#getCompanyLogo) | **GET** /api/v1/company/logo | Company Logo
[**getCompanyUpdates**](CompanyAPIApi.md#getCompanyUpdates) | **GET** /api/v1/company/updates | Company Updates
[**getEmployeeCount**](CompanyAPIApi.md#getEmployeeCount) | **GET** /api/v1/company/employee-count | Employee Count



## getCompanyDetails

> CompanyDetailsResponse getCompanyDetails(website, opts)

Company Details

Retrieve detailed company information including description, industry, executives, addresses, and for public companies: financials and stock info.  **Cost:** 2 credits (4 credits if include_employee_count&#x3D;true, +1 credit if follower_count&#x3D;include)

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
  'includeEmployeeCount': false, // Boolean | Fetch fresh employee count data via web search. Adds 2 credits.
  'followerCount': "followerCount_example" // String | Set to 'include' to fetch Twitter/X follower and following counts. Adds 1 credit.
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
 **followerCount** | **String**| Set to &#39;include&#39; to fetch Twitter/X follower and following counts. Adds 1 credit. | [optional] 

### Return type

[**CompanyDetailsResponse**](CompanyDetailsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getCompanyFunding

> CompanyFundingResponse getCompanyFunding(website)

Company Funding

Retrieve the funding history of a company including all funding rounds and investors.  **Cost:** 2 credits + 1 credit per unique investor returned

### Example

```javascript
import Ninjapear from 'ninjapear';
let defaultClient = Ninjapear.ApiClient.instance;
// Configure Bearer access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new Ninjapear.CompanyAPIApi();
let website = "https://www.stripe.com"; // String | The website URL of the target company
apiInstance.getCompanyFunding(website, (error, data, response) => {
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

[**CompanyFundingResponse**](CompanyFundingResponse.md)

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


## getCompanyUpdates

> CompanyUpdatesResponse getCompanyUpdates(website)

Company Updates

Retrieve recent blog posts and X/Twitter updates for a company.  **Cost:** 2 credits

### Example

```javascript
import Ninjapear from 'ninjapear';
let defaultClient = Ninjapear.ApiClient.instance;
// Configure Bearer access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new Ninjapear.CompanyAPIApi();
let website = "https://www.stripe.com"; // String | The website URL of the target company
apiInstance.getCompanyUpdates(website, (error, data, response) => {
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

[**CompanyUpdatesResponse**](CompanyUpdatesResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


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

