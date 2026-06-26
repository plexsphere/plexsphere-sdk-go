# ImportOutcome

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Slug** | **string** | The Blueprint slug this outcome reports on. | 
**Status** | [**ImportOutcomeStatus**](ImportOutcomeStatus.md) |  | 
**Version** | Pointer to **string** | The version label, present for &#x60;imported&#x60;, &#x60;unchanged&#x60;, and &#x60;drift&#x60;.  | [optional] 
**Detail** | Pointer to **string** | The drift diff, present for the &#x60;drift&#x60; status. | [optional] 
**Reason** | Pointer to [**ImportOutcomeReason**](ImportOutcomeReason.md) |  | [optional] 

## Methods

### NewImportOutcome

`func NewImportOutcome(slug string, status ImportOutcomeStatus, ) *ImportOutcome`

NewImportOutcome instantiates a new ImportOutcome object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewImportOutcomeWithDefaults

`func NewImportOutcomeWithDefaults() *ImportOutcome`

NewImportOutcomeWithDefaults instantiates a new ImportOutcome object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSlug

`func (o *ImportOutcome) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *ImportOutcome) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *ImportOutcome) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetStatus

`func (o *ImportOutcome) GetStatus() ImportOutcomeStatus`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *ImportOutcome) GetStatusOk() (*ImportOutcomeStatus, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *ImportOutcome) SetStatus(v ImportOutcomeStatus)`

SetStatus sets Status field to given value.


### GetVersion

`func (o *ImportOutcome) GetVersion() string`

GetVersion returns the Version field if non-nil, zero value otherwise.

### GetVersionOk

`func (o *ImportOutcome) GetVersionOk() (*string, bool)`

GetVersionOk returns a tuple with the Version field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetVersion

`func (o *ImportOutcome) SetVersion(v string)`

SetVersion sets Version field to given value.

### HasVersion

`func (o *ImportOutcome) HasVersion() bool`

HasVersion returns a boolean if a field has been set.

### GetDetail

`func (o *ImportOutcome) GetDetail() string`

GetDetail returns the Detail field if non-nil, zero value otherwise.

### GetDetailOk

`func (o *ImportOutcome) GetDetailOk() (*string, bool)`

GetDetailOk returns a tuple with the Detail field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDetail

`func (o *ImportOutcome) SetDetail(v string)`

SetDetail sets Detail field to given value.

### HasDetail

`func (o *ImportOutcome) HasDetail() bool`

HasDetail returns a boolean if a field has been set.

### GetReason

`func (o *ImportOutcome) GetReason() ImportOutcomeReason`

GetReason returns the Reason field if non-nil, zero value otherwise.

### GetReasonOk

`func (o *ImportOutcome) GetReasonOk() (*ImportOutcomeReason, bool)`

GetReasonOk returns a tuple with the Reason field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetReason

`func (o *ImportOutcome) SetReason(v ImportOutcomeReason)`

SetReason sets Reason field to given value.

### HasReason

`func (o *ImportOutcome) HasReason() bool`

HasReason returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


