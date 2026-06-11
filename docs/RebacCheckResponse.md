# RebacCheckResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Decision** | [**RebacCheckResponseDecision**](RebacCheckResponseDecision.md) |  | 
**RelationPath** | Pointer to **[]string** | Ordered sequence of relations the authorizer traversed while evaluating the Check. Set only when &#x60;decision&#x60; is &#x60;allowed&#x60;. Empty array when the decision was reached without a relation lookup (typically a direct-binding allowance).  | [optional] 
**Reason** | Pointer to [**RebacCheckResponseReason**](RebacCheckResponseReason.md) |  | [optional] 
**CorrelationId** | **string** | Correlation id that pairs this decision with the matching audit entry emitted by &#x60;internal/audit&#x60;.  | 

## Methods

### NewRebacCheckResponse

`func NewRebacCheckResponse(decision RebacCheckResponseDecision, correlationId string, ) *RebacCheckResponse`

NewRebacCheckResponse instantiates a new RebacCheckResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewRebacCheckResponseWithDefaults

`func NewRebacCheckResponseWithDefaults() *RebacCheckResponse`

NewRebacCheckResponseWithDefaults instantiates a new RebacCheckResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDecision

`func (o *RebacCheckResponse) GetDecision() RebacCheckResponseDecision`

GetDecision returns the Decision field if non-nil, zero value otherwise.

### GetDecisionOk

`func (o *RebacCheckResponse) GetDecisionOk() (*RebacCheckResponseDecision, bool)`

GetDecisionOk returns a tuple with the Decision field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDecision

`func (o *RebacCheckResponse) SetDecision(v RebacCheckResponseDecision)`

SetDecision sets Decision field to given value.


### GetRelationPath

`func (o *RebacCheckResponse) GetRelationPath() []string`

GetRelationPath returns the RelationPath field if non-nil, zero value otherwise.

### GetRelationPathOk

`func (o *RebacCheckResponse) GetRelationPathOk() (*[]string, bool)`

GetRelationPathOk returns a tuple with the RelationPath field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRelationPath

`func (o *RebacCheckResponse) SetRelationPath(v []string)`

SetRelationPath sets RelationPath field to given value.

### HasRelationPath

`func (o *RebacCheckResponse) HasRelationPath() bool`

HasRelationPath returns a boolean if a field has been set.

### GetReason

`func (o *RebacCheckResponse) GetReason() RebacCheckResponseReason`

GetReason returns the Reason field if non-nil, zero value otherwise.

### GetReasonOk

`func (o *RebacCheckResponse) GetReasonOk() (*RebacCheckResponseReason, bool)`

GetReasonOk returns a tuple with the Reason field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetReason

`func (o *RebacCheckResponse) SetReason(v RebacCheckResponseReason)`

SetReason sets Reason field to given value.

### HasReason

`func (o *RebacCheckResponse) HasReason() bool`

HasReason returns a boolean if a field has been set.

### GetCorrelationId

`func (o *RebacCheckResponse) GetCorrelationId() string`

GetCorrelationId returns the CorrelationId field if non-nil, zero value otherwise.

### GetCorrelationIdOk

`func (o *RebacCheckResponse) GetCorrelationIdOk() (*string, bool)`

GetCorrelationIdOk returns a tuple with the CorrelationId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCorrelationId

`func (o *RebacCheckResponse) SetCorrelationId(v string)`

SetCorrelationId sets CorrelationId field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


