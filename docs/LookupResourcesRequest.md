# LookupResourcesRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Subject** | **string** | Object reference of the subject whose reachable resources are enumerated (e.g. &#x60;user:0190a8b8-...&#x60;, &#x60;service-identity:...&#x60;).  | 
**Relation** | **string** | Relation name to evaluate (e.g. &#x60;read&#x60;, &#x60;manage&#x60;). The accepted set is fixed by the schema in &#x60;schema/authz.zed&#x60;.  | 
**ResourceType** | **string** | Object type whose instances are enumerated (e.g. &#x60;project&#x60;, &#x60;domain&#x60;). Returned &#x60;items&#x60; are &#x60;&lt;resource_type&gt;:&lt;id&gt;&#x60; object references.  | 
**CaveatContext** | Pointer to **map[string]interface{}** | Optional set of caveat field NAMES the request makes available to the caveat program. Values are never carried across the contract boundary; the field type is &#x60;object&#x60; for forward-compatibility but the contract requires NAMES-only payloads.  | [optional] 

## Methods

### NewLookupResourcesRequest

`func NewLookupResourcesRequest(subject string, relation string, resourceType string, ) *LookupResourcesRequest`

NewLookupResourcesRequest instantiates a new LookupResourcesRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewLookupResourcesRequestWithDefaults

`func NewLookupResourcesRequestWithDefaults() *LookupResourcesRequest`

NewLookupResourcesRequestWithDefaults instantiates a new LookupResourcesRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSubject

`func (o *LookupResourcesRequest) GetSubject() string`

GetSubject returns the Subject field if non-nil, zero value otherwise.

### GetSubjectOk

`func (o *LookupResourcesRequest) GetSubjectOk() (*string, bool)`

GetSubjectOk returns a tuple with the Subject field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubject

`func (o *LookupResourcesRequest) SetSubject(v string)`

SetSubject sets Subject field to given value.


### GetRelation

`func (o *LookupResourcesRequest) GetRelation() string`

GetRelation returns the Relation field if non-nil, zero value otherwise.

### GetRelationOk

`func (o *LookupResourcesRequest) GetRelationOk() (*string, bool)`

GetRelationOk returns a tuple with the Relation field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRelation

`func (o *LookupResourcesRequest) SetRelation(v string)`

SetRelation sets Relation field to given value.


### GetResourceType

`func (o *LookupResourcesRequest) GetResourceType() string`

GetResourceType returns the ResourceType field if non-nil, zero value otherwise.

### GetResourceTypeOk

`func (o *LookupResourcesRequest) GetResourceTypeOk() (*string, bool)`

GetResourceTypeOk returns a tuple with the ResourceType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResourceType

`func (o *LookupResourcesRequest) SetResourceType(v string)`

SetResourceType sets ResourceType field to given value.


### GetCaveatContext

`func (o *LookupResourcesRequest) GetCaveatContext() map[string]interface{}`

GetCaveatContext returns the CaveatContext field if non-nil, zero value otherwise.

### GetCaveatContextOk

`func (o *LookupResourcesRequest) GetCaveatContextOk() (*map[string]interface{}, bool)`

GetCaveatContextOk returns a tuple with the CaveatContext field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCaveatContext

`func (o *LookupResourcesRequest) SetCaveatContext(v map[string]interface{})`

SetCaveatContext sets CaveatContext field to given value.

### HasCaveatContext

`func (o *LookupResourcesRequest) HasCaveatContext() bool`

HasCaveatContext returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


