# Ninjapear.Feed

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Unique feed identifier | [optional] 
**name** | **String** | Feed display name | [optional] 
**isPublic** | **Boolean** | Whether the RSS feed is publicly accessible without a token | [optional] 
**isSuspended** | **Boolean** | Whether the feed is currently suspended (e.g. due to insufficient credits) | [optional] 
**suspensionReason** | **String** | Reason for suspension, if suspended | [optional] 
**rssUrl** | **String** | URL to the RSS feed. Includes a token query parameter for private feeds. | [optional] 
**createdAt** | **Date** | When the feed was created | [optional] 
**targets** | [**[Target]**](Target.md) | List of monitored targets in this feed | [optional] 



## Enum: SuspensionReasonEnum


* `insufficient_credits` (value: `"insufficient_credits"`)

* `manual` (value: `"manual"`)




