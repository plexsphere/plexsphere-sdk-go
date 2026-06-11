# ProjectPatchRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | Pointer to **string** | New human-readable Project name. The aggregate&#39;s &#x60;Rename&#x60; mutator validates the same constraints as &#x60;NewProject&#x60;.  | [optional] 
**Description** | Pointer to **string** | New free-form description. The empty string clears the description; a whitespace-only string is rejected so an operator typo cannot silently wipe the field.  | [optional] 
**SubRangeCidr** | Pointer to **string** | New canonical RFC 4632 sub-range reservation. Triggers the in-tx sibling-overlap guard inside the parent Domain (&#x60;409 sub_range_overlap&#x60; / &#x60;422 sub_range_invalidates_allocation&#x60;).  | [optional] 
**ReleaseSubRange** | Pointer to **bool** | When &#x60;true&#x60;, clears the existing sub-range reservation. Mutually exclusive with &#x60;sub_range_cidr&#x60; — the service rejects bodies that carry both with &#x60;422 sub_range_invalidates_allocation&#x60;.  | [optional] 

## Methods

### NewProjectPatchRequest

`func NewProjectPatchRequest() *ProjectPatchRequest`

NewProjectPatchRequest instantiates a new ProjectPatchRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewProjectPatchRequestWithDefaults

`func NewProjectPatchRequestWithDefaults() *ProjectPatchRequest`

NewProjectPatchRequestWithDefaults instantiates a new ProjectPatchRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetName

`func (o *ProjectPatchRequest) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *ProjectPatchRequest) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *ProjectPatchRequest) SetName(v string)`

SetName sets Name field to given value.

### HasName

`func (o *ProjectPatchRequest) HasName() bool`

HasName returns a boolean if a field has been set.

### GetDescription

`func (o *ProjectPatchRequest) GetDescription() string`

GetDescription returns the Description field if non-nil, zero value otherwise.

### GetDescriptionOk

`func (o *ProjectPatchRequest) GetDescriptionOk() (*string, bool)`

GetDescriptionOk returns a tuple with the Description field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDescription

`func (o *ProjectPatchRequest) SetDescription(v string)`

SetDescription sets Description field to given value.

### HasDescription

`func (o *ProjectPatchRequest) HasDescription() bool`

HasDescription returns a boolean if a field has been set.

### GetSubRangeCidr

`func (o *ProjectPatchRequest) GetSubRangeCidr() string`

GetSubRangeCidr returns the SubRangeCidr field if non-nil, zero value otherwise.

### GetSubRangeCidrOk

`func (o *ProjectPatchRequest) GetSubRangeCidrOk() (*string, bool)`

GetSubRangeCidrOk returns a tuple with the SubRangeCidr field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubRangeCidr

`func (o *ProjectPatchRequest) SetSubRangeCidr(v string)`

SetSubRangeCidr sets SubRangeCidr field to given value.

### HasSubRangeCidr

`func (o *ProjectPatchRequest) HasSubRangeCidr() bool`

HasSubRangeCidr returns a boolean if a field has been set.

### GetReleaseSubRange

`func (o *ProjectPatchRequest) GetReleaseSubRange() bool`

GetReleaseSubRange returns the ReleaseSubRange field if non-nil, zero value otherwise.

### GetReleaseSubRangeOk

`func (o *ProjectPatchRequest) GetReleaseSubRangeOk() (*bool, bool)`

GetReleaseSubRangeOk returns a tuple with the ReleaseSubRange field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetReleaseSubRange

`func (o *ProjectPatchRequest) SetReleaseSubRange(v bool)`

SetReleaseSubRange sets ReleaseSubRange field to given value.

### HasReleaseSubRange

`func (o *ProjectPatchRequest) HasReleaseSubRange() bool`

HasReleaseSubRange returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


