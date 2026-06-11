# DomainPatchRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | Pointer to **string** | New human-readable Domain name. The aggregate&#39;s &#x60;Rename&#x60; mutator validates the same constraints as &#x60;NewDomain&#x60;.  | [optional] 
**Description** | Pointer to **string** | New free-form description. The empty string clears the description; a whitespace-only string is rejected so an operator typo cannot silently wipe the field.  | [optional] 
**Region** | Pointer to **string** | Re-pin the Domain to a region. The aggregate&#39;s &#x60;ParseRegion&#x60; enforces the same regex. Unlike the immutable &#x60;slug&#x60;, the region is freely re-pinnable through this mutator.  | [optional] 
**MeshCidr** | Pointer to **string** | New canonical RFC 4632 mesh-IP pool. Triggers the cross- Domain GIST exclusion check (&#x60;409 mesh_cidr_overlap&#x60;) and the service-level containment guard against &#x60;project_mesh_ip_reservations.sub_range&#x60; (&#x60;422 mesh_cidr_invalidates_subrange&#x60;).  | [optional] 
**Reachability** | Pointer to [**DomainReachabilityPolicy**](DomainReachabilityPolicy.md) |  | [optional] 

## Methods

### NewDomainPatchRequest

`func NewDomainPatchRequest() *DomainPatchRequest`

NewDomainPatchRequest instantiates a new DomainPatchRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDomainPatchRequestWithDefaults

`func NewDomainPatchRequestWithDefaults() *DomainPatchRequest`

NewDomainPatchRequestWithDefaults instantiates a new DomainPatchRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetName

`func (o *DomainPatchRequest) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *DomainPatchRequest) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *DomainPatchRequest) SetName(v string)`

SetName sets Name field to given value.

### HasName

`func (o *DomainPatchRequest) HasName() bool`

HasName returns a boolean if a field has been set.

### GetDescription

`func (o *DomainPatchRequest) GetDescription() string`

GetDescription returns the Description field if non-nil, zero value otherwise.

### GetDescriptionOk

`func (o *DomainPatchRequest) GetDescriptionOk() (*string, bool)`

GetDescriptionOk returns a tuple with the Description field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDescription

`func (o *DomainPatchRequest) SetDescription(v string)`

SetDescription sets Description field to given value.

### HasDescription

`func (o *DomainPatchRequest) HasDescription() bool`

HasDescription returns a boolean if a field has been set.

### GetRegion

`func (o *DomainPatchRequest) GetRegion() string`

GetRegion returns the Region field if non-nil, zero value otherwise.

### GetRegionOk

`func (o *DomainPatchRequest) GetRegionOk() (*string, bool)`

GetRegionOk returns a tuple with the Region field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRegion

`func (o *DomainPatchRequest) SetRegion(v string)`

SetRegion sets Region field to given value.

### HasRegion

`func (o *DomainPatchRequest) HasRegion() bool`

HasRegion returns a boolean if a field has been set.

### GetMeshCidr

`func (o *DomainPatchRequest) GetMeshCidr() string`

GetMeshCidr returns the MeshCidr field if non-nil, zero value otherwise.

### GetMeshCidrOk

`func (o *DomainPatchRequest) GetMeshCidrOk() (*string, bool)`

GetMeshCidrOk returns a tuple with the MeshCidr field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMeshCidr

`func (o *DomainPatchRequest) SetMeshCidr(v string)`

SetMeshCidr sets MeshCidr field to given value.

### HasMeshCidr

`func (o *DomainPatchRequest) HasMeshCidr() bool`

HasMeshCidr returns a boolean if a field has been set.

### GetReachability

`func (o *DomainPatchRequest) GetReachability() DomainReachabilityPolicy`

GetReachability returns the Reachability field if non-nil, zero value otherwise.

### GetReachabilityOk

`func (o *DomainPatchRequest) GetReachabilityOk() (*DomainReachabilityPolicy, bool)`

GetReachabilityOk returns a tuple with the Reachability field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetReachability

`func (o *DomainPatchRequest) SetReachability(v DomainReachabilityPolicy)`

SetReachability sets Reachability field to given value.

### HasReachability

`func (o *DomainPatchRequest) HasReachability() bool`

HasReachability returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


