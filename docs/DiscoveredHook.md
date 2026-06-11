# DiscoveredHook

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**NodeId** | **string** | Node the hook was discovered on (UUIDv7). | 
**DomainId** | **string** | Owning Domain (UUIDv7) — the residency pivot the per-row visibility filter authorises against.  | 
**Name** | **string** | Discovered hook resource name. | 
**ImageDigest** | **string** | OCI image digest of the discovered hook image in canonical &#x60;sha256:&lt;64 lowercase hex&gt;&#x60; form.  | 
**ImageDigestMatch** | **bool** | &#x60;true&#x60; when the discovered image digest matches the digest declared in the Node&#39;s capability manifest, &#x60;false&#x60; when it diverges.  | 

## Methods

### NewDiscoveredHook

`func NewDiscoveredHook(nodeId string, domainId string, name string, imageDigest string, imageDigestMatch bool, ) *DiscoveredHook`

NewDiscoveredHook instantiates a new DiscoveredHook object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDiscoveredHookWithDefaults

`func NewDiscoveredHookWithDefaults() *DiscoveredHook`

NewDiscoveredHookWithDefaults instantiates a new DiscoveredHook object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetNodeId

`func (o *DiscoveredHook) GetNodeId() string`

GetNodeId returns the NodeId field if non-nil, zero value otherwise.

### GetNodeIdOk

`func (o *DiscoveredHook) GetNodeIdOk() (*string, bool)`

GetNodeIdOk returns a tuple with the NodeId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNodeId

`func (o *DiscoveredHook) SetNodeId(v string)`

SetNodeId sets NodeId field to given value.


### GetDomainId

`func (o *DiscoveredHook) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *DiscoveredHook) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *DiscoveredHook) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.


### GetName

`func (o *DiscoveredHook) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *DiscoveredHook) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *DiscoveredHook) SetName(v string)`

SetName sets Name field to given value.


### GetImageDigest

`func (o *DiscoveredHook) GetImageDigest() string`

GetImageDigest returns the ImageDigest field if non-nil, zero value otherwise.

### GetImageDigestOk

`func (o *DiscoveredHook) GetImageDigestOk() (*string, bool)`

GetImageDigestOk returns a tuple with the ImageDigest field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetImageDigest

`func (o *DiscoveredHook) SetImageDigest(v string)`

SetImageDigest sets ImageDigest field to given value.


### GetImageDigestMatch

`func (o *DiscoveredHook) GetImageDigestMatch() bool`

GetImageDigestMatch returns the ImageDigestMatch field if non-nil, zero value otherwise.

### GetImageDigestMatchOk

`func (o *DiscoveredHook) GetImageDigestMatchOk() (*bool, bool)`

GetImageDigestMatchOk returns a tuple with the ImageDigestMatch field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetImageDigestMatch

`func (o *DiscoveredHook) SetImageDigestMatch(v bool)`

SetImageDigestMatch sets ImageDigestMatch field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


