# ProviderBundleVersionList

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Items** | [**[]ProviderBundleVersion**](ProviderBundleVersion.md) | Versions of the bundle in the current page, newest first. An empty array is a valid page.  | 
**NextCursor** | Pointer to **string** | Continuation token for the next page. Absent when the iteration has reached end-of-stream. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400&#x60; on the next call.  | [optional] 

## Methods

### NewProviderBundleVersionList

`func NewProviderBundleVersionList(items []ProviderBundleVersion, ) *ProviderBundleVersionList`

NewProviderBundleVersionList instantiates a new ProviderBundleVersionList object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewProviderBundleVersionListWithDefaults

`func NewProviderBundleVersionListWithDefaults() *ProviderBundleVersionList`

NewProviderBundleVersionListWithDefaults instantiates a new ProviderBundleVersionList object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetItems

`func (o *ProviderBundleVersionList) GetItems() []ProviderBundleVersion`

GetItems returns the Items field if non-nil, zero value otherwise.

### GetItemsOk

`func (o *ProviderBundleVersionList) GetItemsOk() (*[]ProviderBundleVersion, bool)`

GetItemsOk returns a tuple with the Items field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetItems

`func (o *ProviderBundleVersionList) SetItems(v []ProviderBundleVersion)`

SetItems sets Items field to given value.


### GetNextCursor

`func (o *ProviderBundleVersionList) GetNextCursor() string`

GetNextCursor returns the NextCursor field if non-nil, zero value otherwise.

### GetNextCursorOk

`func (o *ProviderBundleVersionList) GetNextCursorOk() (*string, bool)`

GetNextCursorOk returns a tuple with the NextCursor field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNextCursor

`func (o *ProviderBundleVersionList) SetNextCursor(v string)`

SetNextCursor sets NextCursor field to given value.

### HasNextCursor

`func (o *ProviderBundleVersionList) HasNextCursor() bool`

HasNextCursor returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


