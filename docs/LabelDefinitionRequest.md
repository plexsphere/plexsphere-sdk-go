# LabelDefinitionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Scope** | [**LabelDefinitionRequestScope**](LabelDefinitionRequestScope.md) |  | 
**ScopeId** | Pointer to **string** | Tenancy identifier. Required when &#x60;scope&#x60; is &#x60;domain&#x60; or &#x60;project&#x60;; omitted when &#x60;scope&#x3D;platform&#x60;.  | [optional] 
**LocalKey** | **string** | Unqualified key token — lowercase letters, digits, &#x60;.&#x60;, &#x60;_&#x60;, &#x60;-&#x60;; 1–64 characters; no leading or trailing separator.  | 
**Description** | Pointer to **string** |  | [optional] 
**ValueSchema** | [**LabelValueSchema**](LabelValueSchema.md) |  | 
**ApplicableKinds** | **[]string** |  | 
**Required** | Pointer to **bool** | When &#x60;true&#x60;, Assignments of this Definition are mandatory on every object of the applicable kinds.  | [optional] 
**DefaultValue** | Pointer to **interface{}** |  | [optional] 
**Immutable** | Pointer to **bool** |  | [optional] 
**CloudTagPropagation** | Pointer to **bool** |  | [optional] 
**OnDelete** | Pointer to [**LabelDefinitionRequestOnDelete**](LabelDefinitionRequestOnDelete.md) |  | [optional] 
**Cardinality** | Pointer to **int32** | Declared per-object cardinality cap for Assignments of this Definition. Defaults to &#x60;1&#x60; when omitted .  | [optional] 

## Methods

### NewLabelDefinitionRequest

`func NewLabelDefinitionRequest(scope LabelDefinitionRequestScope, localKey string, valueSchema LabelValueSchema, applicableKinds []string, ) *LabelDefinitionRequest`

NewLabelDefinitionRequest instantiates a new LabelDefinitionRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewLabelDefinitionRequestWithDefaults

`func NewLabelDefinitionRequestWithDefaults() *LabelDefinitionRequest`

NewLabelDefinitionRequestWithDefaults instantiates a new LabelDefinitionRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetScope

`func (o *LabelDefinitionRequest) GetScope() LabelDefinitionRequestScope`

GetScope returns the Scope field if non-nil, zero value otherwise.

### GetScopeOk

`func (o *LabelDefinitionRequest) GetScopeOk() (*LabelDefinitionRequestScope, bool)`

GetScopeOk returns a tuple with the Scope field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetScope

`func (o *LabelDefinitionRequest) SetScope(v LabelDefinitionRequestScope)`

SetScope sets Scope field to given value.


### GetScopeId

`func (o *LabelDefinitionRequest) GetScopeId() string`

GetScopeId returns the ScopeId field if non-nil, zero value otherwise.

### GetScopeIdOk

`func (o *LabelDefinitionRequest) GetScopeIdOk() (*string, bool)`

GetScopeIdOk returns a tuple with the ScopeId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetScopeId

`func (o *LabelDefinitionRequest) SetScopeId(v string)`

SetScopeId sets ScopeId field to given value.

### HasScopeId

`func (o *LabelDefinitionRequest) HasScopeId() bool`

HasScopeId returns a boolean if a field has been set.

### GetLocalKey

`func (o *LabelDefinitionRequest) GetLocalKey() string`

GetLocalKey returns the LocalKey field if non-nil, zero value otherwise.

### GetLocalKeyOk

`func (o *LabelDefinitionRequest) GetLocalKeyOk() (*string, bool)`

GetLocalKeyOk returns a tuple with the LocalKey field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLocalKey

`func (o *LabelDefinitionRequest) SetLocalKey(v string)`

SetLocalKey sets LocalKey field to given value.


### GetDescription

`func (o *LabelDefinitionRequest) GetDescription() string`

GetDescription returns the Description field if non-nil, zero value otherwise.

### GetDescriptionOk

`func (o *LabelDefinitionRequest) GetDescriptionOk() (*string, bool)`

GetDescriptionOk returns a tuple with the Description field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDescription

`func (o *LabelDefinitionRequest) SetDescription(v string)`

SetDescription sets Description field to given value.

### HasDescription

`func (o *LabelDefinitionRequest) HasDescription() bool`

HasDescription returns a boolean if a field has been set.

### GetValueSchema

`func (o *LabelDefinitionRequest) GetValueSchema() LabelValueSchema`

GetValueSchema returns the ValueSchema field if non-nil, zero value otherwise.

### GetValueSchemaOk

`func (o *LabelDefinitionRequest) GetValueSchemaOk() (*LabelValueSchema, bool)`

GetValueSchemaOk returns a tuple with the ValueSchema field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetValueSchema

`func (o *LabelDefinitionRequest) SetValueSchema(v LabelValueSchema)`

SetValueSchema sets ValueSchema field to given value.


### GetApplicableKinds

