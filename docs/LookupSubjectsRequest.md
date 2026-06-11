# LookupSubjectsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**SubjectType** | **string** | Object type whose instances are enumerated (e.g. &#x60;user&#x60;, &#x60;service-identity&#x60;). Returned &#x60;items&#x60; are &#x60;&lt;subject_type&gt;:&lt;id&gt;&#x60; object references.  | 
**Relation** | **string** | Relation name to evaluate (e.g. &#x60;read&#x60;, &#x60;manage&#x60;). The accepted set is fixed by the schema in &#x60;schema/authz.zed&#x60;.  | 
**Resource** | **string** | Object reference of the resource whose authorised subjects are enumerated (e.g. &#x60;project:0190a8b8-...&#x60;, &#x60;domain:...&#x60;).  | 
**CaveatContext** | Pointer to **map[string]interface{}** | Optional set of caveat field NAMES the request makes available to the caveat program. Values are never carried across the contract boundary; the field type is &#x60;object&#x60; for forward-compatibility but the contract requires NAMES-only payloads.  | [optional] 

## Methods

### NewLookupSubjectsRequest

`func NewLookupSubjectsRequest(subjectType string, relation string, resource string, ) *LookupSubjectsRequest`

NewLookupSubjectsRequest instantiates a new LookupSubjectsRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewLookupSubjectsRequestWithDefaults

`func NewLookupSubjectsRequestWithDefaults() *LookupSubjectsRequest`

NewLookupSubjectsRequestWithDefaults instantiates a new LookupSubjectsRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSubjectType

`func (o *LookupSubjectsRequest) GetSubjectType() string`

GetSubjectType returns the SubjectType field if non-nil, zero value otherwise.

### GetSubjectTypeOk

`func (o *LookupSubjectsRequest) GetSubjectTypeOk() (*string, bool)`

GetSubjectTypeOk returns a tuple with the SubjectType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubjectType

`func (o *LookupSubjectsRequest) SetSubjectType(v string)`

SetSubjectType sets SubjectType field to given value.


### GetRelation

`func (o *LookupSubjectsRequest) GetRelation() string`

GetRelation returns the Relation field if non-nil, zero value otherwise.

### GetRelationOk

`func (o *LookupSubjectsRequest) GetRelationOk() (*string, bool)`

GetRelationOk returns a tuple with the Relation field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRelation

`func (o *LookupSubjectsRequest) SetRelation(v string)`

SetRelation sets Relation field to given value.


### GetResource

`func (o *LookupSubjectsRequest) GetResource() string`

GetResource returns the Resource field if non-nil, zero value otherwise.

### GetResourceOk

`func (o *LookupSubjectsRequest) GetResourceOk() (*string, bool)`

GetResourceOk returns a tuple with the Resource field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResource

`func (o *LookupSubjectsRequest) SetResource(v string)`

SetResource sets Resource field to given value.


### GetCaveatContext

`func (o *LookupSubjectsRequest) GetCaveatContext() map[string]interface{}`

GetCaveatContext returns the CaveatContext field if non-nil, zero value otherwise.

### GetCaveatContextOk

`func (o *LookupSubjectsRequest) GetCaveatContextOk() (*map[string]interface{}, bool)`

GetCaveatContextOk returns a tuple with the CaveatContext field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCaveatContext

`func (o *LookupSubjectsRequest) SetCaveatContext(v map[string]interface{})`

SetCaveatContext sets CaveatContext field to given value.

### HasCaveatContext

`func (o *LookupSubjectsRequest) HasCaveatContext() bool`

HasCaveatContext returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


