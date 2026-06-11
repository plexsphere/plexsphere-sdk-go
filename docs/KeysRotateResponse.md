# KeysRotateResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**RotationId** | **string** | Identifier of the &#x60;peer_key_rotation&#x60; row this submission flipped from &#x60;pending&#x60; to &#x60;completed&#x60;. The Node records it so a later audit query can correlate the rotation back to the re-issued PSK row.  | 
**Kid** | **string** | Key id of the freshly-wrapped pairwise PSK the rotation re-issued. Paired with &#x60;wrap_key_version&#x60; it is the reference plexd uses to resolve the PSK without the control plane re-transmitting secret material.  | 
**WrapKeyVersion** | **int32** | Version of the active wrap key under which the re-issued PSK was wrapped. Paired with &#x60;kid&#x60; it pins the exact wrapping epoch.  | 

## Methods

### NewKeysRotateResponse

`func NewKeysRotateResponse(rotationId string, kid string, wrapKeyVersion int32, ) *KeysRotateResponse`

NewKeysRotateResponse instantiates a new KeysRotateResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewKeysRotateResponseWithDefaults

`func NewKeysRotateResponseWithDefaults() *KeysRotateResponse`

NewKeysRotateResponseWithDefaults instantiates a new KeysRotateResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetRotationId

`func (o *KeysRotateResponse) GetRotationId() string`

GetRotationId returns the RotationId field if non-nil, zero value otherwise.

### GetRotationIdOk

`func (o *KeysRotateResponse) GetRotationIdOk() (*string, bool)`

GetRotationIdOk returns a tuple with the RotationId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRotationId

`func (o *KeysRotateResponse) SetRotationId(v string)`

SetRotationId sets RotationId field to given value.


### GetKid

`func (o *KeysRotateResponse) GetKid() string`

GetKid returns the Kid field if non-nil, zero value otherwise.

### GetKidOk

`func (o *KeysRotateResponse) GetKidOk() (*string, bool)`

GetKidOk returns a tuple with the Kid field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKid

`func (o *KeysRotateResponse) SetKid(v string)`

SetKid sets Kid field to given value.


### GetWrapKeyVersion

`func (o *KeysRotateResponse) GetWrapKeyVersion() int32`

GetWrapKeyVersion returns the WrapKeyVersion field if non-nil, zero value otherwise.

### GetWrapKeyVersionOk

`func (o *KeysRotateResponse) GetWrapKeyVersionOk() (*int32, bool)`

GetWrapKeyVersionOk returns a tuple with the WrapKeyVersion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetWrapKeyVersion

`func (o *KeysRotateResponse) SetWrapKeyVersion(v int32)`

SetWrapKeyVersion sets WrapKeyVersion field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


