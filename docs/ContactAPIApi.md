# NinjaPear.ContactAPIApi

All URIs are relative to *https://nubela.co*

Method | HTTP request | Description
------------- | ------------- | -------------
[**checkDisposableEmail**](ContactAPIApi.md#checkDisposableEmail) | **GET** /api/v1/contact/disposable-email | Disposable Email Checker



## checkDisposableEmail

> DisposableEmailResponse checkDisposableEmail(email)

Disposable Email Checker

Check if an email address is a disposable (temporary/throwaway) email or a free email provider.  **Cost:** FREE (0 credits)

### Example

```javascript
import NinjaPear from 'ninjapear';
let defaultClient = NinjaPear.ApiClient.instance;
// Configure Bearer access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new NinjaPear.ContactAPIApi();
let email = "test@mailinator.com"; // String | The email address to check
apiInstance.checkDisposableEmail(email).then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email** | **String**| The email address to check | 

### Return type

[**DisposableEmailResponse**](DisposableEmailResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

