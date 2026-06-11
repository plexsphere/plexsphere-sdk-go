# PolicyCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Slug** | **string** |  | 
**DisplayName** | Pointer to **string** |  | [optional] 
**Selector** | [**PolicySelector**](PolicySelector.md) |  | 
**Rules** | [**[]PolicyRule**](PolicyRule.md) |  | 

## Methods

### NewPolicyCreateRequest

`func NewPolicyCreateRequest(slug string, selector PolicySelector, rules []PolicyRule, ) *PolicyCreateRequest`

NewPolicyCreateRequest instantiates a new PolicyCreateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewPolicyCreateRequestWithDefaults

`func NewPolicyCreateRequestWithDefaults() *PolicyCreateRequest`

NewPolicyCreateRequestWithDefaults instantiates a new PolicyCreateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSlug

`func (o *PolicyCreateRequest) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *PolicyCreateRequest) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *PolicyCreateRequest) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetDisplayName

`func (o *PolicyCreateRequest) GetDisplayName() string`

GetDisplayName returns the DisplayName field if non-nil, zero value otherwise.

### GetDisplayNameOk

`func (o *PolicyCreateRequest) GetDisplayNameOk() (*string, bool)`

GetDisplayNameOk returns a tuple with the DisplayName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisplayName

`func (o *PolicyCreateRequest) SetDisplayName(v string)`

SetDisplayName sets DisplayName field to given value.

### HasDisplayName

`func (o *PolicyCreateRequest) HasDisplayName() bool`

HasDisplayName returns a boolean if a field has been set.

### GetSelector

`func (o *PolicyCreateRequest) GetSelector() PolicySelector`

GetSelector returns the Selector field if non-nil, zero value otherwise.

### GetSelectorOk

`func (o *PolicyCreateRequest) GetSelectorOk() (*PolicySelector, bool)`

GetSelectorOk returns a tuple with the Selector field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSelector

`func (o *PolicyCreateRequest) SetSelector(v PolicySelector)`

SetSelector sets Selector field to given value.


### GetRules

`func (o *PolicyCreateRequest) GetRules() []PolicyRule`

GetRules returns the Rules field if non-nil, zero value otherwise.

### GetRulesOk

`func (o *PolicyCreateRequest) GetRulesOk() (*[]PolicyRule, bool)`

GetRulesOk returns a tuple with the Rules field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRules

`func (o *PolicyCreateRequest) SetRules(v []PolicyRule)`

SetRules sets Rules field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


