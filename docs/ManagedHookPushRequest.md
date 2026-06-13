# ManagedHookPushRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Namespace** | **string** | Target namespace the PlexdHook is applied into. | 
**Name** | **string** | PlexdHook object name. | 
**ImageDigest** | **string** | Pinned image digest the hook executes — a &#x60;sha256:&#x60; content address, never a mutable tag.  | 
**Parameters** | Pointer to **map[string]string** | Opaque string-to-string parameter map forwarded to the hook.  | [optional] 
**TimeoutSeconds** | Pointer to **int64** | Per-invocation timeout in seconds. Zero or omitted leaves the agent&#39;s default in force.  | [optional] 
**Sandbox** | Pointer to **bool** | Whether the hook runs in the agent&#39;s sandboxed execution mode.  | [optional] 

## Methods

### NewManagedHookPushRequest

`func NewManagedHookPushRequest(namespace string, name string, imageDigest string, ) *ManagedHookPushRequest`

NewManagedHookPushRequest instantiates a new ManagedHookPushRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewManagedHookPushRequestWithDefaults

`func NewManagedHookPushRequestWithDefaults() *ManagedHookPushRequest`

NewManagedHookPushRequestWithDefaults instantiates a new ManagedHookPushRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetNamespace

`func (o *ManagedHookPushRequest) GetNamespace() string`

GetNamespace returns the Namespace field if non-nil, zero value otherwise.

### GetNamespaceOk

`func (o *ManagedHookPushRequest) GetNamespaceOk() (*string, bool)`

GetNamespaceOk returns a tuple with the Namespace field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNamespace

`func (o *ManagedHookPushRequest) SetNamespace(v string)`

SetNamespace sets Namespace field to given value.


### GetName

`func (o *ManagedHookPushRequest) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *ManagedHookPushRequest) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *ManagedHookPushRequest) SetName(v string)`

SetName sets Name field to given value.


### GetImageDigest

`func (o *ManagedHookPushRequest) GetImageDigest() string`

GetImageDigest returns the ImageDigest field if non-nil, zero value otherwise.

### GetImageDigestOk

`func (o *ManagedHookPushRequest) GetImageDigestOk() (*string, bool)`

GetImageDigestOk returns a tuple with the ImageDigest field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetImageDigest

`func (o *ManagedHookPushRequest) SetImageDigest(v string)`

SetImageDigest sets ImageDigest field to given value.


### GetParameters

`func (o *ManagedHookPushRequest) GetParameters() map[string]string`

GetParameters returns the Parameters field if non-nil, zero value otherwise.

### GetParametersOk

`func (o *ManagedHookPushRequest) GetParametersOk() (*map[string]string, bool)`

GetParametersOk returns a tuple with the Parameters field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetParameters

`func (o *ManagedHookPushRequest) SetParameters(v map[string]string)`

SetParameters sets Parameters field to given value.

### HasParameters

`func (o *ManagedHookPushRequest) HasParameters() bool`

HasParameters returns a boolean if a field has been set.

### GetTimeoutSeconds

`func (o *ManagedHookPushRequest) GetTimeoutSeconds() int64`

GetTimeoutSeconds returns the TimeoutSeconds field if non-nil, zero value otherwise.

### GetTimeoutSecondsOk

`func (o *ManagedHookPushRequest) GetTimeoutSecondsOk() (*int64, bool)`

GetTimeoutSecondsOk returns a tuple with the TimeoutSeconds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTimeoutSeconds

`func (o *ManagedHookPushRequest) SetTimeoutSeconds(v int64)`

SetTimeoutSeconds sets TimeoutSeconds field to given value.

### HasTimeoutSeconds

`func (o *ManagedHookPushRequest) HasTimeoutSeconds() bool`

HasTimeoutSeconds returns a boolean if a field has been set.

### GetSandbox

`func (o *ManagedHookPushRequest) GetSandbox() bool`

GetSandbox returns the Sandbox field if non-nil, zero value otherwise.

### GetSandboxOk

`func (o *ManagedHookPushRequest) GetSandboxOk() (*bool, bool)`

GetSandboxOk returns a tuple with the Sandbox field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSandbox

`func (o *ManagedHookPushRequest) SetSandbox(v bool)`

SetSandbox sets Sandbox field to given value.

### HasSandbox

`func (o *ManagedHookPushRequest) HasSandbox() bool`

HasSandbox returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


