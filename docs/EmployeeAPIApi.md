# Ninjapear.EmployeeAPIApi

All URIs are relative to *https://nubela.co*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getPersonProfile**](EmployeeAPIApi.md#getPersonProfile) | **GET** /api/v1/employee/profile | Person Profile Enrichment
[**getWorkEmail**](EmployeeAPIApi.md#getWorkEmail) | **GET** /api/v1/employee/work-email | Work Email Lookup



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
  'employerWebsite': "https://stripe.com", // String | Employer's website URL or company name. A website URL (e.g. `https://stripe.com`) is strongly recommended for precision.
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
 **employerWebsite** | **String**| Employer&#39;s website URL or company name. A website URL (e.g. &#x60;https://stripe.com&#x60;) is strongly recommended for precision. | [optional] 
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


## getWorkEmail

> WorkEmailResponse getWorkEmail(firstName, domain, opts)

Work Email Lookup

Makes a best-effort attempt to return a person&#39;s public work email address given their first name (optional last name) and a company domain. Searches public sources for the specific email first; if none is found, infers the address from observed employee email patterns at the domain. Returns &#x60;work_email: null&#x60; if no evidence is available.  **Cost:** 2 credits per API call, charged regardless of whether an email is returned.

### Example

```javascript
import Ninjapear from 'ninjapear';
let defaultClient = Ninjapear.ApiClient.instance;
// Configure Bearer access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new Ninjapear.EmployeeAPIApi();
let firstName = "Patrick"; // String | Person's first name
let domain = "stripe.com"; // String | Company domain. Scheme, www, and trailing slash are stripped if present.
let opts = {
  'lastName': "Collison", // String | Person's last name. Improves accuracy when the email pattern needs it.
  'forceRefresh': true // Boolean | If `true`, bypass the cache and re-run the AI lookup.
};
apiInstance.getWorkEmail(firstName, domain, opts, (error, data, response) => {
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
 **firstName** | **String**| Person&#39;s first name | 
 **domain** | **String**| Company domain. Scheme, www, and trailing slash are stripped if present. | 
 **lastName** | **String**| Person&#39;s last name. Improves accuracy when the email pattern needs it. | [optional] 
 **forceRefresh** | **Boolean**| If &#x60;true&#x60;, bypass the cache and re-run the AI lookup. | [optional] 

### Return type

[**WorkEmailResponse**](WorkEmailResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

