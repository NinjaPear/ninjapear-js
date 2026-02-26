# Ninjapear.UpdatesAPIApi

All URIs are relative to *https://nubela.co*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addTarget**](UpdatesAPIApi.md#addTarget) | **POST** /api/v1/feeds/{feed_id}/targets | Add Target
[**createFeed**](UpdatesAPIApi.md#createFeed) | **POST** /api/v1/feeds | Create Feed
[**deleteFeed**](UpdatesAPIApi.md#deleteFeed) | **DELETE** /api/v1/feeds/{feed_id} | Delete Feed
[**deleteTarget**](UpdatesAPIApi.md#deleteTarget) | **DELETE** /api/v1/feeds/{feed_id}/targets/{target_id} | Delete Target
[**getFeed**](UpdatesAPIApi.md#getFeed) | **GET** /api/v1/feeds/{feed_id} | Get Feed
[**getRssFeed**](UpdatesAPIApi.md#getRssFeed) | **GET** /api/v1/feeds/{feed_id}/rss.xml | Get RSS Feed
[**listFeeds**](UpdatesAPIApi.md#listFeeds) | **GET** /api/v1/feeds | List Feeds
[**updateFeed**](UpdatesAPIApi.md#updateFeed) | **PATCH** /api/v1/feeds/{feed_id} | Update Feed
[**updateTarget**](UpdatesAPIApi.md#updateTarget) | **PATCH** /api/v1/feeds/{feed_id}/targets/{target_id} | Update Target



## addTarget

> Target addTarget(feedId, addTargetRequest)

Add Target

Add a new company target to an existing feed.  **Cost:** FREE (0 credits)

### Example

```javascript
import Ninjapear from 'ninjapear';
let defaultClient = Ninjapear.ApiClient.instance;
// Configure Bearer access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new Ninjapear.UpdatesAPIApi();
let feedId = "feedId_example"; // String | Feed identifier (e.g. feed_abc123xyz)
let addTargetRequest = new Ninjapear.AddTargetRequest(); // AddTargetRequest | 
apiInstance.addTarget(feedId, addTargetRequest, (error, data, response) => {
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
 **feedId** | **String**| Feed identifier (e.g. feed_abc123xyz) | 
 **addTargetRequest** | [**AddTargetRequest**](AddTargetRequest.md)|  | 

### Return type

[**Target**](Target.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## createFeed

> Feed createFeed(createFeedRequest)

Create Feed

Create a new monitoring feed with one or more company targets. Each target specifies a company website and which channels to monitor (blog, X/Twitter, website changes).  **Cost:** 3 credits

### Example

```javascript
import Ninjapear from 'ninjapear';
let defaultClient = Ninjapear.ApiClient.instance;
// Configure Bearer access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new Ninjapear.UpdatesAPIApi();
let createFeedRequest = new Ninjapear.CreateFeedRequest(); // CreateFeedRequest | 
apiInstance.createFeed(createFeedRequest, (error, data, response) => {
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
 **createFeedRequest** | [**CreateFeedRequest**](CreateFeedRequest.md)|  | 

### Return type

[**Feed**](Feed.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## deleteFeed

> MessageResponse deleteFeed(feedId)

Delete Feed

Soft-delete a feed and all its targets.  **Cost:** FREE (0 credits)

### Example

```javascript
import Ninjapear from 'ninjapear';
let defaultClient = Ninjapear.ApiClient.instance;
// Configure Bearer access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new Ninjapear.UpdatesAPIApi();
let feedId = "feedId_example"; // String | Feed identifier (e.g. feed_abc123xyz)
apiInstance.deleteFeed(feedId, (error, data, response) => {
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
 **feedId** | **String**| Feed identifier (e.g. feed_abc123xyz) | 

### Return type

[**MessageResponse**](MessageResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## deleteTarget

> MessageResponse deleteTarget(feedId, targetId)

Delete Target

Soft-delete a target from a feed.  **Cost:** FREE (0 credits)

### Example

```javascript
import Ninjapear from 'ninjapear';
let defaultClient = Ninjapear.ApiClient.instance;
// Configure Bearer access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new Ninjapear.UpdatesAPIApi();
let feedId = "feedId_example"; // String | Feed identifier (e.g. feed_abc123xyz)
let targetId = "targetId_example"; // String | Target identifier (e.g. target_abc123xyz)
apiInstance.deleteTarget(feedId, targetId, (error, data, response) => {
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
 **feedId** | **String**| Feed identifier (e.g. feed_abc123xyz) | 
 **targetId** | **String**| Target identifier (e.g. target_abc123xyz) | 

### Return type

[**MessageResponse**](MessageResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getFeed

> Feed getFeed(feedId)

Get Feed

Get a feed with all its targets.  **Cost:** FREE (0 credits)

### Example

```javascript
import Ninjapear from 'ninjapear';
let defaultClient = Ninjapear.ApiClient.instance;
// Configure Bearer access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new Ninjapear.UpdatesAPIApi();
let feedId = "feedId_example"; // String | Feed identifier (e.g. feed_abc123xyz)
apiInstance.getFeed(feedId, (error, data, response) => {
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
 **feedId** | **String**| Feed identifier (e.g. feed_abc123xyz) | 

### Return type

[**Feed**](Feed.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## getRssFeed

> String getRssFeed(feedId, opts)

Get RSS Feed

Get the RSS 2.0 XML feed for a monitoring feed. Public feeds are accessible without authentication. Private feeds require the &#x60;token&#x60; query parameter.  **Cost:** FREE (0 credits)  **Authentication:** This endpoint does NOT use Bearer authentication. Private feeds are authenticated via the &#x60;token&#x60; query parameter, which is included in the &#x60;rss_url&#x60; returned when creating a feed.

### Example

```javascript
import Ninjapear from 'ninjapear';

let apiInstance = new Ninjapear.UpdatesAPIApi();
let feedId = "feedId_example"; // String | Feed identifier (e.g. feed_abc123xyz)
let opts = {
  'token': "token_example" // String | Access token for private feeds (included in rss_url)
};
apiInstance.getRssFeed(feedId, opts, (error, data, response) => {
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
 **feedId** | **String**| Feed identifier (e.g. feed_abc123xyz) | 
 **token** | **String**| Access token for private feeds (included in rss_url) | [optional] 

### Return type

**String**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/xml, application/json


## listFeeds

> FeedListResponse listFeeds()

List Feeds

List all feeds for the authenticated account.  **Cost:** FREE (0 credits)

### Example

```javascript
import Ninjapear from 'ninjapear';
let defaultClient = Ninjapear.ApiClient.instance;
// Configure Bearer access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new Ninjapear.UpdatesAPIApi();
apiInstance.listFeeds((error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**FeedListResponse**](FeedListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## updateFeed

> Feed updateFeed(feedId, updateFeedRequest)

Update Feed

Update feed metadata such as name, visibility, or suspension status.  **Cost:** FREE (0 credits)

### Example

```javascript
import Ninjapear from 'ninjapear';
let defaultClient = Ninjapear.ApiClient.instance;
// Configure Bearer access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new Ninjapear.UpdatesAPIApi();
let feedId = "feedId_example"; // String | Feed identifier (e.g. feed_abc123xyz)
let updateFeedRequest = new Ninjapear.UpdateFeedRequest(); // UpdateFeedRequest | 
apiInstance.updateFeed(feedId, updateFeedRequest, (error, data, response) => {
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
 **feedId** | **String**| Feed identifier (e.g. feed_abc123xyz) | 
 **updateFeedRequest** | [**UpdateFeedRequest**](UpdateFeedRequest.md)|  | 

### Return type

[**Feed**](Feed.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## updateTarget

> Target updateTarget(feedId, targetId, updateTargetRequest)

Update Target

Update monitoring settings for a target.  **Cost:** FREE (0 credits)

### Example

```javascript
import Ninjapear from 'ninjapear';
let defaultClient = Ninjapear.ApiClient.instance;
// Configure Bearer access token for authorization: bearerAuth
let bearerAuth = defaultClient.authentications['bearerAuth'];
bearerAuth.accessToken = "YOUR ACCESS TOKEN"

let apiInstance = new Ninjapear.UpdatesAPIApi();
let feedId = "feedId_example"; // String | Feed identifier (e.g. feed_abc123xyz)
let targetId = "targetId_example"; // String | Target identifier (e.g. target_abc123xyz)
let updateTargetRequest = new Ninjapear.UpdateTargetRequest(); // UpdateTargetRequest | 
apiInstance.updateTarget(feedId, targetId, updateTargetRequest, (error, data, response) => {
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
 **feedId** | **String**| Feed identifier (e.g. feed_abc123xyz) | 
 **targetId** | **String**| Target identifier (e.g. target_abc123xyz) | 
 **updateTargetRequest** | [**UpdateTargetRequest**](UpdateTargetRequest.md)|  | 

### Return type

[**Target**](Target.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

