# Ninjapear.CompanyDetailsResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**websites** | **[String]** | List of all company website URLs | [optional] 
**description** | **String** | A brief description of the company | [optional] 
**industry** | **Number** | GICS 8-digit industry code | [optional] 
**companyType** | **String** | Type of company | [optional] 
**foundedYear** | **Number** | Year the company was founded | [optional] 
**specialties** | **[String]** | List of company specialties | [optional] 
**name** | **String** | Company name | [optional] 
**tagline** | **String** | Company tagline or slogan | [optional] 
**logoUrl** | **String** | URL to the company logo endpoint | [optional] 
**coverPicUrl** | **String** | URL to the company&#39;s cover/banner image | [optional] 
**facebookUrl** | **String** | Facebook profile URL | [optional] 
**twitterUrl** | **String** | Twitter/X profile URL | [optional] 
**instagramUrl** | **String** | Instagram profile URL | [optional] 
**employeeCount** | **Number** | Estimated number of employees | [optional] 
**employeeCountRangeMin** | **Number** | Lower bound of employee count range (only with include_employee_count&#x3D;true) | [optional] 
**employeeCountRangeMax** | **Number** | Upper bound of employee count range (only with include_employee_count&#x3D;true) | [optional] 
**addresses** | [**[Address]**](Address.md) | List of company addresses | [optional] 
**executives** | [**[Executive]**](Executive.md) | List of company executives and board members | [optional] 
**publicListing** | [**PublicListing**](PublicListing.md) | Public company data. Null for private companies. | [optional] 



## Enum: CompanyTypeEnum


* `PUBLIC_COMPANY` (value: `"PUBLIC_COMPANY"`)

* `PRIVATELY_HELD` (value: `"PRIVATELY_HELD"`)

* `GOVERNMENT_AGENCY` (value: `"GOVERNMENT_AGENCY"`)

* `NON_PROFIT` (value: `"NON_PROFIT"`)

* `EDUCATIONAL` (value: `"EDUCATIONAL"`)

* `PARTNERSHIP` (value: `"PARTNERSHIP"`)

* `SELF_EMPLOYED` (value: `"SELF_EMPLOYED"`)

* `SELF_OWNED` (value: `"SELF_OWNED"`)




