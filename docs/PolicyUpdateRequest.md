# PolicyUpdateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DisplayName** | Pointer to **string** |  | [optional] 
**Selector** | Pointer to [**PolicySelector**](PolicySelector.md) |  | [optional] 
**Rules** | Pointer to [**[]PolicyRule**](PolicyRule.md) |  | [optional] 
**ExpectedRevisionId** | Pointer to **string** | Revision identifier the client believes is current. When present, the PATCH only succeeds if the persisted head still matches; otherwise the call surfaces as &#x60;409 revision_conflict&#x60;.  | [optional] 

## Methods

### NewPolicyUpdateRequest

`func NewPolicyUpdateRequest() *PolicyUpdateRequest`

NewPolicyUpdateRequest instantiates a new PolicyUpdateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewPolicyUpdateRequestWithDefaults

`func NewPolicyUpdateRequestWithDefaults() *PolicyUpdateRequest`

NewPolicyUpdateRequestWithDefaults instantiates a new PolicyUpdateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDisplayName

`func (o *PolicyUpdateRequest) GetDisplayName() string`

GetDisplayName returns the DisplayName field if non-nil, zero value otherwise.

### GetDisplayNameOk

`func (o *PolicyUpdateRequest) GetDisplayNameOk() (*string, bool)`

GetDisplayNameOk returns a tuple with the DisplayName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisplayName

`func (o *PolicyUpdateRequest) SetDisplayName(v string)`

SetDisplayName sets DisplayName field to given value.

### HasDisplayName

`func (o *PolicyUpdateRequest) HasDisplayName() bool`

HasDisplayName returns a boolean if a field has been set.

### GetSelector

`func (o *PolicyUpdateRequest) GetSelector() PolicySelector`

GetSelector returns the Selector field if non-nil, zero value otherwise.

### GetSelectorOk

`func (o *PolicyUpdateRequest) GetSelectorOk() (*PolicySelector, bool)`

GetSelectorOk returns a tuple with the Selector field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSelector

`func (o *PolicyUpdateRequest) SetSelector(v PolicySelector)`

SetSelector sets Selector field to given value.

### HasSelector

`func (o *PolicyUpdateRequest) HasSelector() bool`

HasSelector returns a boolean if a field has been set.

### GetRules

`func (o *PolicyUpdateRequest) GetRules() []PolicyRule`

GetRules returns the Rules field if non-nil, zero value otherwise.

### GetRulesOk

`func (o *PolicyUpdateRequest) GetRulesOk() (*[]PolicyRule, bool)`

GetRulesOk returns a tuple with the Rules field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRules

`func (o *PolicyUpdateRequest) SetRules(v []PolicyRule)`

SetRules sets Rules field to given value.

### HasRules

`func (o *PolicyUpdateRequest) HasRules() bool`

HasRules returns a boolean if a field has been set.

### GetExpectedRevisionId

`func (o *PolicyUpdateRequest) GetExpectedRevisionId() string`

GetExpectedRevisionId returns the ExpectedRevisionId field if non-nil, zero value otherwise.

### GetExpectedRevisionIdOk

`func (o *PolicyUpdateRequest) GetExpectedRevisionIdOk() (*string, bool)`

GetExpectedRevisionIdOk returns a tuple with the ExpectedRevisionId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExpectedRevisionId

`func (o *PolicyUpdateRequest) SetExpectedRevisionId(v string)`

SetExpectedRevisionId sets ExpectedRevisionId field to given value.

### HasExpectedRevisionId

`func (o *PolicyUpdateRequest) HasExpectedRevisionId() bool`

HasExpectedRevisionId returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


