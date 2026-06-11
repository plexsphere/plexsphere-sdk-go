# RebacCheckRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Subject** | **string** | Object reference of the subject performing the check (e.g. &#x60;user:0190a8b8-...&#x60;, &#x60;service-identity:...&#x60;).  | 
**Relation** | **string** | Relation name to evaluate (e.g. &#x60;read&#x60;, &#x60;manage&#x60;, &#x60;maintainer&#x60;). The accepted set is fixed by the schema in &#x60;schema/authz.zed&#x60;.  | 
**Resource** | **string** | Object reference of the resource the relation is evaluated against (e.g. &#x60;project:0190a8b8-...&#x60;, &#x60;domain:...&#x60;).  | 
**CaveatContext** | Pointer to **map[string]interface{}** | Optional set of caveat field NAMES the request makes available to the caveat program. Values are never carried across the contract boundary; the field type is &#x60;object&#x60; for forward-compatibility but the contract requires NAMES-only payloads.  | [optional] 

## Methods

### NewRebacCheckRequest

`func NewRebacCheckRequest(subject string, relation string, resource string, ) *RebacCheckRequest`

NewRebacCheckRequest instantiates a new RebacCheckRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewRebacCheckRequestWithDefaults

`func NewRebacCheckRequestWithDefaults() *RebacCheckRequest`

NewRebacCheckRequestWithDefaults instantiates a new RebacCheckRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSubject

`func (o *RebacCheckRequest) GetSubject() string`

GetSubject returns the Subject field if non-nil, zero value otherwise.

### GetSubjectOk

`func (o *RebacCheckRequest) GetSubjectOk() (*string, bool)`

GetSubjectOk returns a tuple with the Subject field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubject

`func (o *RebacCheckRequest) SetSubject(v string)`

SetSubject sets Subject field to given value.


### GetRelation

`func (o *RebacCheckRequest) GetRelation() string`

GetRelation returns the Relation field if non-nil, zero value otherwise.

### GetRelationOk

`func (o *RebacCheckRequest) GetRelationOk() (*string, bool)`

GetRelationOk returns a tuple with the Relation field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRelation

`func (o *RebacCheckRequest) SetRelation(v string)`

SetRelation sets Relation field to given value.


### GetResource

`func (o *RebacCheckRequest) GetResource() string`

GetResource returns the Resource field if non-nil, zero value otherwise.

### GetResourceOk

`func (o *RebacCheckRequest) GetResourceOk() (*string, bool)`

GetResourceOk returns a tuple with the Resource field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResource

`func (o *RebacCheckRequest) SetResource(v string)`

SetResource sets Resource field to given value.


### GetCaveatContext

`func (o *RebacCheckRequest) GetCaveatContext() map[string]interface{}`

GetCaveatContext returns the CaveatContext field if non-nil, zero value otherwise.

### GetCaveatContextOk

`func (o *RebacCheckRequest) GetCaveatContextOk() (*map[string]interface{}, bool)`

GetCaveatContextOk returns a tuple with the CaveatContext field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCaveatContext

`func (o *RebacCheckRequest) SetCaveatContext(v map[string]interface{})`

SetCaveatContext sets CaveatContext field to given value.

### HasCaveatContext

`func (o *RebacCheckRequest) HasCaveatContext() bool`

HasCaveatContext returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


