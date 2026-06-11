# BlueprintVersionResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Version** | **string** | Version identifier, unique within the parent Blueprint. | 
**ProviderKinds** | [**[]BlueprintVersionResponseProviderKindsInner**](BlueprintVersionResponseProviderKindsInner.md) | Closed-set infrastructure substrates this version can target. Non-empty.  | 
**InjectionStrategy** | [**BlueprintVersionResponseInjectionStrategy**](BlueprintVersionResponseInjectionStrategy.md) |  | 
**ParameterSchema** | [**[]BlueprintParameter**](BlueprintParameter.md) | Typed parameter declarations an operator fills in when provisioning a Resource from this version. May be empty when the version declares no parameters.  | 
**CreatedAt** | **time.Time** | Version creation timestamp (UTC). | 

## Methods

### NewBlueprintVersionResponse

`func NewBlueprintVersionResponse(version string, providerKinds []BlueprintVersionResponseProviderKindsInner, injectionStrategy BlueprintVersionResponseInjectionStrategy, parameterSchema []BlueprintParameter, createdAt time.Time, ) *BlueprintVersionResponse`

NewBlueprintVersionResponse instantiates a new BlueprintVersionResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBlueprintVersionResponseWithDefaults

`func NewBlueprintVersionResponseWithDefaults() *BlueprintVersionResponse`

NewBlueprintVersionResponseWithDefaults instantiates a new BlueprintVersionResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetVersion

`func (o *BlueprintVersionResponse) GetVersion() string`

GetVersion returns the Version field if non-nil, zero value otherwise.

### GetVersionOk

`func (o *BlueprintVersionResponse) GetVersionOk() (*string, bool)`

GetVersionOk returns a tuple with the Version field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetVersion

`func (o *BlueprintVersionResponse) SetVersion(v string)`

SetVersion sets Version field to given value.


### GetProviderKinds

`func (o *BlueprintVersionResponse) GetProviderKinds() []BlueprintVersionResponseProviderKindsInner`

GetProviderKinds returns the ProviderKinds field if non-nil, zero value otherwise.

### GetProviderKindsOk

`func (o *BlueprintVersionResponse) GetProviderKindsOk() (*[]BlueprintVersionResponseProviderKindsInner, bool)`

GetProviderKindsOk returns a tuple with the ProviderKinds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderKinds

`func (o *BlueprintVersionResponse) SetProviderKinds(v []BlueprintVersionResponseProviderKindsInner)`

SetProviderKinds sets ProviderKinds field to given value.


### GetInjectionStrategy

`func (o *BlueprintVersionResponse) GetInjectionStrategy() BlueprintVersionResponseInjectionStrategy`

GetInjectionStrategy returns the InjectionStrategy field if non-nil, zero value otherwise.

### GetInjectionStrategyOk

`func (o *BlueprintVersionResponse) GetInjectionStrategyOk() (*BlueprintVersionResponseInjectionStrategy, bool)`

GetInjectionStrategyOk returns a tuple with the InjectionStrategy field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetInjectionStrategy

`func (o *BlueprintVersionResponse) SetInjectionStrategy(v BlueprintVersionResponseInjectionStrategy)`

SetInjectionStrategy sets InjectionStrategy field to given value.


### GetParameterSchema

`func (o *BlueprintVersionResponse) GetParameterSchema() []BlueprintParameter`

GetParameterSchema returns the ParameterSchema field if non-nil, zero value otherwise.

### GetParameterSchemaOk

`func (o *BlueprintVersionResponse) GetParameterSchemaOk() (*[]BlueprintParameter, bool)`

GetParameterSchemaOk returns a tuple with the ParameterSchema field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetParameterSchema

`func (o *BlueprintVersionResponse) SetParameterSchema(v []BlueprintParameter)`

SetParameterSchema sets ParameterSchema field to given value.


### GetCreatedAt

`func (o *BlueprintVersionResponse) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *BlueprintVersionResponse) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *BlueprintVersionResponse) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


