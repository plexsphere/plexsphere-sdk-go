# RelationTupleCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Subject** | **string** | Object reference of the subject side. | 
**Relation** | **string** | Relation name. | 
**Resource** | **string** | Object reference of the resource side. | 
**CaveatName** | Pointer to **string** | Optional caveat program name to attach to the tuple. When set, SpiceDB evaluates the caveat against the supplied &#x60;caveat_context&#x60; at every Check.  | [optional] 
**CaveatContext** | Pointer to **map[string]interface{}** | Optional set of caveat field NAMES the tuple binds. NAMES only — values never cross the contract boundary.  | [optional] 

## Methods

### NewRelationTupleCreateRequest

`func NewRelationTupleCreateRequest(subject string, relation string, resource string, ) *RelationTupleCreateRequest`

NewRelationTupleCreateRequest instantiates a new RelationTupleCreateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewRelationTupleCreateRequestWithDefaults

`func NewRelationTupleCreateRequestWithDefaults() *RelationTupleCreateRequest`

NewRelationTupleCreateRequestWithDefaults instantiates a new RelationTupleCreateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSubject

`func (o *RelationTupleCreateRequest) GetSubject() string`

GetSubject returns the Subject field if non-nil, zero value otherwise.

### GetSubjectOk

`func (o *RelationTupleCreateRequest) GetSubjectOk() (*string, bool)`

GetSubjectOk returns a tuple with the Subject field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubject

`func (o *RelationTupleCreateRequest) SetSubject(v string)`

SetSubject sets Subject field to given value.


### GetRelation

`func (o *RelationTupleCreateRequest) GetRelation() string`

GetRelation returns the Relation field if non-nil, zero value otherwise.

### GetRelationOk

`func (o *RelationTupleCreateRequest) GetRelationOk() (*string, bool)`

GetRelationOk returns a tuple with the Relation field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRelation

`func (o *RelationTupleCreateRequest) SetRelation(v string)`

SetRelation sets Relation field to given value.


### GetResource

`func (o *RelationTupleCreateRequest) GetResource() string`

GetResource returns the Resource field if non-nil, zero value otherwise.

### GetResourceOk

`func (o *RelationTupleCreateRequest) GetResourceOk() (*string, bool)`

GetResourceOk returns a tuple with the Resource field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResource

`func (o *RelationTupleCreateRequest) SetResource(v string)`

SetResource sets Resource field to given value.


### GetCaveatName

`func (o *RelationTupleCreateRequest) GetCaveatName() string`

GetCaveatName returns the CaveatName field if non-nil, zero value otherwise.

### GetCaveatNameOk

`func (o *RelationTupleCreateRequest) GetCaveatNameOk() (*string, bool)`

GetCaveatNameOk returns a tuple with the CaveatName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCaveatName

`func (o *RelationTupleCreateRequest) SetCaveatName(v string)`

SetCaveatName sets CaveatName field to given value.

### HasCaveatName

`func (o *RelationTupleCreateRequest) HasCaveatName() bool`

HasCaveatName returns a boolean if a field has been set.

### GetCaveatContext

`func (o *RelationTupleCreateRequest) GetCaveatContext() map[string]interface{}`

GetCaveatContext returns the CaveatContext field if non-nil, zero value otherwise.

### GetCaveatContextOk

`func (o *RelationTupleCreateRequest) GetCaveatContextOk() (*map[string]interface{}, bool)`

GetCaveatContextOk returns a tuple with the CaveatContext field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCaveatContext

`func (o *RelationTupleCreateRequest) SetCaveatContext(v map[string]interface{})`

SetCaveatContext sets CaveatContext field to given value.

### HasCaveatContext

`func (o *RelationTupleCreateRequest) HasCaveatContext() bool`

HasCaveatContext returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


