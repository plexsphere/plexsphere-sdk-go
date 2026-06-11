# SessionActivityK8s

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Verb** | **string** | Kubernetes API verb the request issued. | 
**ResourceKind** | Pointer to **string** | Kubernetes resource kind the request addressed. | [optional] 
**Namespace** | Pointer to **string** | Namespace the request addressed, when namespaced. | [optional] 
**Name** | Pointer to **string** | Resource name the request addressed, when named. | [optional] 
**StatusCode** | Pointer to **int32** | HTTP status the API server returned. | [optional] 
**DurationMs** | Pointer to **int32** | Request duration in milliseconds. | [optional] 

## Methods

### NewSessionActivityK8s

`func NewSessionActivityK8s(verb string, ) *SessionActivityK8s`

NewSessionActivityK8s instantiates a new SessionActivityK8s object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSessionActivityK8sWithDefaults

`func NewSessionActivityK8sWithDefaults() *SessionActivityK8s`

NewSessionActivityK8sWithDefaults instantiates a new SessionActivityK8s object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetVerb

`func (o *SessionActivityK8s) GetVerb() string`

GetVerb returns the Verb field if non-nil, zero value otherwise.

### GetVerbOk

`func (o *SessionActivityK8s) GetVerbOk() (*string, bool)`

GetVerbOk returns a tuple with the Verb field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetVerb

`func (o *SessionActivityK8s) SetVerb(v string)`

SetVerb sets Verb field to given value.


### GetResourceKind

`func (o *SessionActivityK8s) GetResourceKind() string`

GetResourceKind returns the ResourceKind field if non-nil, zero value otherwise.

### GetResourceKindOk

`func (o *SessionActivityK8s) GetResourceKindOk() (*string, bool)`

GetResourceKindOk returns a tuple with the ResourceKind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResourceKind

`func (o *SessionActivityK8s) SetResourceKind(v string)`

SetResourceKind sets ResourceKind field to given value.

### HasResourceKind

`func (o *SessionActivityK8s) HasResourceKind() bool`

HasResourceKind returns a boolean if a field has been set.

### GetNamespace

`func (o *SessionActivityK8s) GetNamespace() string`

GetNamespace returns the Namespace field if non-nil, zero value otherwise.

### GetNamespaceOk

`func (o *SessionActivityK8s) GetNamespaceOk() (*string, bool)`

GetNamespaceOk returns a tuple with the Namespace field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNamespace

`func (o *SessionActivityK8s) SetNamespace(v string)`

SetNamespace sets Namespace field to given value.

### HasNamespace

`func (o *SessionActivityK8s) HasNamespace() bool`

HasNamespace returns a boolean if a field has been set.

### GetName

`func (o *SessionActivityK8s) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *SessionActivityK8s) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *SessionActivityK8s) SetName(v string)`

SetName sets Name field to given value.

### HasName

`func (o *SessionActivityK8s) HasName() bool`

HasName returns a boolean if a field has been set.

### GetStatusCode

`func (o *SessionActivityK8s) GetStatusCode() int32`

GetStatusCode returns the StatusCode field if non-nil, zero value otherwise.

### GetStatusCodeOk

`func (o *SessionActivityK8s) GetStatusCodeOk() (*int32, bool)`

GetStatusCodeOk returns a tuple with the StatusCode field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatusCode

`func (o *SessionActivityK8s) SetStatusCode(v int32)`

SetStatusCode sets StatusCode field to given value.

### HasStatusCode

`func (o *SessionActivityK8s) HasStatusCode() bool`

HasStatusCode returns a boolean if a field has been set.

### GetDurationMs

`func (o *SessionActivityK8s) GetDurationMs() int32`

GetDurationMs returns the DurationMs field if non-nil, zero value otherwise.

### GetDurationMsOk

`func (o *SessionActivityK8s) GetDurationMsOk() (*int32, bool)`

GetDurationMsOk returns a tuple with the DurationMs field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDurationMs

`func (o *SessionActivityK8s) SetDurationMs(v int32)`

SetDurationMs sets DurationMs field to given value.

### HasDurationMs

`func (o *SessionActivityK8s) HasDurationMs() bool`

HasDurationMs returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


