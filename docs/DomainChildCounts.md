# DomainChildCounts

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Projects** | **int32** | Number of &#x60;Project&#x60; aggregates still attached. | 
**Groups** | **int32** | Number of &#x60;Group&#x60; aggregates still attached. | 
**Identities** | **int32** | Number of identities (users + service identities) still attached.  | 
**IdpBindings** | **int32** | Number of &#x60;IdPBinding&#x60; rows still attached. | 
**Nodes** | **int32** | Number of &#x60;Node&#x60; aggregates still attached. | 

## Methods

### NewDomainChildCounts

`func NewDomainChildCounts(projects int32, groups int32, identities int32, idpBindings int32, nodes int32, ) *DomainChildCounts`

NewDomainChildCounts instantiates a new DomainChildCounts object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDomainChildCountsWithDefaults

`func NewDomainChildCountsWithDefaults() *DomainChildCounts`

NewDomainChildCountsWithDefaults instantiates a new DomainChildCounts object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetProjects

`func (o *DomainChildCounts) GetProjects() int32`

GetProjects returns the Projects field if non-nil, zero value otherwise.

### GetProjectsOk

`func (o *DomainChildCounts) GetProjectsOk() (*int32, bool)`

GetProjectsOk returns a tuple with the Projects field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProjects

`func (o *DomainChildCounts) SetProjects(v int32)`

SetProjects sets Projects field to given value.


### GetGroups

`func (o *DomainChildCounts) GetGroups() int32`

GetGroups returns the Groups field if non-nil, zero value otherwise.

### GetGroupsOk

`func (o *DomainChildCounts) GetGroupsOk() (*int32, bool)`

GetGroupsOk returns a tuple with the Groups field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetGroups

`func (o *DomainChildCounts) SetGroups(v int32)`

SetGroups sets Groups field to given value.


### GetIdentities

`func (o *DomainChildCounts) GetIdentities() int32`

GetIdentities returns the Identities field if non-nil, zero value otherwise.

### GetIdentitiesOk

`func (o *DomainChildCounts) GetIdentitiesOk() (*int32, bool)`

GetIdentitiesOk returns a tuple with the Identities field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIdentities

`func (o *DomainChildCounts) SetIdentities(v int32)`

SetIdentities sets Identities field to given value.


### GetIdpBindings

`func (o *DomainChildCounts) GetIdpBindings() int32`

GetIdpBindings returns the IdpBindings field if non-nil, zero value otherwise.

### GetIdpBindingsOk

`func (o *DomainChildCounts) GetIdpBindingsOk() (*int32, bool)`

GetIdpBindingsOk returns a tuple with the IdpBindings field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIdpBindings

`func (o *DomainChildCounts) SetIdpBindings(v int32)`

SetIdpBindings sets IdpBindings field to given value.


### GetNodes

`func (o *DomainChildCounts) GetNodes() int32`

GetNodes returns the Nodes field if non-nil, zero value otherwise.

### GetNodesOk

`func (o *DomainChildCounts) GetNodesOk() (*int32, bool)`

GetNodesOk returns a tuple with the Nodes field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNodes

`func (o *DomainChildCounts) SetNodes(v int32)`

SetNodes sets Nodes field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


