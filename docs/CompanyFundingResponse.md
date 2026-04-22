# Ninjapear.CompanyFundingResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**website** | **String** | The company domain the response describes, echoed from the request. | [optional] 
**totalFundsRaisedUsd** | **Number** | Total funds raised across all rounds in USD | [optional] 
**fundingRounds** | [**[FundingRound]**](FundingRound.md) | List of funding rounds. Empty array on fresh-path failures (see &#x60;error_code&#x60;). | [optional] 
**creditCost** | **Number** | Total credits charged for this call (2 base + 1 per unique investor). Delivered in the response body rather than the &#x60;X-NinjaPear-Credit-Cost&#x60; header on cache misses, because streaming responses cannot set HTTP trailers. | [optional] 
**error** | **String** | Error message when funding data could not be extracted. Only present alongside &#x60;error_code&#x60;. | [optional] 
**errorCode** | **String** | Present only on fresh-path failures (HTTP 200, streaming). Clients that previously branched on &#x60;status_code &#x3D;&#x3D; 404&#x60; should branch on this field. &#x60;no_funding_data&#x60; still charges the 2-credit base; &#x60;service_temp_unavailable&#x60; is not charged. | [optional] 



## Enum: ErrorCodeEnum


* `no_funding_data` (value: `"no_funding_data"`)

* `service_temp_unavailable` (value: `"service_temp_unavailable"`)




