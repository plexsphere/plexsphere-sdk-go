# BuiltinAction

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Action identifier (e.g. &#x60;diagnostics.collect&#x60;, &#x60;service.upgrade&#x60;). Non-empty after trimming whitespace; a violation surfaces as 422 &#x60;builtin_action_invalid&#x60;. Unique within one manifest — a duplicate surfaces as 422 &#x60;builtin_action_duplicate&#x60;.  | 
**Description** | Pointer to **string** | Optional human-readable summary of what the action does, shown on operator surfaces beside the action name.  | [optional] 
**Parameters** | Pointer to [**[]BuiltinActionParameter**](BuiltinActionParameter.md) | Optional list of the parameters the action accepts. Entries are ordered as the agent reported them, which is the order an operator surface should present them in. Duplicate parameter names within one action surface as 422 &#x60;builtin_action_invalid&#x60;.  | [optional] 

## Methods

### NewBuiltinAction

`func NewBuiltinAction(name string, ) *BuiltinAction`

NewBuiltinAction instantiates a new BuiltinAction object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBuiltinActionWithDefaults

`func NewBuiltinActionWithDefaults() *BuiltinAction`

NewBuiltinActionWithDefaults instantiates a new BuiltinAction object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetName

`func (o *BuiltinAction) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *BuiltinAction) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *BuiltinAction) SetName(v string)`

SetName sets Name field to given value.


### GetDescription

`func (o *BuiltinAction) GetDescription() string`

GetDescription returns the Description field if non-nil, zero value otherwise.

### GetDescriptionOk

`func (o *BuiltinAction) GetDescriptionOk() (*string, bool)`

GetDescriptionOk returns a tuple with the Description field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDescription

`func (o *BuiltinAction) SetDescription(v string)`

SetDescription sets Description field to given value.

### HasDescription

`func (o *BuiltinAction) HasDescription() bool`

HasDescription returns a boolean if a field has been set.

### GetParameters

`func (o *BuiltinAction) GetParameters() []BuiltinActionParameter`

GetParameters returns the Parameters field if non-nil, zero value otherwise.

### GetParametersOk

`func (o *BuiltinAction) GetParametersOk() (*[]BuiltinActionParameter, bool)`

GetParametersOk returns a tuple with the Parameters field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetParameters

`func (o *BuiltinAction) SetParameters(v []BuiltinActionParameter)`

SetParameters sets Parameters field to given value.

### HasParameters

`func (o *BuiltinAction) HasParameters() bool`

HasParameters returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


