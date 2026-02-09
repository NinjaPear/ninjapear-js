# NinjaPear.CompanyAPIApi

All URIs are relative to *https://nubela.co*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getCompanyLogo**](CompanyAPIApi.md#getCompanyLogo) | **GET** /api/v1/company/logo | Company Logo



## getCompanyLogo

> File getCompanyLogo(website)

Company Logo

Retrieve the logo of a company given its website URL. Returns the logo as a PNG image (128x128).  **Cost:** FREE (0 credits)

### Example

```javascript
import NinjaPear from 'ninjapear';
let defaultClient = NinjaPear.ApiClient.instance;
// Configure Bearer access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new NinjaPear.CompanyAPIApi();
let website = "https://www.stripe.com"; // String | The website URL of the target company
apiInstance.getCompanyLogo(website).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
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

