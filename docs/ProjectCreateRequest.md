# ProjectCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DomainId** | **string** | Parent Domain identifier (UUIDv7). The handler authorises &#x60;manage&#x60; on &#x60;domain:&lt;id&gt;&#x60; BEFORE invoking the service .  | 
**Name** | **string** | Human-readable Project name. Whitespace-only is rejected. | 
**Slug** | **string** | Kebab-case URL handle. The aggregate&#39;s &#x60;ParseSlug&#x60; enforces the same regex; surfacing the pattern here lets the generated client validate before the round-trip.  | 
**Description** | Pointer to **string** | Optional free-form description. Whitespace-only strings are rejected by the aggregate (the operator most likely fat-fingered the field instead of meaning to clear it).  | [optional] 
**SubRangeCidr** | Pointer to **string** | Optional canonical RFC 4632 sub-range reservation. Must be contained in the parent Domain&#39;s mesh_cidr and must not overlap a sibling Project&#39;s reservation. Surfaces as &#x60;409 sub_range_overlap&#x60; on conflict.  | [optional] 

## Methods

### NewProjectCreateRequest

`func NewProjectCreateRequest(domainId string, name string, slug string, ) *ProjectCreateRequest`

NewProjectCreateRequest instantiates a new ProjectCreateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewProjectCreateRequestWithDefaults

`func NewProjectCreateRequestWithDefaults() *ProjectCreateRequest`

NewProjectCreateRequestWithDefaults instantiates a new ProjectCreateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDomainId

`func (o *ProjectCreateRequest) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *ProjectCreateRequest) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *ProjectCreateRequest) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.


### GetName

`func (o *ProjectCreateRequest) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *ProjectCreateRequest) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *ProjectCreateRequest) SetName(v string)`

SetName sets Name field to given value.


### GetSlug

`func (o *ProjectCreateRequest) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *ProjectCreateRequest) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *ProjectCreateRequest) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetDescription

`func (o *ProjectCreateRequest) GetDescription() string`

GetDescription returns the Description field if non-nil, zero value otherwise.

### GetDescriptionOk

`func (o *ProjectCreateRequest) GetDescriptionOk() (*string, bool)`

GetDescriptionOk returns a tuple with the Description field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDescription

`func (o *ProjectCreateRequest) SetDescription(v string)`

SetDescription sets Description field to given value.

### HasDescription

`func (o *ProjectCreateRequest) HasDescription() bool`

HasDescription returns a boolean if a field has been set.

### GetSubRangeCidr

`func (o *ProjectCreateRequest) GetSubRangeCidr() string`

GetSubRangeCidr returns the SubRangeCidr field if non-nil, zero value otherwise.

### GetSubRangeCidrOk

`func (o *ProjectCreateRequest) GetSubRangeCidrOk() (*string, bool)`

GetSubRangeCidrOk returns a tuple with the SubRangeCidr field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubRangeCidr

`func (o *ProjectCreateRequest) SetSubRangeCidr(v string)`

SetSubRangeCidr sets SubRangeCidr field to given value.

### HasSubRangeCidr

`func (o *ProjectCreateRequest) HasSubRangeCidr() bool`

HasSubRangeCidr returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


