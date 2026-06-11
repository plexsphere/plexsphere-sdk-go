# DeclaredHook

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Hook identifier (e.g. &#x60;post-install&#x60;). Non-empty after trimming whitespace; a violation surfaces as 400 &#x60;declared_hook_invalid&#x60;.  | 
**Checksum** | **string** | SHA-256 digest of the hook payload, 32 bytes base64-encoded with standard padding. Anything that does not decode to exactly 32 bytes surfaces as 400 &#x60;declared_hook_invalid&#x60;.  | 

## Methods

### NewDeclaredHook

`func NewDeclaredHook(name string, checksum string, ) *DeclaredHook`

NewDeclaredHook instantiates a new DeclaredHook object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDeclaredHookWithDefaults

`func NewDeclaredHookWithDefaults() *DeclaredHook`

NewDeclaredHookWithDefaults instantiates a new DeclaredHook object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetName

`func (o *DeclaredHook) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *DeclaredHook) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *DeclaredHook) SetName(v string)`

SetName sets Name field to given value.


### GetChecksum

`func (o *DeclaredHook) GetChecksum() string`

GetChecksum returns the Checksum field if non-nil, zero value otherwise.

### GetChecksumOk

`func (o *DeclaredHook) GetChecksumOk() (*string, bool)`

GetChecksumOk returns a tuple with the Checksum field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChecksum

`func (o *DeclaredHook) SetChecksum(v string)`

SetChecksum sets Checksum field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


