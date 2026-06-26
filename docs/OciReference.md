# OciReference

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Registry** | **string** | Registry host with an optional port, e.g. &#x60;ghcr.io&#x60;. | 
**Repository** | **string** | Slash-separated repository path, e.g. &#x60;plexsphere/catalog&#x60;. | 
**Tag** | Pointer to **string** | Mutable tag, e.g. &#x60;v1.2.3&#x60;. Set exactly one of &#x60;tag&#x60; or &#x60;digest&#x60;. A &#x60;track-tag&#x60; tracking policy requires a tag.  | [optional] 
**Digest** | Pointer to **string** | Immutable &#x60;sha256:&lt;64 hex&gt;&#x60; content digest. Set exactly one of &#x60;tag&#x60; or &#x60;digest&#x60;.  | [optional] 

## Methods

### NewOciReference

`func NewOciReference(registry string, repository string, ) *OciReference`

NewOciReference instantiates a new OciReference object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewOciReferenceWithDefaults

`func NewOciReferenceWithDefaults() *OciReference`

NewOciReferenceWithDefaults instantiates a new OciReference object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetRegistry

`func (o *OciReference) GetRegistry() string`

GetRegistry returns the Registry field if non-nil, zero value otherwise.

### GetRegistryOk

`func (o *OciReference) GetRegistryOk() (*string, bool)`

GetRegistryOk returns a tuple with the Registry field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRegistry

`func (o *OciReference) SetRegistry(v string)`

SetRegistry sets Registry field to given value.


### GetRepository

`func (o *OciReference) GetRepository() string`

GetRepository returns the Repository field if non-nil, zero value otherwise.

### GetRepositoryOk

`func (o *OciReference) GetRepositoryOk() (*string, bool)`

GetRepositoryOk returns a tuple with the Repository field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRepository

`func (o *OciReference) SetRepository(v string)`

SetRepository sets Repository field to given value.


### GetTag

`func (o *OciReference) GetTag() string`

GetTag returns the Tag field if non-nil, zero value otherwise.

### GetTagOk

`func (o *OciReference) GetTagOk() (*string, bool)`

GetTagOk returns a tuple with the Tag field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTag

`func (o *OciReference) SetTag(v string)`

SetTag sets Tag field to given value.

### HasTag

`func (o *OciReference) HasTag() bool`

HasTag returns a boolean if a field has been set.

### GetDigest

`func (o *OciReference) GetDigest() string`

GetDigest returns the Digest field if non-nil, zero value otherwise.

### GetDigestOk

`func (o *OciReference) GetDigestOk() (*string, bool)`

GetDigestOk returns a tuple with the Digest field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDigest

`func (o *OciReference) SetDigest(v string)`

SetDigest sets Digest field to given value.

### HasDigest

`func (o *OciReference) HasDigest() bool`

HasDigest returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


