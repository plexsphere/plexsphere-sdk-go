# ExecutionCallbackRequestOutput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Inline** | Pointer to **string** | Base64-encoded inline output bytes (≤ 16 KiB). An inline body over the ceiling is refused with 413.  | [optional] 
**ObjectKey** | Pointer to **string** | Object-store key of the uploaded over-ceiling output, set on the final callback after the Node has uploaded the body to the presigned URL.  | [optional] 
**Sha256** | Pointer to **string** | Hex-encoded SHA-256 digest of the uploaded over-ceiling output.  | [optional] 

## Methods

### NewExecutionCallbackRequestOutput

`func NewExecutionCallbackRequestOutput() *ExecutionCallbackRequestOutput`

NewExecutionCallbackRequestOutput instantiates a new ExecutionCallbackRequestOutput object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewExecutionCallbackRequestOutputWithDefaults

`func NewExecutionCallbackRequestOutputWithDefaults() *ExecutionCallbackRequestOutput`

NewExecutionCallbackRequestOutputWithDefaults instantiates a new ExecutionCallbackRequestOutput object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetInline

`func (o *ExecutionCallbackRequestOutput) GetInline() string`

GetInline returns the Inline field if non-nil, zero value otherwise.

### GetInlineOk

`func (o *ExecutionCallbackRequestOutput) GetInlineOk() (*string, bool)`

GetInlineOk returns a tuple with the Inline field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetInline

`func (o *ExecutionCallbackRequestOutput) SetInline(v string)`

SetInline sets Inline field to given value.

### HasInline

`func (o *ExecutionCallbackRequestOutput) HasInline() bool`

HasInline returns a boolean if a field has been set.

### GetObjectKey

`func (o *ExecutionCallbackRequestOutput) GetObjectKey() string`

GetObjectKey returns the ObjectKey field if non-nil, zero value otherwise.

### GetObjectKeyOk

`func (o *ExecutionCallbackRequestOutput) GetObjectKeyOk() (*string, bool)`

GetObjectKeyOk returns a tuple with the ObjectKey field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetObjectKey

`func (o *ExecutionCallbackRequestOutput) SetObjectKey(v string)`

SetObjectKey sets ObjectKey field to given value.

### HasObjectKey

`func (o *ExecutionCallbackRequestOutput) HasObjectKey() bool`

HasObjectKey returns a boolean if a field has been set.

### GetSha256

`func (o *ExecutionCallbackRequestOutput) GetSha256() string`

GetSha256 returns the Sha256 field if non-nil, zero value otherwise.

### GetSha256Ok

`func (o *ExecutionCallbackRequestOutput) GetSha256Ok() (*string, bool)`

GetSha256Ok returns a tuple with the Sha256 field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSha256

`func (o *ExecutionCallbackRequestOutput) SetSha256(v string)`

SetSha256 sets Sha256 field to given value.

### HasSha256

`func (o *ExecutionCallbackRequestOutput) HasSha256() bool`

HasSha256 returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


