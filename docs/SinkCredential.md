# SinkCredential

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**KvMount** | **string** | KV mount the material lives under. | 
**KvPath** | **string** | Path the material lives at under the mount. It is derived server-side from the owning Domain and the sink id, so a reference can never address another tenant&#39;s material.  | 
**KvVersion** | Pointer to **int64** | KV version to read. Absent or &#x60;0&#x60; reads the latest one.  | [optional] 

## Methods

### NewSinkCredential

`func NewSinkCredential(kvMount string, kvPath string, ) *SinkCredential`

NewSinkCredential instantiates a new SinkCredential object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSinkCredentialWithDefaults

`func NewSinkCredentialWithDefaults() *SinkCredential`

NewSinkCredentialWithDefaults instantiates a new SinkCredential object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetKvMount

`func (o *SinkCredential) GetKvMount() string`

GetKvMount returns the KvMount field if non-nil, zero value otherwise.

### GetKvMountOk

`func (o *SinkCredential) GetKvMountOk() (*string, bool)`

GetKvMountOk returns a tuple with the KvMount field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKvMount

`func (o *SinkCredential) SetKvMount(v string)`

SetKvMount sets KvMount field to given value.


### GetKvPath

`func (o *SinkCredential) GetKvPath() string`

GetKvPath returns the KvPath field if non-nil, zero value otherwise.

### GetKvPathOk

`func (o *SinkCredential) GetKvPathOk() (*string, bool)`

GetKvPathOk returns a tuple with the KvPath field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKvPath

`func (o *SinkCredential) SetKvPath(v string)`

SetKvPath sets KvPath field to given value.


### GetKvVersion

`func (o *SinkCredential) GetKvVersion() int64`

GetKvVersion returns the KvVersion field if non-nil, zero value otherwise.

### GetKvVersionOk

`func (o *SinkCredential) GetKvVersionOk() (*int64, bool)`

GetKvVersionOk returns a tuple with the KvVersion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKvVersion

`func (o *SinkCredential) SetKvVersion(v int64)`

SetKvVersion sets KvVersion field to given value.

### HasKvVersion

`func (o *SinkCredential) HasKvVersion() bool`

HasKvVersion returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


