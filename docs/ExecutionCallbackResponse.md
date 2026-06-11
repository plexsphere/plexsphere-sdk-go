# ExecutionCallbackResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Status** | [**ExecutionStatus**](ExecutionStatus.md) |  | 
**OutputUploadUrl** | Pointer to **string** | Presigned object-store PUT URL the Node uploads its over- ceiling output to. Present ONLY on the first callback that declares an over-ceiling output; omitted on every other callback.  | [optional] 

## Methods

### NewExecutionCallbackResponse

`func NewExecutionCallbackResponse(status ExecutionStatus, ) *ExecutionCallbackResponse`

NewExecutionCallbackResponse instantiates a new ExecutionCallbackResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewExecutionCallbackResponseWithDefaults

`func NewExecutionCallbackResponseWithDefaults() *ExecutionCallbackResponse`

NewExecutionCallbackResponseWithDefaults instantiates a new ExecutionCallbackResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetStatus

`func (o *ExecutionCallbackResponse) GetStatus() ExecutionStatus`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *ExecutionCallbackResponse) GetStatusOk() (*ExecutionStatus, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *ExecutionCallbackResponse) SetStatus(v ExecutionStatus)`

SetStatus sets Status field to given value.


### GetOutputUploadUrl

`func (o *ExecutionCallbackResponse) GetOutputUploadUrl() string`

GetOutputUploadUrl returns the OutputUploadUrl field if non-nil, zero value otherwise.

### GetOutputUploadUrlOk

`func (o *ExecutionCallbackResponse) GetOutputUploadUrlOk() (*string, bool)`

GetOutputUploadUrlOk returns a tuple with the OutputUploadUrl field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOutputUploadUrl

`func (o *ExecutionCallbackResponse) SetOutputUploadUrl(v string)`

SetOutputUploadUrl sets OutputUploadUrl field to given value.

### HasOutputUploadUrl

`func (o *ExecutionCallbackResponse) HasOutputUploadUrl() bool`

HasOutputUploadUrl returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


