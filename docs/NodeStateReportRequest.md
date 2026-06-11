# NodeStateReportRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Value** | **string** | The report value to store for the addressed key. Capped at 4096 bytes; an over-size value is rejected with 400.  | 
**WorkloadTag** | Pointer to **string** | Optional tag of the workload producing the report. Stored verbatim and echoed back on the next reconciliation pull.  | [optional] 

## Methods

### NewNodeStateReportRequest

`func NewNodeStateReportRequest(value string, ) *NodeStateReportRequest`

NewNodeStateReportRequest instantiates a new NodeStateReportRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewNodeStateReportRequestWithDefaults

`func NewNodeStateReportRequestWithDefaults() *NodeStateReportRequest`

NewNodeStateReportRequestWithDefaults instantiates a new NodeStateReportRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetValue

`func (o *NodeStateReportRequest) GetValue() string`

GetValue returns the Value field if non-nil, zero value otherwise.

### GetValueOk

`func (o *NodeStateReportRequest) GetValueOk() (*string, bool)`

GetValueOk returns a tuple with the Value field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetValue

`func (o *NodeStateReportRequest) SetValue(v string)`

SetValue sets Value field to given value.


### GetWorkloadTag

`func (o *NodeStateReportRequest) GetWorkloadTag() string`

GetWorkloadTag returns the WorkloadTag field if non-nil, zero value otherwise.

### GetWorkloadTagOk

`func (o *NodeStateReportRequest) GetWorkloadTagOk() (*string, bool)`

GetWorkloadTagOk returns a tuple with the WorkloadTag field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetWorkloadTag

`func (o *NodeStateReportRequest) SetWorkloadTag(v string)`

SetWorkloadTag sets WorkloadTag field to given value.

### HasWorkloadTag

`func (o *NodeStateReportRequest) HasWorkloadTag() bool`

HasWorkloadTag returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


