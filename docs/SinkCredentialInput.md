# SinkCredentialInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**KvMount** | **string** | KV mount the material lives under. Free of surrounding whitespace and of any &#x60;..&#x60; traversal segment.  | 
**KvVersion** | Pointer to **int64** | KV version to read. Absent or &#x60;0&#x60; reads the latest one.  | [optional] 

## Methods

### NewSinkCredentialInput

`func NewSinkCredentialInput(kvMount string, ) *SinkCredentialInput`

NewSinkCredentialInput instantiates a new SinkCredentialInput object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSinkCredentialInputWithDefaults

`func NewSinkCredentialInputWithDefaults() *SinkCredentialInput`

NewSinkCredentialInputWithDefaults instantiates a new SinkCredentialInput object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetKvMount

`func (o *SinkCredentialInput) GetKvMount() string`

GetKvMount returns the KvMount field if non-nil, zero value otherwise.

### GetKvMountOk

`func (o *SinkCredentialInput) GetKvMountOk() (*string, bool)`

GetKvMountOk returns a tuple with the KvMount field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKvMount

`func (o *SinkCredentialInput) SetKvMount(v string)`

SetKvMount sets KvMount field to given value.


### GetKvVersion

`func (o *SinkCredentialInput) GetKvVersion() int64`

GetKvVersion returns the KvVersion field if non-nil, zero value otherwise.

### GetKvVersionOk

`func (o *SinkCredentialInput) GetKvVersionOk() (*int64, bool)`

GetKvVersionOk returns a tuple with the KvVersion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKvVersion

`func (o *SinkCredentialInput) SetKvVersion(v int64)`

SetKvVersion sets KvVersion field to given value.

### HasKvVersion

`func (o *SinkCredentialInput) HasKvVersion() bool`

HasKvVersion returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


