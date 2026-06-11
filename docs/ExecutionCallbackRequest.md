# ExecutionCallbackRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Status** | [**ExecutionStatus**](ExecutionStatus.md) |  | 
**ExitCode** | Pointer to **int32** | Process exit code the action reported. Present on terminal callbacks that ran the action to completion.  | [optional] 
**Error** | Pointer to **string** | Free-text error the action reported. Present on a &#x60;failed&#x60; terminal callback.  | [optional] 
**DeclaredOutputBytes** | Pointer to **int32** | Size in bytes the Node declares it intends to upload. A value over the 16 KiB ceiling drives the over-ceiling presign mint on the first callback.  | [optional] 
**Output** | Pointer to [**ExecutionCallbackRequestOutput**](ExecutionCallbackRequestOutput.md) |  | [optional] 

## Methods

### NewExecutionCallbackRequest

`func NewExecutionCallbackRequest(status ExecutionStatus, ) *ExecutionCallbackRequest`

NewExecutionCallbackRequest instantiates a new ExecutionCallbackRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewExecutionCallbackRequestWithDefaults

`func NewExecutionCallbackRequestWithDefaults() *ExecutionCallbackRequest`

NewExecutionCallbackRequestWithDefaults instantiates a new ExecutionCallbackRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetStatus

`func (o *ExecutionCallbackRequest) GetStatus() ExecutionStatus`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *ExecutionCallbackRequest) GetStatusOk() (*ExecutionStatus, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *ExecutionCallbackRequest) SetStatus(v ExecutionStatus)`

SetStatus sets Status field to given value.


### GetExitCode

`func (o *ExecutionCallbackRequest) GetExitCode() int32`

GetExitCode returns the ExitCode field if non-nil, zero value otherwise.

### GetExitCodeOk

`func (o *ExecutionCallbackRequest) GetExitCodeOk() (*int32, bool)`

GetExitCodeOk returns a tuple with the ExitCode field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExitCode

`func (o *ExecutionCallbackRequest) SetExitCode(v int32)`

SetExitCode sets ExitCode field to given value.

### HasExitCode

`func (o *ExecutionCallbackRequest) HasExitCode() bool`

HasExitCode returns a boolean if a field has been set.

### GetError

`func (o *ExecutionCallbackRequest) GetError() string`

GetError returns the Error field if non-nil, zero value otherwise.

### GetErrorOk

`func (o *ExecutionCallbackRequest) GetErrorOk() (*string, bool)`

GetErrorOk returns a tuple with the Error field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetError

`func (o *ExecutionCallbackRequest) SetError(v string)`

SetError sets Error field to given value.

### HasError

`func (o *ExecutionCallbackRequest) HasError() bool`

HasError returns a boolean if a field has been set.

### GetDeclaredOutputBytes

`func (o *ExecutionCallbackRequest) GetDeclaredOutputBytes() int32`

GetDeclaredOutputBytes returns the DeclaredOutputBytes field if non-nil, zero value otherwise.

### GetDeclaredOutputBytesOk

`func (o *ExecutionCallbackRequest) GetDeclaredOutputBytesOk() (*int32, bool)`

GetDeclaredOutputBytesOk returns a tuple with the DeclaredOutputBytes field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDeclaredOutputBytes

`func (o *ExecutionCallbackRequest) SetDeclaredOutputBytes(v int32)`

SetDeclaredOutputBytes sets DeclaredOutputBytes field to given value.

### HasDeclaredOutputBytes

`func (o *ExecutionCallbackRequest) HasDeclaredOutputBytes() bool`

HasDeclaredOutputBytes returns a boolean if a field has been set.

### GetOutput

`func (o *ExecutionCallbackRequest) GetOutput() ExecutionCallbackRequestOutput`

GetOutput returns the Output field if non-nil, zero value otherwise.

### GetOutputOk

`func (o *ExecutionCallbackRequest) GetOutputOk() (*ExecutionCallbackRequestOutput, bool)`

GetOutputOk returns a tuple with the Output field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOutput

`func (o *ExecutionCallbackRequest) SetOutput(v ExecutionCallbackRequestOutput)`

SetOutput sets Output field to given value.

### HasOutput

`func (o *ExecutionCallbackRequest) HasOutput() bool`

HasOutput returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


