# SinkEnablementGrantBody

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProjectId** | **string** | Identifier of the Project to enable the sink in. Must be a non-zero UUID naming a Project of the sink&#39;s own Domain.  | 

## Methods

### NewSinkEnablementGrantBody

`func NewSinkEnablementGrantBody(projectId string, ) *SinkEnablementGrantBody`

NewSinkEnablementGrantBody instantiates a new SinkEnablementGrantBody object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSinkEnablementGrantBodyWithDefaults

`func NewSinkEnablementGrantBodyWithDefaults() *SinkEnablementGrantBody`

NewSinkEnablementGrantBodyWithDefaults instantiates a new SinkEnablementGrantBody object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetProjectId

`func (o *SinkEnablementGrantBody) GetProjectId() string`

GetProjectId returns the ProjectId field if non-nil, zero value otherwise.

### GetProjectIdOk

`func (o *SinkEnablementGrantBody) GetProjectIdOk() (*string, bool)`

GetProjectIdOk returns a tuple with the ProjectId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProjectId

`func (o *SinkEnablementGrantBody) SetProjectId(v string)`

SetProjectId sets ProjectId field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


