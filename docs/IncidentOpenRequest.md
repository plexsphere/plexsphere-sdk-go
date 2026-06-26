# IncidentOpenRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Title** | **string** | Short human-readable title of the incident. | 
**Severity** | [**IncidentSeverity**](IncidentSeverity.md) |  | 

## Methods

### NewIncidentOpenRequest

`func NewIncidentOpenRequest(title string, severity IncidentSeverity, ) *IncidentOpenRequest`

NewIncidentOpenRequest instantiates a new IncidentOpenRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewIncidentOpenRequestWithDefaults

`func NewIncidentOpenRequestWithDefaults() *IncidentOpenRequest`

NewIncidentOpenRequestWithDefaults instantiates a new IncidentOpenRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetTitle

`func (o *IncidentOpenRequest) GetTitle() string`

GetTitle returns the Title field if non-nil, zero value otherwise.

### GetTitleOk

`func (o *IncidentOpenRequest) GetTitleOk() (*string, bool)`

GetTitleOk returns a tuple with the Title field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTitle

`func (o *IncidentOpenRequest) SetTitle(v string)`

SetTitle sets Title field to given value.


### GetSeverity

`func (o *IncidentOpenRequest) GetSeverity() IncidentSeverity`

GetSeverity returns the Severity field if non-nil, zero value otherwise.

### GetSeverityOk

`func (o *IncidentOpenRequest) GetSeverityOk() (*IncidentSeverity, bool)`

GetSeverityOk returns a tuple with the Severity field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSeverity

`func (o *IncidentOpenRequest) SetSeverity(v IncidentSeverity)`

SetSeverity sets Severity field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


