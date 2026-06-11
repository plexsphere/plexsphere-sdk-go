# LabelAssignmentRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DefinitionId** | **string** | Parent Label Definition. DECISION: addressed by id rather than qualified key — the transport resolves qualified keys to ids at decode time, and Assignment.Put must round-trip the exact aggregate that produced the snapshot.  | 
**Value** | **interface{}** |  | 

## Methods

### NewLabelAssignmentRequest

`func NewLabelAssignmentRequest(definitionId string, value interface{}, ) *LabelAssignmentRequest`

NewLabelAssignmentRequest instantiates a new LabelAssignmentRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewLabelAssignmentRequestWithDefaults

`func NewLabelAssignmentRequestWithDefaults() *LabelAssignmentRequest`

NewLabelAssignmentRequestWithDefaults instantiates a new LabelAssignmentRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDefinitionId

`func (o *LabelAssignmentRequest) GetDefinitionId() string`

GetDefinitionId returns the DefinitionId field if non-nil, zero value otherwise.

### GetDefinitionIdOk

`func (o *LabelAssignmentRequest) GetDefinitionIdOk() (*string, bool)`

GetDefinitionIdOk returns a tuple with the DefinitionId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDefinitionId

`func (o *LabelAssignmentRequest) SetDefinitionId(v string)`

SetDefinitionId sets DefinitionId field to given value.


### GetValue

`func (o *LabelAssignmentRequest) GetValue() interface{}`

GetValue returns the Value field if non-nil, zero value otherwise.

### GetValueOk

`func (o *LabelAssignmentRequest) GetValueOk() (*interface{}, bool)`

GetValueOk returns a tuple with the Value field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetValue

`func (o *LabelAssignmentRequest) SetValue(v interface{})`

SetValue sets Value field to given value.


### SetValueNil

`func (o *LabelAssignmentRequest) SetValueNil(b bool)`

 SetValueNil sets the value for Value to be an explicit nil

### UnsetValue
`func (o *LabelAssignmentRequest) UnsetValue()`

UnsetValue ensures that no value is present for Value, not even an explicit nil

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


