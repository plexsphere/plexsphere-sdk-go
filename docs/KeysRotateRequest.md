# KeysRotateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**NewPublicKey** | **string** | The Node&#39;s freshly-generated Curve25519 (WireGuard) public key, 32 bytes, base64-encoded with standard padding. RFC 7748 §5 fixes the curve to a 32-byte little-endian point encoding, so any other decoded length is rejected with 422 &#x60;keys_rotate_public_key_invalid&#x60;; the all-zero degenerate value (a known small-order point) is rejected with the same code. A key byte-identical to the Node&#39;s current public key is rejected with 422 &#x60;keys_rotate_public_key_unchanged&#x60;.  | 

## Methods

### NewKeysRotateRequest

`func NewKeysRotateRequest(newPublicKey string, ) *KeysRotateRequest`

NewKeysRotateRequest instantiates a new KeysRotateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewKeysRotateRequestWithDefaults

`func NewKeysRotateRequestWithDefaults() *KeysRotateRequest`

NewKeysRotateRequestWithDefaults instantiates a new KeysRotateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetNewPublicKey

`func (o *KeysRotateRequest) GetNewPublicKey() string`

GetNewPublicKey returns the NewPublicKey field if non-nil, zero value otherwise.

### GetNewPublicKeyOk

`func (o *KeysRotateRequest) GetNewPublicKeyOk() (*string, bool)`

GetNewPublicKeyOk returns a tuple with the NewPublicKey field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNewPublicKey

`func (o *KeysRotateRequest) SetNewPublicKey(v string)`

SetNewPublicKey sets NewPublicKey field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


