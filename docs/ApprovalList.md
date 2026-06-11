# ApprovalList

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Items** | [**[]Approval**](Approval.md) | Approvals in the current page. | 
**NextCursor** | Pointer to **string** | Continuation token for the next page. &#x60;null&#x60; or omitted when the iteration has reached end-of-stream. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400&#x60; on the next call.  | [optional] 

## Methods

### NewApprovalList

`func NewApprovalList(items []Approval, ) *ApprovalList`

NewApprovalList instantiates a new ApprovalList object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewApprovalListWithDefaults

`func NewApprovalListWithDefaults() *ApprovalList`

NewApprovalListWithDefaults instantiates a new ApprovalList object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetItems

`func (o *ApprovalList) GetItems() []Approval`

GetItems returns the Items field if non-nil, zero value otherwise.

### GetItemsOk

`func (o *ApprovalList) GetItemsOk() (*[]Approval, bool)`

GetItemsOk returns a tuple with the Items field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetItems

`func (o *ApprovalList) SetItems(v []Approval)`

SetItems sets Items field to given value.


### GetNextCursor

`func (o *ApprovalList) GetNextCursor() string`

GetNextCursor returns the NextCursor field if non-nil, zero value otherwise.

### GetNextCursorOk

`func (o *ApprovalList) GetNextCursorOk() (*string, bool)`

GetNextCursorOk returns a tuple with the NextCursor field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNextCursor

`func (o *ApprovalList) SetNextCursor(v string)`

SetNextCursor sets NextCursor field to given value.

### HasNextCursor

`func (o *ApprovalList) HasNextCursor() bool`

HasNextCursor returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


