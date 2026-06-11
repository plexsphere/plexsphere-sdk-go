# BlueprintParameter

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Parameter name an operator fills in at provisioning time.  | 
**Type** | [**BlueprintParameterType**](BlueprintParameterType.md) |  | 
**Required** | **bool** | Whether the operator MUST supply a value. A non-required parameter may carry a &#x60;default&#x60;.  | 
**Default** | Pointer to [**BlueprintParameterDefault**](BlueprintParameterDefault.md) |  | [optional] 

## Methods

### NewBlueprintParameter

`func NewBlueprintParameter(name string, type_ BlueprintParameterType, required bool, ) *BlueprintParameter`

NewBlueprintParameter instantiates a new BlueprintParameter object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBlueprintParameterWithDefaults

`func NewBlueprintParameterWithDefaults() *BlueprintParameter`

NewBlueprintParameterWithDefaults instantiates a new BlueprintParameter object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetName

`func (o *BlueprintParameter) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *BlueprintParameter) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *BlueprintParameter) SetName(v string)`

SetName sets Name field to given value.


### GetType

`func (o *BlueprintParameter) GetType() BlueprintParameterType`

GetType returns the Type field if non-nil, zero value otherwise.

### GetTypeOk

`func (o *BlueprintParameter) GetTypeOk() (*BlueprintParameterType, bool)`

GetTypeOk returns a tuple with the Type field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetType

`func (o *BlueprintParameter) SetType(v BlueprintParameterType)`

SetType sets Type field to given value.


### GetRequired

`func (o *BlueprintParameter) GetRequired() bool`

GetRequired returns the Required field if non-nil, zero value otherwise.

### GetRequiredOk

`func (o *BlueprintParameter) GetRequiredOk() (*bool, bool)`

GetRequiredOk returns a tuple with the Required field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRequired

`func (o *BlueprintParameter) SetRequired(v bool)`

SetRequired sets Required field to given value.


### GetDefault

`func (o *BlueprintParameter) GetDefault() BlueprintParameterDefault`

GetDefault returns the Default field if non-nil, zero value otherwise.

### GetDefaultOk

`func (o *BlueprintParameter) GetDefaultOk() (*BlueprintParameterDefault, bool)`

GetDefaultOk returns a tuple with the Default field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDefault

`func (o *BlueprintParameter) SetDefault(v BlueprintParameterDefault)`

SetDefault sets Default field to given value.

### HasDefault

`func (o *BlueprintParameter) HasDefault() bool`

HasDefault returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


