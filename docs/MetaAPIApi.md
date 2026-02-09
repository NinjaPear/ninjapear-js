# NinjaPear.MetaAPIApi

All URIs are relative to *https://nubela.co*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getCreditBalance**](MetaAPIApi.md#getCreditBalance) | **GET** /api/v1/meta/credit-balance | View Credit Balance



## getCreditBalance

> CreditBalanceResponse getCreditBalance()

View Credit Balance

Get your current credit balance.  **Cost:** FREE (0 credits)

### Example

```javascript
import NinjaPear from 'ninjapear';
let defaultClient = NinjaPear.ApiClient.instance;
// Configure Bearer access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new NinjaPear.MetaAPIApi();
apiInstance.getCreditBalance().then((data) => {
  console.log('API called successfully. Returned data: ' + data);
}, (error) => {
  console.error(error);
});

```

### Parameters

This endpoint does not need any parameter.

### Return type

[**CreditBalanceResponse**](CreditBalanceResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

