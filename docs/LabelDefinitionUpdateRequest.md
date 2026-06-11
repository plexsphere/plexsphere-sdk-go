# LabelDefinitionUpdateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Description** | Pointer to **string** |  | [optional] 
**ValueSchema** | Pointer to [**LabelValueSchema**](LabelValueSchema.md) |  | [optional] 
**ApplicableKinds** | Pointer to **[]string** |  | [optional] 
**Required** | Pointer to **bool** |  | [optional] 
**DefaultValue** | Pointer to **interface{}** |  | [optional] 
**CloudTagPropagation** | Pointer to **bool** |  | [optional] 
**OnDelete** | Pointer to [**LabelDefinitionUpdateRequestOnDelete**](LabelDefinitionUpdateRequestOnDelete.md) |  | [optional] 

## Methods

### NewLabelDefinitionUpdateRequest

`func NewLabelDefinitionUpdateRequest() *LabelDefinitionUpdateRequest`

NewLabelDefinitionUpdateRequest instantiates a new LabelDefinitionUpdateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewLabelDefinitionUpdateRequestWithDefaults

`func NewLabelDefinitionUpdateRequestWithDefaults() *LabelDefinitionUpdateRequest`

NewLabelDefinitionUpdateRequestWithDefaults instantiates a new LabelDefinitionUpdateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDescription

`func (o *LabelDefinitionUpdateRequest) GetDescription() string`

GetDescription returns the Description field if non-nil, zero value otherwise.

### GetDescriptionOk

`func (o *LabelDefinitionUpdateRequest) GetDescriptionOk() (*string, bool)`

GetDescriptionOk returns a tuple with the Description field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDescription

`func (o *LabelDefinitionUpdateRequest) SetDescription(v string)`

SetDescription sets Description field to given value.

### HasDescription

`func (o *LabelDefinitionUpdateRequest) HasDescription() bool`

HasDescription returns a boolean if a field has been set.

### GetValueSchema

`func (o *LabelDefinitionUpdateRequest) GetValueSchema() LabelValueSchema`

GetValueSchema returns the ValueSchema field if non-nil, zero value otherwise.

### GetValueSchemaOk

`func (o *LabelDefinitionUpdateRequest) GetValueSchemaOk() (*LabelValueSchema, bool)`

GetValueSchemaOk returns a tuple with the ValueSchema field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetValueSchema

`func (o *LabelDefinitionUpdateRequest) SetValueSchema(v LabelValueSchema)`

SetValueSchema sets ValueSchema field to given value.

### HasValueSchema

`func (o *LabelDefinitionUpdateRequest) HasValueSchema() bool`

HasValueSchema returns a boolean if a field has been set.

### GetApplicableKinds

`func (o *LabelDefinitionUpdateRequest) GetApplicableKinds() []string`

GetApplicableKinds returns the ApplicableKinds field if non-nil, zero value otherwise.

### GetApplicableKindsOk

`func (o *LabelDefinitionUpdateRequest) GetApplicableKindsOk() (*[]string, bool)`

GetApplicableKindsOk returns a tuple with the ApplicableKinds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetApplicableKinds

`func (o *LabelDefinitionUpdateRequest) SetApplicableKinds(v []string)`

SetApplicableKinds sets ApplicableKinds field to given value.

### HasApplicableKinds

`func (o *LabelDefinitionUpdateRequest) HasApplicableKinds() bool`

HasApplicableKinds returns a boolean if a field has been set.

### GetRequired

`func (o *LabelDefinitionUpdateRequest) GetRequired() bool`

GetRequired returns the Required field if non-nil, zero value otherwise.

### GetRequiredOk

`func (o *LabelDefinitionUpdateRequest) GetRequiredOk() (*bool, bool)`

GetRequiredOk returns a tuple with the Required field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRequired

`func (o *LabelDefinitionUpdateRequest) SetRequired(v bool)`

SetRequired sets Required field to given value.

### HasRequired

`func (o *LabelDefinitionUpdateRequest) HasRequired() bool`

HasRequired returns a boolean if a field has been set.

### GetDefaultValue

`func (o *LabelDefinitionUpdateRequest) GetDefaultValue() interface{}`

GetDefaultValue returns the DefaultValue field if non-nil, zero value otherwise.

### GetDefaultValueOk

`func (o *LabelDefinitionUpdateRequest) GetDefaultValueOk() (*interface{}, bool)`

GetDefaultValueOk returns a tuple with the DefaultValue field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDefaultValue

`func (o *LabelDefinitionUpdateRequest) SetDefaultValue(v interface{})`

SetDefaultValue sets DefaultValue field to given value.

### HasDefaultValue

`func (o *LabelDefinitionUpdateRequest) HasDefaultValue() bool`

HasDefaultValue returns a boolean if a field has been set.

### SetDefaultValueNil

`func (o *LabelDefinitionUpdateRequest) SetDefaultValueNil(b bool)`

 SetDefaultValueNil sets the value for DefaultValue to be an explicit nil

### UnsetDefaultValue
`func (o *LabelDefinitionUpdateRequest) UnsetDefaultValue()`

UnsetDefaultValue ensures that no value is present for DefaultValue, not even an explicit nil
### GetCloudTagPropagation

`func (o *LabelDefinitionUpdateRequest) GetCloudTagPropagation() bool`

GetCloudTagPropagation returns the CloudTagPropagation field if non-nil, zero value otherwise.

### GetCloudTagPropagationOk

`func (o *LabelDefinitionUpdateRequest) GetCloudTagPropagationOk() (*bool, bool)`

GetCloudTagPropagationOk returns a tuple with the CloudTagPropagation field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCloudTagPropagation

`func (o *LabelDefinitionUpdateRequest) SetCloudTagPropagation(v bool)`

SetCloudTagPropagation sets CloudTagPropagation field to given value.

### HasCloudTagPropagation

`func (o *LabelDefinitionUpdateRequest) HasCloudTagPropagation() bool`

HasCloudTagPropagation returns a boolean if a field has been set.

### GetOnDelete

`func (o *LabelDefinitionUpdateRequest) GetOnDelete() LabelDefinitionUpdateRequestOnDelete`

GetOnDelete returns the OnDelete field if non-nil, zero value otherwise.

### GetOnDeleteOk

`func (o *LabelDefinitionUpdateRequest) GetOnDeleteOk() (*LabelDefinitionUpdateRequestOnDelete, bool)`

GetOnDeleteOk returns a tuple with the OnDelete field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOnDelete

`func (o *LabelDefinitionUpdateRequest) SetOnDelete(v LabelDefinitionUpdateRequestOnDelete)`

SetOnDelete sets OnDelete field to given value.

### HasOnDelete

`func (o *LabelDefinitionUpdateRequest) HasOnDelete() bool`

HasOnDelete returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