`func (o *LabelDefinitionRequest) GetApplicableKinds() []string`

GetApplicableKinds returns the ApplicableKinds field if non-nil, zero value otherwise.

### GetApplicableKindsOk

`func (o *LabelDefinitionRequest) GetApplicableKindsOk() (*[]string, bool)`

GetApplicableKindsOk returns a tuple with the ApplicableKinds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetApplicableKinds

`func (o *LabelDefinitionRequest) SetApplicableKinds(v []string)`

SetApplicableKinds sets ApplicableKinds field to given value.


### GetRequired

`func (o *LabelDefinitionRequest) GetRequired() bool`

GetRequired returns the Required field if non-nil, zero value otherwise.

### GetRequiredOk

`func (o *LabelDefinitionRequest) GetRequiredOk() (*bool, bool)`

GetRequiredOk returns a tuple with the Required field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRequired

`func (o *LabelDefinitionRequest) SetRequired(v bool)`

SetRequired sets Required field to given value.

### HasRequired

`func (o *LabelDefinitionRequest) HasRequired() bool`

HasRequired returns a boolean if a field has been set.

### GetDefaultValue

`func (o *LabelDefinitionRequest) GetDefaultValue() interface{}`

GetDefaultValue returns the DefaultValue field if non-nil, zero value otherwise.

### GetDefaultValueOk

`func (o *LabelDefinitionRequest) GetDefaultValueOk() (*interface{}, bool)`

GetDefaultValueOk returns a tuple with the DefaultValue field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDefaultValue

`func (o *LabelDefinitionRequest) SetDefaultValue(v interface{})`

SetDefaultValue sets DefaultValue field to given value.

### HasDefaultValue

`func (o *LabelDefinitionRequest) HasDefaultValue() bool`

HasDefaultValue returns a boolean if a field has been set.

### SetDefaultValueNil

`func (o *LabelDefinitionRequest) SetDefaultValueNil(b bool)`

 SetDefaultValueNil sets the value for DefaultValue to be an explicit nil

### UnsetDefaultValue
`func (o *LabelDefinitionRequest) UnsetDefaultValue()`

UnsetDefaultValue ensures that no value is present for DefaultValue, not even an explicit nil
### GetImmutable

`func (o *LabelDefinitionRequest) GetImmutable() bool`

GetImmutable returns the Immutable field if non-nil, zero value otherwise.

### GetImmutableOk

`func (o *LabelDefinitionRequest) GetImmutableOk() (*bool, bool)`

GetImmutableOk returns a tuple with the Immutable field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetImmutable

`func (o *LabelDefinitionRequest) SetImmutable(v bool)`

SetImmutable sets Immutable field to given value.

### HasImmutable

`func (o *LabelDefinitionRequest) HasImmutable() bool`

HasImmutable returns a boolean if a field has been set.

### GetCloudTagPropagation

`func (o *LabelDefinitionRequest) GetCloudTagPropagation() bool`

GetCloudTagPropagation returns the CloudTagPropagation field if non-nil, zero value otherwise.

### GetCloudTagPropagationOk

`func (o *LabelDefinitionRequest) GetCloudTagPropagationOk() (*bool, bool)`

GetCloudTagPropagationOk returns a tuple with the CloudTagPropagation field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCloudTagPropagation

`func (o *LabelDefinitionRequest) SetCloudTagPropagation(v bool)`

SetCloudTagPropagation sets CloudTagPropagation field to given value.

### HasCloudTagPropagation

`func (o *LabelDefinitionRequest) HasCloudTagPropagation() bool`

HasCloudTagPropagation returns a boolean if a field has been set.

### GetOnDelete

`func (o *LabelDefinitionRequest) GetOnDelete() LabelDefinitionRequestOnDelete`

GetOnDelete returns the OnDelete field if non-nil, zero value otherwise.

### GetOnDeleteOk

`func (o *LabelDefinitionRequest) GetOnDeleteOk() (*LabelDefinitionRequestOnDelete, bool)`

GetOnDeleteOk returns a tuple with the OnDelete field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOnDelete

`func (o *LabelDefinitionRequest) SetOnDelete(v LabelDefinitionRequestOnDelete)`

SetOnDelete sets OnDelete field to given value.

### HasOnDelete

`func (o *LabelDefinitionRequest) HasOnDelete() bool`

HasOnDelete returns a boolean if a field has been set.

### GetCardinality

`func (o *LabelDefinitionRequest) GetCardinality() int32`

GetCardinality returns the Cardinality field if non-nil, zero value otherwise.

### GetCardinalityOk

`func (o *LabelDefinitionRequest) GetCardinalityOk() (*int32, bool)`

GetCardinalityOk returns a tuple with the Cardinality field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCardinality

`func (o *LabelDefinitionRequest) SetCardinality(v int32)`

SetCardinality sets Cardinality field to given value.

### HasCardinality

`func (o *LabelDefinitionRequest) HasCardinality() bool`

HasCardinality returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


