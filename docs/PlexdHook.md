# PlexdHook

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | PlexdHook resource name (e.g. &#x60;nightly-backup&#x60;). Non-empty after trimming whitespace; a violation surfaces as 422 &#x60;plexd_hook_invalid&#x60;.  | 
**ImageDigest** | **string** | OCI image digest of the hook image in canonical &#x60;sha256:&lt;64 lowercase hex&gt;&#x60; form. Format-only validation — plexsphere performs no registry lookup. Anything that does not match surfaces as 422 &#x60;plexd_hook_invalid&#x60;.  | 
**Parameters** | Pointer to **map[string]string** | Optional free-form string-to-string parameter map copied verbatim from the discovered PlexdHook spec.  | [optional] 
**TimeoutSeconds** | Pointer to **int64** | Optional execution timeout in whole seconds. Non-negative; a negative value surfaces as 422 &#x60;plexd_hook_invalid&#x60;. The domain owns this as a duration — the &#x60;_seconds&#x60; suffix is the wire encoding only.  | [optional] 
**Sandbox** | Pointer to **bool** | Optional flag indicating the discovered hook requests sandboxed execution. Absent is treated as &#x60;false&#x60;.  | [optional] 

## Methods

### NewPlexdHook

`func NewPlexdHook(name string, imageDigest string, ) *PlexdHook`

NewPlexdHook instantiates a new PlexdHook object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewPlexdHookWithDefaults

`func NewPlexdHookWithDefaults() *PlexdHook`

NewPlexdHookWithDefaults instantiates a new PlexdHook object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetName

`func (o *PlexdHook) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *PlexdHook) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *PlexdHook) SetName(v string)`

SetName sets Name field to given value.


### GetImageDigest

`func (o *PlexdHook) GetImageDigest() string`

GetImageDigest returns the ImageDigest field if non-nil, zero value otherwise.

### GetImageDigestOk

`func (o *PlexdHook) GetImageDigestOk() (*string, bool)`

GetImageDigestOk returns a tuple with the ImageDigest field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetImageDigest

`func (o *PlexdHook) SetImageDigest(v string)`

SetImageDigest sets ImageDigest field to given value.


### GetParameters

`func (o *PlexdHook) GetParameters() map[string]string`

GetParameters returns the Parameters field if non-nil, zero value otherwise.

### GetParametersOk

`func (o *PlexdHook) GetParametersOk() (*map[string]string, bool)`

GetParametersOk returns a tuple with the Parameters field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetParameters

`func (o *PlexdHook) SetParameters(v map[string]string)`

SetParameters sets Parameters field to given value.

### HasParameters

`func (o *PlexdHook) HasParameters() bool`

HasParameters returns a boolean if a field has been set.

### GetTimeoutSeconds

`func (o *PlexdHook) GetTimeoutSeconds() int64`

GetTimeoutSeconds returns the TimeoutSeconds field if non-nil, zero value otherwise.

### GetTimeoutSecondsOk

`func (o *PlexdHook) GetTimeoutSecondsOk() (*int64, bool)`

GetTimeoutSecondsOk returns a tuple with the TimeoutSeconds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTimeoutSeconds

`func (o *PlexdHook) SetTimeoutSeconds(v int64)`

SetTimeoutSeconds sets TimeoutSeconds field to given value.

### HasTimeoutSeconds

`func (o *PlexdHook) HasTimeoutSeconds() bool`

HasTimeoutSeconds returns a boolean if a field has been set.

### GetSandbox

`func (o *PlexdHook) GetSandbox() bool`

GetSandbox returns the Sandbox field if non-nil, zero value otherwise.

### GetSandboxOk

`func (o *PlexdHook) GetSandboxOk() (*bool, bool)`

GetSandboxOk returns a tuple with the Sandbox field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSandbox

`func (o *PlexdHook) SetSandbox(v bool)`

SetSandbox sets Sandbox field to given value.

### HasSandbox

`func (o *PlexdHook) HasSandbox() bool`

HasSandbox returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


