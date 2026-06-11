# DomainResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Domain identifier (UUIDv7). | 
**Name** | **string** | Human-readable Domain name (trimmed at the aggregate). | 
**Slug** | **string** | Kebab-case URL handle. Stable for the lifetime of the Domain — see the &#x60;tenancy&#x60; tag description for the immutability rationale.  | 
**Description** | Pointer to **string** | Optional free-form description. Empty string when the operator did not set one (the wire shape never carries &#x60;null&#x60; for this field).  | [optional] 
**Region** | Pointer to **string** | The region the Domain is pinned to. Unlike &#x60;description&#x60;, this field is OMITTED from the wire entirely when the Domain is unpinned — it is never carried as an empty string, so an absent key means \&quot;no region\&quot;.  | [optional] 
**MeshCidr** | **string** | Canonical RFC 4632 mesh-IP pool the Domain owns. Cross- Domain non-overlap is enforced by the SQL GIST exclusion constraint.  | 
**Reachability** | [**DomainReachabilityPolicy**](DomainReachabilityPolicy.md) |  | 
**CreatedAt** | **time.Time** | Aggregate creation timestamp (UTC). | 
**UpdatedAt** | **time.Time** | Last-modified timestamp (UTC). Bumped by every mutator — &#x60;Rename&#x60;, &#x60;ChangeDescription&#x60;, &#x60;RetargetMeshCIDR&#x60;, and &#x60;ChangeReachabilityPolicy&#x60;.  | 

## Methods

### NewDomainResponse

`func NewDomainResponse(id string, name string, slug string, meshCidr string, reachability DomainReachabilityPolicy, createdAt time.Time, updatedAt time.Time, ) *DomainResponse`

NewDomainResponse instantiates a new DomainResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDomainResponseWithDefaults

`func NewDomainResponseWithDefaults() *DomainResponse`

NewDomainResponseWithDefaults instantiates a new DomainResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *DomainResponse) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *DomainResponse) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *DomainResponse) SetId(v string)`

SetId sets Id field to given value.


### GetName

`func (o *DomainResponse) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *DomainResponse) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *DomainResponse) SetName(v string)`

SetName sets Name field to given value.


### GetSlug

`func (o *DomainResponse) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *DomainResponse) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *DomainResponse) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetDescription

`func (o *DomainResponse) GetDescription() string`

GetDescription returns the Description field if non-nil, zero value otherwise.

### GetDescriptionOk

`func (o *DomainResponse) GetDescriptionOk() (*string, bool)`

GetDescriptionOk returns a tuple with the Description field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDescription

`func (o *DomainResponse) SetDescription(v string)`

SetDescription sets Description field to given value.

### HasDescription

`func (o *DomainResponse) HasDescription() bool`

HasDescription returns a boolean if a field has been set.

### GetRegion

`func (o *DomainResponse) GetRegion() string`

GetRegion returns the Region field if non-nil, zero value otherwise.

### GetRegionOk

`func (o *DomainResponse) GetRegionOk() (*string, bool)`

GetRegionOk returns a tuple with the Region field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRegion

`func (o *DomainResponse) SetRegion(v string)`

SetRegion sets Region field to given value.

### HasRegion

`func (o *DomainResponse) HasRegion() bool`

HasRegion returns a boolean if a field has been set.

### GetMeshCidr

`func (o *DomainResponse) GetMeshCidr() string`

GetMeshCidr returns the MeshCidr field if non-nil, zero value otherwise.

### GetMeshCidrOk

`func (o *DomainResponse) GetMeshCidrOk() (*string, bool)`

GetMeshCidrOk returns a tuple with the MeshCidr field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMeshCidr

`func (o *DomainResponse) SetMeshCidr(v string)`

SetMeshCidr sets MeshCidr field to given value.


### GetReachability

`func (o *DomainResponse) GetReachability() DomainReachabilityPolicy`

GetReachability returns the Reachability field if non-nil, zero value otherwise.

### GetReachabilityOk

`func (o *DomainResponse) GetReachabilityOk() (*DomainReachabilityPolicy, bool)`

GetReachabilityOk returns a tuple with the Reachability field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetReachability

`func (o *DomainResponse) SetReachability(v DomainReachabilityPolicy)`

SetReachability sets Reachability field to given value.


### GetCreatedAt

`func (o *DomainResponse) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *DomainResponse) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *DomainResponse) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetUpdatedAt

`func (o *DomainResponse) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *DomainResponse) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *DomainResponse) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


