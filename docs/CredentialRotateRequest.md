# CredentialRotateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ExpectedVersion** | **int64** | The broker-row &#x60;version&#x60; the caller observed. The Custodian performs a compare-and-swap against this value.  | 
**Material** | [**CredentialRotateMaterial**](CredentialRotateMaterial.md) |  | 

## Methods

### NewCredentialRotateRequest

`func NewCredentialRotateRequest(expectedVersion int64, material CredentialRotateMaterial, ) *CredentialRotateRequest`

NewCredentialRotateRequest instantiates a new CredentialRotateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCredentialRotateRequestWithDefaults

`func NewCredentialRotateRequestWithDefaults() *CredentialRotateRequest`

NewCredentialRotateRequestWithDefaults instantiates a new CredentialRotateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetExpectedVersion

`func (o *CredentialRotateRequest) GetExpectedVersion() int64`

GetExpectedVersion returns the ExpectedVersion field if non-nil, zero value otherwise.

### GetExpectedVersionOk

`func (o *CredentialRotateRequest) GetExpectedVersionOk() (*int64, bool)`

GetExpectedVersionOk returns a tuple with the ExpectedVersion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExpectedVersion

`func (o *CredentialRotateRequest) SetExpectedVersion(v int64)`

SetExpectedVersion sets ExpectedVersion field to given value.


### GetMaterial

`func (o *CredentialRotateRequest) GetMaterial() CredentialRotateMaterial`

GetMaterial returns the Material field if non-nil, zero value otherwise.

### GetMaterialOk

`func (o *CredentialRotateRequest) GetMaterialOk() (*CredentialRotateMaterial, bool)`

GetMaterialOk returns a tuple with the Material field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMaterial

`func (o *CredentialRotateRequest) SetMaterial(v CredentialRotateMaterial)`

SetMaterial sets Material field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


