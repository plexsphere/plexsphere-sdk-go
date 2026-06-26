# IncidentList

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Items** | [**[]Incident**](Incident.md) | The incident headers on this page. | 
**NextCursor** | Pointer to **string** | Opaque pagination cursor for the next page, or absent when the page is the last.  | [optional] 

## Methods

### NewIncidentList

`func NewIncidentList(items []Incident, ) *IncidentList`

NewIncidentList instantiates a new IncidentList object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewIncidentListWithDefaults

`func NewIncidentListWithDefaults() *IncidentList`

NewIncidentListWithDefaults instantiates a new IncidentList object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetItems

`func (o *IncidentList) GetItems() []Incident`

GetItems returns the Items field if non-nil, zero value otherwise.

### GetItemsOk

`func (o *IncidentList) GetItemsOk() (*[]Incident, bool)`

GetItemsOk returns a tuple with the Items field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetItems

`func (o *IncidentList) SetItems(v []Incident)`

SetItems sets Items field to given value.


### GetNextCursor

`func (o *IncidentList) GetNextCursor() string`

GetNextCursor returns the NextCursor field if non-nil, zero value otherwise.

### GetNextCursorOk

`func (o *IncidentList) GetNextCursorOk() (*string, bool)`

GetNextCursorOk returns a tuple with the NextCursor field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNextCursor

`func (o *IncidentList) SetNextCursor(v string)`

SetNextCursor sets NextCursor field to given value.

### HasNextCursor

`func (o *IncidentList) HasNextCursor() bool`

HasNextCursor returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


