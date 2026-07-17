# ObjectSearchRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Selector** | **string** | Raw label-selector expression (for example &#x60;env&#x3D;production, tier in (gold, silver)&#x60;). Parsed by the same grammar /v1/labels/selectors/preview validates.  | 
**Relation** | **string** | ReBAC relation the caller must hold on a match for it to appear in the result (for example &#x60;read&#x60;). Required; clients commonly default it to &#x60;read&#x60;.  | 
**Scope** | [**ObjectSearchRequestScope**](ObjectSearchRequestScope.md) |  | 
**ScopeId** | Pointer to **string** | Domain or Project UUID addressed by &#x60;scope&#x60;. Required when &#x60;scope&#x60; is &#x60;domain&#x60; or &#x60;project&#x60;; MUST be omitted (or the zero UUID) when &#x60;scope&#x60; is &#x60;platform&#x60;.  | [optional] 
**Kind** | Pointer to **string** | Optional object-kind filter (for example &#x60;project&#x60; or &#x60;node&#x60;). When set, only matches of that kind are returned; when omitted the result is mixed-kind.  | [optional] 
**Cursor** | Pointer to **string** | Opaque forward cursor from a previous page&#39;s &#x60;next_cursor&#x60;. Omit (or send empty) to read the first page.  | [optional] 
**Limit** | Pointer to **int32** | Upper bound on the PRE-filter page size. Because the ReBAC filter runs after pagination, the returned page may hold fewer items than &#x60;limit&#x60;; paginate until &#x60;next_cursor&#x60; is absent. Omitted defers to the server default.  | [optional] 

## Methods

### NewObjectSearchRequest

`func NewObjectSearchRequest(selector string, relation string, scope ObjectSearchRequestScope, ) *ObjectSearchRequest`

NewObjectSearchRequest instantiates a new ObjectSearchRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewObjectSearchRequestWithDefaults

`func NewObjectSearchRequestWithDefaults() *ObjectSearchRequest`

NewObjectSearchRequestWithDefaults instantiates a new ObjectSearchRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSelector

`func (o *ObjectSearchRequest) GetSelector() string`

GetSelector returns the Selector field if non-nil, zero value otherwise.

### GetSelectorOk

`func (o *ObjectSearchRequest) GetSelectorOk() (*string, bool)`

GetSelectorOk returns a tuple with the Selector field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSelector

`func (o *ObjectSearchRequest) SetSelector(v string)`

SetSelector sets Selector field to given value.


### GetRelation

`func (o *ObjectSearchRequest) GetRelation() string`

GetRelation returns the Relation field if non-nil, zero value otherwise.

### GetRelationOk

`func (o *ObjectSearchRequest) GetRelationOk() (*string, bool)`

GetRelationOk returns a tuple with the Relation field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRelation

`func (o *ObjectSearchRequest) SetRelation(v string)`

SetRelation sets Relation field to given value.


### GetScope

`func (o *ObjectSearchRequest) GetScope() ObjectSearchRequestScope`

GetScope returns the Scope field if non-nil, zero value otherwise.

### GetScopeOk

`func (o *ObjectSearchRequest) GetScopeOk() (*ObjectSearchRequestScope, bool)`

GetScopeOk returns a tuple with the Scope field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetScope

`func (o *ObjectSearchRequest) SetScope(v ObjectSearchRequestScope)`

SetScope sets Scope field to given value.


### GetScopeId

`func (o *ObjectSearchRequest) GetScopeId() string`

GetScopeId returns the ScopeId field if non-nil, zero value otherwise.

### GetScopeIdOk

`func (o *ObjectSearchRequest) GetScopeIdOk() (*string, bool)`

GetScopeIdOk returns a tuple with the ScopeId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetScopeId

`func (o *ObjectSearchRequest) SetScopeId(v string)`

SetScopeId sets ScopeId field to given value.

### HasScopeId

`func (o *ObjectSearchRequest) HasScopeId() bool`

HasScopeId returns a boolean if a field has been set.

### GetKind

`func (o *ObjectSearchRequest) GetKind() string`

GetKind returns the Kind field if non-nil, zero value otherwise.

### GetKindOk

`func (o *ObjectSearchRequest) GetKindOk() (*string, bool)`

GetKindOk returns a tuple with the Kind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKind

`func (o *ObjectSearchRequest) SetKind(v string)`

SetKind sets Kind field to given value.

### HasKind

`func (o *ObjectSearchRequest) HasKind() bool`

HasKind returns a boolean if a field has been set.

### GetCursor

`func (o *ObjectSearchRequest) GetCursor() string`

GetCursor returns the Cursor field if non-nil, zero value otherwise.

### GetCursorOk

`func (o *ObjectSearchRequest) GetCursorOk() (*string, bool)`

GetCursorOk returns a tuple with the Cursor field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCursor

`func (o *ObjectSearchRequest) SetCursor(v string)`

SetCursor sets Cursor field to given value.

### HasCursor

`func (o *ObjectSearchRequest) HasCursor() bool`

HasCursor returns a boolean if a field has been set.

### GetLimit

`func (o *ObjectSearchRequest) GetLimit() int32`

GetLimit returns the Limit field if non-nil, zero value otherwise.

### GetLimitOk

`func (o *ObjectSearchRequest) GetLimitOk() (*int32, bool)`

GetLimitOk returns a tuple with the Limit field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLimit

`func (o *ObjectSearchRequest) SetLimit(v int32)`

SetLimit sets Limit field to given value.

### HasLimit

`func (o *ObjectSearchRequest) HasLimit() bool`

HasLimit returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


