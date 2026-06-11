# DomainCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Human-readable Domain name. Whitespace-only is rejected. | 
**Slug** | **string** | Kebab-case URL handle. The aggregate&#39;s &#x60;ParseSlug&#x60; enforces the same regex; surfacing the pattern here lets the generated client validate before the round-trip.  | 
**Description** | Pointer to **string** | Optional free-form description. Whitespace-only strings are rejected by the aggregate (the operator most likely fat- fingered the field instead of meaning to clear it).  | [optional] 
**Region** | Pointer to **string** | Optional region the Domain is pinned to at creation; absent or empty means the Domain is left unpinned. The aggregate&#39;s &#x60;ParseRegion&#x60; enforces the same regex, so surfacing the pattern here lets the generated client validate before the round-trip.  | [optional] 
**MeshCidr** | **string** | Canonical RFC 4632 mesh-IP pool. Cross-Domain non-overlap is enforced by the SQL GIST exclusion constraint and surfaces as &#x60;409 mesh_cidr_overlap&#x60;.  | 
**Reachability** | Pointer to [**DomainReachabilityPolicy**](DomainReachabilityPolicy.md) |  | [optional] 

## Methods

### NewDomainCreateRequest

`func NewDomainCreateRequest(name string, slug string, meshCidr string, ) *DomainCreateRequest`

NewDomainCreateRequest instantiates a new DomainCreateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDomainCreateRequestWithDefaults

`func NewDomainCreateRequestWithDefaults() *DomainCreateRequest`

NewDomainCreateRequestWithDefaults instantiates a new DomainCreateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetName

`func (o *DomainCreateRequest) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *DomainCreateRequest) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *DomainCreateRequest) SetName(v string)`

SetName sets Name field to given value.


### GetSlug

`func (o *DomainCreateRequest) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *DomainCreateRequest) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *DomainCreateRequest) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetDescription

`func (o *DomainCreateRequest) GetDescription() string`

GetDescription returns the Description field if non-nil, zero value otherwise.

### GetDescriptionOk

`func (o *DomainCreateRequest) GetDescriptionOk() (*string, bool)`

GetDescriptionOk returns a tuple with the Description field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDescription

`func (o *DomainCreateRequest) SetDescription(v string)`

SetDescription sets Description field to given value.

### HasDescription

`func (o *DomainCreateRequest) HasDescription() bool`

HasDescription returns a boolean if a field has been set.

### GetRegion

`func (o *DomainCreateRequest) GetRegion() string`

GetRegion returns the Region field if non-nil, zero value otherwise.

### GetRegionOk

`func (o *DomainCreateRequest) GetRegionOk() (*string, bool)`

GetRegionOk returns a tuple with the Region field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRegion

`func (o *DomainCreateRequest) SetRegion(v string)`

SetRegion sets Region field to given value.

### HasRegion

`func (o *DomainCreateRequest) HasRegion() bool`

HasRegion returns a boolean if a field has been set.

### GetMeshCidr

`func (o *DomainCreateRequest) GetMeshCidr() string`

GetMeshCidr returns the MeshCidr field if non-nil, zero value otherwise.

### GetMeshCidrOk

`func (o *DomainCreateRequest) GetMeshCidrOk() (*string, bool)`

GetMeshCidrOk returns a tuple with the MeshCidr field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMeshCidr

`func (o *DomainCreateRequest) SetMeshCidr(v string)`

SetMeshCidr sets MeshCidr field to given value.


### GetReachability

`func (o *DomainCreateRequest) GetReachability() DomainReachabilityPolicy`

GetReachability returns the Reachability field if non-nil, zero value otherwise.

### GetReachabilityOk

`func (o *DomainCreateRequest) GetReachabilityOk() (*DomainReachabilityPolicy, bool)`

GetReachabilityOk returns a tuple with the Reachability field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetReachability

`func (o *DomainCreateRequest) SetReachability(v DomainReachabilityPolicy)`

SetReachability sets Reachability field to given value.

### HasReachability

`func (o *DomainCreateRequest) HasReachability() bool`

HasReachability returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


