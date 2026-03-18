# Ninjapear.EmployeeAPIApi

All URIs are relative to *https://nubela.co*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getPersonProfile**](EmployeeAPIApi.md#getPersonProfile) | **GET** /api/v1/employee/profile | Person Profile Enrichment



## getPersonProfile

> PersonProfileResponse getPersonProfile(opts)

Person Profile Enrichment

Enrich a person&#39;s professional profile including work experience, education, and social media presence. Provide at least one of the following combinations: - &#x60;work_email&#x60; - &#x60;first_name&#x60; + &#x60;employer_website&#x60; - &#x60;employer_website&#x60; + &#x60;role&#x60; - &#x60;slug&#x60; or &#x60;id&#x60; for direct lookup  **Cost:** 3 credits

### Example

```javascript
import Ninjapear from 'ninjapear';
let defaultClient = Ninjapear.ApiClient.instance;
// Configure Bearer access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new Ninjapear.EmployeeAPIApi();
let opts = {
  'workEmail': "john@stripe.com", // String | Person's work email address
  'firstName': "firstName_example", // String | Person's first name
  'middleName': "middleName_example", // String | Person's middle name
  'lastName': "lastName_example", // String | Person's last name
  'employerWebsite': "https://stripe.com", // String | Employer's website URL
  'role': "CEO", // String | Job role/title
  'slug': "slug_example", // String | Person's unique slug identifier (direct lookup)
  'id': "id_example" // String | Person's unique ID (direct lookup)
};
apiInstance.getPersonProfile(opts, (error, data, response) => {
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
 **workEmail** | **String**| Person&#39;s work email address | [optional] 
 **firstName** | **String**| Person&#39;s first name | [optional] 
 **middleName** | **String**| Person&#39;s middle name | [optional] 
 **lastName** | **String**| Person&#39;s last name | [optional] 
 **employerWebsite** | **String**| Employer&#39;s website URL | [optional] 
 **role** | **String**| Job role/title | [optional] 
 **slug** | **String**| Person&#39;s unique slug identifier (direct lookup) | [optional] 
 **id** | **String**| Person&#39;s unique ID (direct lookup) | [optional] 

### Return type

[**PersonProfileResponse**](PersonProfileResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

