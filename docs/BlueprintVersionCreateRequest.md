# BlueprintVersionCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Version** | **string** | Version identifier, unique within the parent Blueprint. | 
**Xrd** | **map[string]interface{}** | Crossplane CompositeResourceDefinition manifest as a JSON object. Validated structurally against the Composition before any write; a malformed pair surfaces as &#x60;400 invalid_manifest&#x60;.  | 
**Composition** | **map[string]interface{}** | Crossplane Composition manifest as a JSON object. Its composite-type reference must name the composite type the XRD declares.  | 
**ParameterSchema** | **map[string]interface{}** | Typed parameter-schema document of the form &#x60;{\&quot;parameters\&quot;:[{\&quot;name\&quot;:…,\&quot;type\&quot;:…,\&quot;required\&quot;:…,\&quot;default\&quot;?:…}]}&#x60;. A structurally invalid document surfaces as &#x60;400 invalid_parameter_schema&#x60;.  | 
**ProviderKinds** | **[]string** | Closed-set infrastructure substrates this version can target, one or more of &#x60;aws&#x60;, &#x60;gcp&#x60;, &#x60;hetzner&#x60;, &#x60;openstack&#x60;. The server validates each value through the domain provider-kind parser; an out-of-set value is rejected with &#x60;400 invalid_provider_kind&#x60;. Non-empty.  | 
**InjectionStrategy** | **string** | Discriminator naming how this version threads request parameters into the rendered Composite Resource, one of &#x60;cloud-init-user-data&#x60;, &#x60;helm-values&#x60;, &#x60;provider-secret&#x60;. The server validates the value; an out-of-set value is rejected with &#x60;400 invalid_injection_strategy&#x60;.  | 

## Methods

### NewBlueprintVersionCreateRequest

`func NewBlueprintVersionCreateRequest(version string, xrd map[string]interface{}, composition map[string]interface{}, parameterSchema map[string]interface{}, providerKinds []string, injectionStrategy string, ) *BlueprintVersionCreateRequest`

NewBlueprintVersionCreateRequest instantiates a new BlueprintVersionCreateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBlueprintVersionCreateRequestWithDefaults

`func NewBlueprintVersionCreateRequestWithDefaults() *BlueprintVersionCreateRequest`

NewBlueprintVersionCreateRequestWithDefaults instantiates a new BlueprintVersionCreateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetVersion

`func (o *BlueprintVersionCreateRequest) GetVersion() string`

GetVersion returns the Version field if non-nil, zero value otherwise.

### GetVersionOk

`func (o *BlueprintVersionCreateRequest) GetVersionOk() (*string, bool)`

GetVersionOk returns a tuple with the Version field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetVersion

`func (o *BlueprintVersionCreateRequest) SetVersion(v string)`

SetVersion sets Version field to given value.


### GetXrd

`func (o *BlueprintVersionCreateRequest) GetXrd() map[string]interface{}`

GetXrd returns the Xrd field if non-nil, zero value otherwise.

### GetXrdOk

`func (o *BlueprintVersionCreateRequest) GetXrdOk() (*map[string]interface{}, bool)`

GetXrdOk returns a tuple with the Xrd field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetXrd

`func (o *BlueprintVersionCreateRequest) SetXrd(v map[string]interface{})`

SetXrd sets Xrd field to given value.


### GetComposition

`func (o *BlueprintVersionCreateRequest) GetComposition() map[string]interface{}`

GetComposition returns the Composition field if non-nil, zero value otherwise.

### GetCompositionOk

`func (o *BlueprintVersionCreateRequest) GetCompositionOk() (*map[string]interface{}, bool)`

GetCompositionOk returns a tuple with the Composition field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetComposition

`func (o *BlueprintVersionCreateRequest) SetComposition(v map[string]interface{})`

SetComposition sets Composition field to given value.


### GetParameterSchema

`func (o *BlueprintVersionCreateRequest) GetParameterSchema() map[string]interface{}`

GetParameterSchema returns the ParameterSchema field if non-nil, zero value otherwise.

### GetParameterSchemaOk

`func (o *BlueprintVersionCreateRequest) GetParameterSchemaOk() (*map[string]interface{}, bool)`

GetParameterSchemaOk returns a tuple with the ParameterSchema field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetParameterSchema

`func (o *BlueprintVersionCreateRequest) SetParameterSchema(v map[string]interface{})`

SetParameterSchema sets ParameterSchema field to given value.


### GetProviderKinds

`func (o *BlueprintVersionCreateRequest) GetProviderKinds() []string`

GetProviderKinds returns the ProviderKinds field if non-nil, zero value otherwise.

### GetProviderKindsOk

`func (o *BlueprintVersionCreateRequest) GetProviderKindsOk() (*[]string, bool)`

GetProviderKindsOk returns a tuple with the ProviderKinds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderKinds

`func (o *BlueprintVersionCreateRequest) SetProviderKinds(v []string)`

SetProviderKinds sets ProviderKinds field to given value.


### GetInjectionStrategy

`func (o *BlueprintVersionCreateRequest) GetInjectionStrategy() string`

GetInjectionStrategy returns the InjectionStrategy field if non-nil, zero value otherwise.

### GetInjectionStrategyOk

`func (o *BlueprintVersionCreateRequest) GetInjectionStrategyOk() (*string, bool)`

GetInjectionStrategyOk returns a tuple with the InjectionStrategy field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetInjectionStrategy

`func (o *BlueprintVersionCreateRequest) SetInjectionStrategy(v string)`

SetInjectionStrategy sets InjectionStrategy field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


