# BuiltinActionParameter

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Parameter identifier as the action expects it in a dispatch&#39;s &#x60;parameters&#x60; object. Non-empty after trimming whitespace; a violation surfaces as 422 &#x60;builtin_action_invalid&#x60;.  | 
**Type** | Pointer to **string** | Optional agent-reported type name (e.g. &#x60;string&#x60;, &#x60;int&#x60;, &#x60;duration&#x60;). Free-form and recorded verbatim — see the schema description for why it is not an enum.  | [optional] 
**Required** | Pointer to **bool** | Whether the agent reports the parameter as mandatory. Descriptive only; dispatch is not gated on it.  | [optional] [default to false]
**Default** | Pointer to **string** | Optional default value the agent applies when the parameter is omitted, rendered as the agent reported it.  | [optional] 
**Description** | Pointer to **string** | Optional human-readable summary of the parameter.  | [optional] 

## Methods

### NewBuiltinActionParameter

`func NewBuiltinActionParameter(name string, ) *BuiltinActionParameter`

NewBuiltinActionParameter instantiates a new BuiltinActionParameter object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBuiltinActionParameterWithDefaults

`func NewBuiltinActionParameterWithDefaults() *BuiltinActionParameter`

NewBuiltinActionParameterWithDefaults instantiates a new BuiltinActionParameter object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetName

`func (o *BuiltinActionParameter) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *BuiltinActionParameter) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *BuiltinActionParameter) SetName(v string)`

SetName sets Name field to given value.


### GetType

`func (o *BuiltinActionParameter) GetType() string`

GetType returns the Type field if non-nil, zero value otherwise.

### GetTypeOk

`func (o *BuiltinActionParameter) GetTypeOk() (*string, bool)`

GetTypeOk returns a tuple with the Type field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetType

`func (o *BuiltinActionParameter) SetType(v string)`

SetType sets Type field to given value.

### HasType

`func (o *BuiltinActionParameter) HasType() bool`

HasType returns a boolean if a field has been set.

### GetRequired

`func (o *BuiltinActionParameter) GetRequired() bool`

GetRequired returns the Required field if non-nil, zero value otherwise.

### GetRequiredOk

`func (o *BuiltinActionParameter) GetRequiredOk() (*bool, bool)`

GetRequiredOk returns a tuple with the Required field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRequired

`func (o *BuiltinActionParameter) SetRequired(v bool)`

SetRequired sets Required field to given value.

### HasRequired

`func (o *BuiltinActionParameter) HasRequired() bool`

HasRequired returns a boolean if a field has been set.

### GetDefault

`func (o *BuiltinActionParameter) GetDefault() string`

GetDefault returns the Default field if non-nil, zero value otherwise.

### GetDefaultOk

`func (o *BuiltinActionParameter) GetDefaultOk() (*string, bool)`

GetDefaultOk returns a tuple with the Default field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDefault

`func (o *BuiltinActionParameter) SetDefault(v string)`

SetDefault sets Default field to given value.

### HasDefault

`func (o *BuiltinActionParameter) HasDefault() bool`

HasDefault returns a boolean if a field has been set.

### GetDescription

`func (o *BuiltinActionParameter) GetDescription() string`

GetDescription returns the Description field if non-nil, zero value otherwise.

### GetDescriptionOk

`func (o *BuiltinActionParameter) GetDescriptionOk() (*string, bool)`

GetDescriptionOk returns a tuple with the Description field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDescription

`func (o *BuiltinActionParameter) SetDescription(v string)`

SetDescription sets Description field to given value.

### HasDescription

`func (o *BuiltinActionParameter) HasDescription() bool`

HasDescription returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


