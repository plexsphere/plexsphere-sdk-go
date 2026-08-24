# SinkEnablementRequestBody

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**SinkId** | **string** | Identifier of the sink to enable. Must be a non-zero UUID naming a tenant sink of the Project&#39;s own Domain.  | 

## Methods

### NewSinkEnablementRequestBody

`func NewSinkEnablementRequestBody(sinkId string, ) *SinkEnablementRequestBody`

NewSinkEnablementRequestBody instantiates a new SinkEnablementRequestBody object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSinkEnablementRequestBodyWithDefaults

`func NewSinkEnablementRequestBodyWithDefaults() *SinkEnablementRequestBody`

NewSinkEnablementRequestBodyWithDefaults instantiates a new SinkEnablementRequestBody object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSinkId

`func (o *SinkEnablementRequestBody) GetSinkId() string`

GetSinkId returns the SinkId field if non-nil, zero value otherwise.

### GetSinkIdOk

`func (o *SinkEnablementRequestBody) GetSinkIdOk() (*string, bool)`

GetSinkIdOk returns a tuple with the SinkId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSinkId

`func (o *SinkEnablementRequestBody) SetSinkId(v string)`

SetSinkId sets SinkId field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


