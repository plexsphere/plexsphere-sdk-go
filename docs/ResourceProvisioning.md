# ResourceProvisioning

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Phase** | [**ProvisionedResourcePhase**](ProvisionedResourcePhase.md) |  | 
**ProvisionedResourceId** | **string** | Identifier of the broker-owned ProvisionedResource bound to this Resource (UUIDv7).  | 

## Methods

### NewResourceProvisioning

`func NewResourceProvisioning(phase ProvisionedResourcePhase, provisionedResourceId string, ) *ResourceProvisioning`

NewResourceProvisioning instantiates a new ResourceProvisioning object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewResourceProvisioningWithDefaults

`func NewResourceProvisioningWithDefaults() *ResourceProvisioning`

NewResourceProvisioningWithDefaults instantiates a new ResourceProvisioning object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetPhase

`func (o *ResourceProvisioning) GetPhase() ProvisionedResourcePhase`

GetPhase returns the Phase field if non-nil, zero value otherwise.

### GetPhaseOk

`func (o *ResourceProvisioning) GetPhaseOk() (*ProvisionedResourcePhase, bool)`

GetPhaseOk returns a tuple with the Phase field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPhase

`func (o *ResourceProvisioning) SetPhase(v ProvisionedResourcePhase)`

SetPhase sets Phase field to given value.


### GetProvisionedResourceId

`func (o *ResourceProvisioning) GetProvisionedResourceId() string`

GetProvisionedResourceId returns the ProvisionedResourceId field if non-nil, zero value otherwise.

### GetProvisionedResourceIdOk

`func (o *ResourceProvisioning) GetProvisionedResourceIdOk() (*string, bool)`

GetProvisionedResourceIdOk returns a tuple with the ProvisionedResourceId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProvisionedResourceId

`func (o *ResourceProvisioning) SetProvisionedResourceId(v string)`

SetProvisionedResourceId sets ProvisionedResourceId field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


