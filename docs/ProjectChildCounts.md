# ProjectChildCounts

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Resources** | **int32** | Number of &#x60;Resource&#x60; aggregates still attached. | 
**Nodes** | **int32** | Number of &#x60;Node&#x60; aggregates still attached. | 
**RelationTuples** | **int32** | Number of relation tuples still referencing the Project. | 

## Methods

### NewProjectChildCounts

`func NewProjectChildCounts(resources int32, nodes int32, relationTuples int32, ) *ProjectChildCounts`

NewProjectChildCounts instantiates a new ProjectChildCounts object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewProjectChildCountsWithDefaults

`func NewProjectChildCountsWithDefaults() *ProjectChildCounts`

NewProjectChildCountsWithDefaults instantiates a new ProjectChildCounts object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetResources

`func (o *ProjectChildCounts) GetResources() int32`

GetResources returns the Resources field if non-nil, zero value otherwise.

### GetResourcesOk

`func (o *ProjectChildCounts) GetResourcesOk() (*int32, bool)`

GetResourcesOk returns a tuple with the Resources field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResources

`func (o *ProjectChildCounts) SetResources(v int32)`

SetResources sets Resources field to given value.


### GetNodes

`func (o *ProjectChildCounts) GetNodes() int32`

GetNodes returns the Nodes field if non-nil, zero value otherwise.

### GetNodesOk

`func (o *ProjectChildCounts) GetNodesOk() (*int32, bool)`

GetNodesOk returns a tuple with the Nodes field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNodes

`func (o *ProjectChildCounts) SetNodes(v int32)`

SetNodes sets Nodes field to given value.


### GetRelationTuples

`func (o *ProjectChildCounts) GetRelationTuples() int32`

GetRelationTuples returns the RelationTuples field if non-nil, zero value otherwise.

### GetRelationTuplesOk

`func (o *ProjectChildCounts) GetRelationTuplesOk() (*int32, bool)`

GetRelationTuplesOk returns a tuple with the RelationTuples field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRelationTuples

`func (o *ProjectChildCounts) SetRelationTuples(v int32)`

SetRelationTuples sets RelationTuples field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


