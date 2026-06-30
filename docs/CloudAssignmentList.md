# CloudAssignmentList

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Items** | [**[]CloudAssignmentResponse**](CloudAssignmentResponse.md) | Cloud Assignments in the current page. | 
**NextCursor** | Pointer to **string** | Continuation token for the next page. &#x60;null&#x60; or omitted when the iteration has reached end-of-stream. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400&#x60; on the next call.  | [optional] 

## Methods

### NewCloudAssignmentList

`func NewCloudAssignmentList(items []CloudAssignmentResponse, ) *CloudAssignmentList`

NewCloudAssignmentList instantiates a new CloudAssignmentList object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCloudAssignmentListWithDefaults

`func NewCloudAssignmentListWithDefaults() *CloudAssignmentList`

NewCloudAssignmentListWithDefaults instantiates a new CloudAssignmentList object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetItems

`func (o *CloudAssignmentList) GetItems() []CloudAssignmentResponse`

GetItems returns the Items field if non-nil, zero value otherwise.

### GetItemsOk

`func (o *CloudAssignmentList) GetItemsOk() (*[]CloudAssignmentResponse, bool)`

GetItemsOk returns a tuple with the Items field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetItems

`func (o *CloudAssignmentList) SetItems(v []CloudAssignmentResponse)`

SetItems sets Items field to given value.


### GetNextCursor

`func (o *CloudAssignmentList) GetNextCursor() string`

GetNextCursor returns the NextCursor field if non-nil, zero value otherwise.

### GetNextCursorOk

`func (o *CloudAssignmentList) GetNextCursorOk() (*string, bool)`

GetNextCursorOk returns a tuple with the NextCursor field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNextCursor

`func (o *CloudAssignmentList) SetNextCursor(v string)`

SetNextCursor sets NextCursor field to given value.

### HasNextCursor

`func (o *CloudAssignmentList) HasNextCursor() bool`

HasNextCursor returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


