# RelationTuple

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Relation tuple identifier (UUIDv7). | 
**Subject** | **string** | Object reference of the subject side. | 
**Relation** | **string** | Relation name (e.g. &#x60;maintainer&#x60;, &#x60;read&#x60;). | 
**Resource** | **string** | Object reference of the resource side. | 
**CaveatContext** | Pointer to **map[string]interface{}** | Optional set of caveat field NAMES the tuple binds. NAMES only — values never cross the contract boundary.  | [optional] 
**CreatedAt** | **time.Time** | Aggregate creation timestamp (UTC). | 

## Methods

### NewRelationTuple

`func NewRelationTuple(id string, subject string, relation string, resource string, createdAt time.Time, ) *RelationTuple`

NewRelationTuple instantiates a new RelationTuple object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewRelationTupleWithDefaults

`func NewRelationTupleWithDefaults() *RelationTuple`

NewRelationTupleWithDefaults instantiates a new RelationTuple object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *RelationTuple) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *RelationTuple) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *RelationTuple) SetId(v string)`

SetId sets Id field to given value.


### GetSubject

`func (o *RelationTuple) GetSubject() string`

GetSubject returns the Subject field if non-nil, zero value otherwise.

### GetSubjectOk

`func (o *RelationTuple) GetSubjectOk() (*string, bool)`

GetSubjectOk returns a tuple with the Subject field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubject

`func (o *RelationTuple) SetSubject(v string)`

SetSubject sets Subject field to given value.


### GetRelation

`func (o *RelationTuple) GetRelation() string`

GetRelation returns the Relation field if non-nil, zero value otherwise.

### GetRelationOk

`func (o *RelationTuple) GetRelationOk() (*string, bool)`

GetRelationOk returns a tuple with the Relation field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRelation

`func (o *RelationTuple) SetRelation(v string)`

SetRelation sets Relation field to given value.


### GetResource

`func (o *RelationTuple) GetResource() string`

GetResource returns the Resource field if non-nil, zero value otherwise.

### GetResourceOk

`func (o *RelationTuple) GetResourceOk() (*string, bool)`

GetResourceOk returns a tuple with the Resource field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResource

`func (o *RelationTuple) SetResource(v string)`

SetResource sets Resource field to given value.


### GetCaveatContext

`func (o *RelationTuple) GetCaveatContext() map[string]interface{}`

GetCaveatContext returns the CaveatContext field if non-nil, zero value otherwise.

### GetCaveatContextOk

`func (o *RelationTuple) GetCaveatContextOk() (*map[string]interface{}, bool)`

GetCaveatContextOk returns a tuple with the CaveatContext field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCaveatContext

`func (o *RelationTuple) SetCaveatContext(v map[string]interface{})`

SetCaveatContext sets CaveatContext field to given value.

### HasCaveatContext

`func (o *RelationTuple) HasCaveatContext() bool`

HasCaveatContext returns a boolean if a field has been set.

### GetCreatedAt

`func (o *RelationTuple) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *RelationTuple) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *RelationTuple) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


