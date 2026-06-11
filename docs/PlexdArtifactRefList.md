# PlexdArtifactRefList

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Items** | [**[]PlexdArtifactRef**](PlexdArtifactRef.md) | Indexed plexd releases in the current page. | 
**NextCursor** | Pointer to **string** | Continuation token for the next page. &#x60;null&#x60; or omitted when the iteration has reached end-of-stream. The encoding is HMAC-signed so a tampered cursor surfaces as &#x60;400&#x60; on the next call.  | [optional] 

## Methods

### NewPlexdArtifactRefList

`func NewPlexdArtifactRefList(items []PlexdArtifactRef, ) *PlexdArtifactRefList`

NewPlexdArtifactRefList instantiates a new PlexdArtifactRefList object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewPlexdArtifactRefListWithDefaults

`func NewPlexdArtifactRefListWithDefaults() *PlexdArtifactRefList`

NewPlexdArtifactRefListWithDefaults instantiates a new PlexdArtifactRefList object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetItems

`func (o *PlexdArtifactRefList) GetItems() []PlexdArtifactRef`

GetItems returns the Items field if non-nil, zero value otherwise.

### GetItemsOk

`func (o *PlexdArtifactRefList) GetItemsOk() (*[]PlexdArtifactRef, bool)`

GetItemsOk returns a tuple with the Items field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetItems

`func (o *PlexdArtifactRefList) SetItems(v []PlexdArtifactRef)`

SetItems sets Items field to given value.


### GetNextCursor

`func (o *PlexdArtifactRefList) GetNextCursor() string`

GetNextCursor returns the NextCursor field if non-nil, zero value otherwise.

### GetNextCursorOk

`func (o *PlexdArtifactRefList) GetNextCursorOk() (*string, bool)`

GetNextCursorOk returns a tuple with the NextCursor field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNextCursor

`func (o *PlexdArtifactRefList) SetNextCursor(v string)`

SetNextCursor sets NextCursor field to given value.

### HasNextCursor

`func (o *PlexdArtifactRefList) HasNextCursor() bool`

HasNextCursor returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


