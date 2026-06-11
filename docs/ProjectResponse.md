# ProjectResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Project identifier (UUIDv7). | 
**DomainId** | **string** | Parent Domain identifier (UUIDv7). | 
**Name** | **string** | Human-readable Project name (trimmed at the aggregate). | 
**Slug** | **string** | Kebab-case URL handle. Stable for the lifetime of the Project — see the &#x60;tenancy&#x60; tag description for the immutability rationale.  | 
**Description** | Pointer to **string** | Optional free-form description. Empty string when the operator did not set one (the wire shape never carries &#x60;null&#x60; for this field).  | [optional] 
**SubRangeCidr** | Pointer to **string** | Optional canonical RFC 4632 sub-range reservation inside the parent Domain&#39;s mesh_cidr. Cross-Project non-overlap within the parent Domain is enforced by the SQL GIST exclusion constraint on &#x60;plexsphere.project_mesh_ip_reservations&#x60;.  | [optional] 
**CreatedAt** | **time.Time** | Aggregate creation timestamp (UTC). | 
**UpdatedAt** | **time.Time** | Last-modified timestamp (UTC). Bumped by every mutator — &#x60;Rename&#x60;, &#x60;ChangeDescription&#x60;, &#x60;ReserveSubRange&#x60;, &#x60;ResizeSubRange&#x60;, &#x60;ReleaseSubRange&#x60;.  | 

## Methods

### NewProjectResponse

`func NewProjectResponse(id string, domainId string, name string, slug string, createdAt time.Time, updatedAt time.Time, ) *ProjectResponse`

NewProjectResponse instantiates a new ProjectResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewProjectResponseWithDefaults

`func NewProjectResponseWithDefaults() *ProjectResponse`

NewProjectResponseWithDefaults instantiates a new ProjectResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *ProjectResponse) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *ProjectResponse) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *ProjectResponse) SetId(v string)`

SetId sets Id field to given value.


### GetDomainId

`func (o *ProjectResponse) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *ProjectResponse) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *ProjectResponse) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.


### GetName

`func (o *ProjectResponse) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *ProjectResponse) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *ProjectResponse) SetName(v string)`

SetName sets Name field to given value.


### GetSlug

`func (o *ProjectResponse) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *ProjectResponse) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *ProjectResponse) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetDescription

`func (o *ProjectResponse) GetDescription() string`

GetDescription returns the Description field if non-nil, zero value otherwise.

### GetDescriptionOk

`func (o *ProjectResponse) GetDescriptionOk() (*string, bool)`

GetDescriptionOk returns a tuple with the Description field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDescription

`func (o *ProjectResponse) SetDescription(v string)`

SetDescription sets Description field to given value.

### HasDescription

`func (o *ProjectResponse) HasDescription() bool`

HasDescription returns a boolean if a field has been set.

### GetSubRangeCidr

`func (o *ProjectResponse) GetSubRangeCidr() string`

GetSubRangeCidr returns the SubRangeCidr field if non-nil, zero value otherwise.

### GetSubRangeCidrOk

`func (o *ProjectResponse) GetSubRangeCidrOk() (*string, bool)`

GetSubRangeCidrOk returns a tuple with the SubRangeCidr field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubRangeCidr

`func (o *ProjectResponse) SetSubRangeCidr(v string)`

SetSubRangeCidr sets SubRangeCidr field to given value.

### HasSubRangeCidr

`func (o *ProjectResponse) HasSubRangeCidr() bool`

HasSubRangeCidr returns a boolean if a field has been set.

### GetCreatedAt

`func (o *ProjectResponse) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *ProjectResponse) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *ProjectResponse) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetUpdatedAt

`func (o *ProjectResponse) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *ProjectResponse) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *ProjectResponse) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


