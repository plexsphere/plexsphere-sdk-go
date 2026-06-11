# PolicyRevision

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Revision identifier (UUIDv7). | 
**PolicyId** | **string** | Parent Policy identifier. | 
**ParentId** | Pointer to **string** | Predecessor revision identifier. &#x60;null&#x60; on the initial revision of a fresh Policy; non-null on every subsequent revision.  | [optional] 
**Selector** | [**PolicySelector**](PolicySelector.md) |  | 
**Rules** | [**[]PolicyRule**](PolicyRule.md) | Ordered rule list at this revision. Capped at 1024 entries by the aggregate; the cap is mirrored as a CHECK constraint in the persistence layer so a wire-level oversize is rejected before it reaches the editor.  | 
**CreatedAt** | **time.Time** |  | 
**CreatedBy** | **string** | Identifier of the principal that authored the revision.  | 
**CorrelationId** | Pointer to **string** | Upstream request correlation identifier propagated into the audit row and outbox event. &#x60;null&#x60; when the revision was authored outside an inbound HTTP request.  | [optional] 

## Methods

### NewPolicyRevision

`func NewPolicyRevision(id string, policyId string, selector PolicySelector, rules []PolicyRule, createdAt time.Time, createdBy string, ) *PolicyRevision`

NewPolicyRevision instantiates a new PolicyRevision object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewPolicyRevisionWithDefaults

`func NewPolicyRevisionWithDefaults() *PolicyRevision`

NewPolicyRevisionWithDefaults instantiates a new PolicyRevision object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *PolicyRevision) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *PolicyRevision) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *PolicyRevision) SetId(v string)`

SetId sets Id field to given value.


### GetPolicyId

`func (o *PolicyRevision) GetPolicyId() string`

GetPolicyId returns the PolicyId field if non-nil, zero value otherwise.

### GetPolicyIdOk

`func (o *PolicyRevision) GetPolicyIdOk() (*string, bool)`

GetPolicyIdOk returns a tuple with the PolicyId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPolicyId

`func (o *PolicyRevision) SetPolicyId(v string)`

SetPolicyId sets PolicyId field to given value.


### GetParentId

`func (o *PolicyRevision) GetParentId() string`

GetParentId returns the ParentId field if non-nil, zero value otherwise.

### GetParentIdOk

`func (o *PolicyRevision) GetParentIdOk() (*string, bool)`

GetParentIdOk returns a tuple with the ParentId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetParentId

`func (o *PolicyRevision) SetParentId(v string)`

SetParentId sets ParentId field to given value.

### HasParentId

`func (o *PolicyRevision) HasParentId() bool`

HasParentId returns a boolean if a field has been set.

### GetSelector

`func (o *PolicyRevision) GetSelector() PolicySelector`

GetSelector returns the Selector field if non-nil, zero value otherwise.

### GetSelectorOk

`func (o *PolicyRevision) GetSelectorOk() (*PolicySelector, bool)`

GetSelectorOk returns a tuple with the Selector field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSelector

`func (o *PolicyRevision) SetSelector(v PolicySelector)`

SetSelector sets Selector field to given value.


### GetRules

`func (o *PolicyRevision) GetRules() []PolicyRule`

GetRules returns the Rules field if non-nil, zero value otherwise.

### GetRulesOk

`func (o *PolicyRevision) GetRulesOk() (*[]PolicyRule, bool)`

GetRulesOk returns a tuple with the Rules field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRules

`func (o *PolicyRevision) SetRules(v []PolicyRule)`

SetRules sets Rules field to given value.


### GetCreatedAt

`func (o *PolicyRevision) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *PolicyRevision) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *PolicyRevision) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetCreatedBy

`func (o *PolicyRevision) GetCreatedBy() string`

GetCreatedBy returns the CreatedBy field if non-nil, zero value otherwise.

### GetCreatedByOk

`func (o *PolicyRevision) GetCreatedByOk() (*string, bool)`

GetCreatedByOk returns a tuple with the CreatedBy field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedBy

`func (o *PolicyRevision) SetCreatedBy(v string)`

SetCreatedBy sets CreatedBy field to given value.


### GetCorrelationId

`func (o *PolicyRevision) GetCorrelationId() string`

GetCorrelationId returns the CorrelationId field if non-nil, zero value otherwise.

### GetCorrelationIdOk

`func (o *PolicyRevision) GetCorrelationIdOk() (*string, bool)`

GetCorrelationIdOk returns a tuple with the CorrelationId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCorrelationId

`func (o *PolicyRevision) SetCorrelationId(v string)`

SetCorrelationId sets CorrelationId field to given value.

### HasCorrelationId

`func (o *PolicyRevision) HasCorrelationId() bool`

HasCorrelationId returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


