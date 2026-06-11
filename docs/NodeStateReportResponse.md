# NodeStateReportResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AcceptedAt** | **time.Time** | Server wall-clock time at which the report write was accepted and durably recorded.  | 
**Key** | **string** | The report key that was written. | 

## Methods

### NewNodeStateReportResponse

`func NewNodeStateReportResponse(acceptedAt time.Time, key string, ) *NodeStateReportResponse`

NewNodeStateReportResponse instantiates a new NodeStateReportResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewNodeStateReportResponseWithDefaults

`func NewNodeStateReportResponseWithDefaults() *NodeStateReportResponse`

NewNodeStateReportResponseWithDefaults instantiates a new NodeStateReportResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetAcceptedAt

`func (o *NodeStateReportResponse) GetAcceptedAt() time.Time`

GetAcceptedAt returns the AcceptedAt field if non-nil, zero value otherwise.

### GetAcceptedAtOk

`func (o *NodeStateReportResponse) GetAcceptedAtOk() (*time.Time, bool)`

GetAcceptedAtOk returns a tuple with the AcceptedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAcceptedAt

`func (o *NodeStateReportResponse) SetAcceptedAt(v time.Time)`

SetAcceptedAt sets AcceptedAt field to given value.


### GetKey

`func (o *NodeStateReportResponse) GetKey() string`

GetKey returns the Key field if non-nil, zero value otherwise.

### GetKeyOk

`func (o *NodeStateReportResponse) GetKeyOk() (*string, bool)`

GetKeyOk returns a tuple with the Key field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKey

`func (o *NodeStateReportResponse) SetKey(v string)`

SetKey sets Key field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


