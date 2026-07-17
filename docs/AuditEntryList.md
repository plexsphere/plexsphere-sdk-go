# AuditEntryList

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Items** | [**[]AuditEntry**](AuditEntry.md) | Audit rows in ascending &#x60;seq&#x60; order. | 
**NextCursor** | Pointer to **string** | Opaque, HMAC-signed cursor scoped to the addressed chain. Replaying a cursor minted for a different chain surfaces as 400 with &#x60;code: invalid_cursor&#x60;.  | [optional] 

## Methods

### NewAuditEntryList

`func NewAuditEntryList(items []AuditEntry, ) *AuditEntryList`

NewAuditEntryList instantiates a new AuditEntryList object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewAuditEntryListWithDefaults

`func NewAuditEntryListWithDefaults() *AuditEntryList`

NewAuditEntryListWithDefaults instantiates a new AuditEntryList object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetItems

`func (o *AuditEntryList) GetItems() []AuditEntry`

GetItems returns the Items field if non-nil, zero value otherwise.

### GetItemsOk

`func (o *AuditEntryList) GetItemsOk() (*[]AuditEntry, bool)`

GetItemsOk returns a tuple with the Items field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetItems

`func (o *AuditEntryList) SetItems(v []AuditEntry)`

SetItems sets Items field to given value.


### GetNextCursor

`func (o *AuditEntryList) GetNextCursor() string`

GetNextCursor returns the NextCursor field if non-nil, zero value otherwise.

### GetNextCursorOk

`func (o *AuditEntryList) GetNextCursorOk() (*string, bool)`

GetNextCursorOk returns a tuple with the NextCursor field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNextCursor

`func (o *AuditEntryList) SetNextCursor(v string)`

SetNextCursor sets NextCursor field to given value.

### HasNextCursor

`func (o *AuditEntryList) HasNextCursor() bool`

HasNextCursor returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


