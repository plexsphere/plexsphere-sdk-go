# ProviderBundlePatchRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DisplayName** | Pointer to **string** | New human-readable bundle name. The aggregate&#39;s &#x60;Rename&#x60; mutator validates the same constraints as construction.  | [optional] 
**ProviderPackages** | Pointer to [**[]CloudProviderPackage**](CloudProviderPackage.md) | Replacement package set. The whole set is replaced rather than merged. Omit the field to leave the current set untouched. The read surfaces render the result in canonical source-ascending order.  | [optional] 
**ProviderConfigApiVersion** | Pointer to **string** | New &#x60;&lt;group&gt;/&lt;version&gt;&#x60; every declared package serves its ProviderConfig under. Patchable independently of &#x60;provider_packages&#x60;: a package bump within one provider family keeps the served group, and a family migration changes the group without touching the pins.  | [optional] 

## Methods

### NewProviderBundlePatchRequest

`func NewProviderBundlePatchRequest() *ProviderBundlePatchRequest`

NewProviderBundlePatchRequest instantiates a new ProviderBundlePatchRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewProviderBundlePatchRequestWithDefaults

`func NewProviderBundlePatchRequestWithDefaults() *ProviderBundlePatchRequest`

NewProviderBundlePatchRequestWithDefaults instantiates a new ProviderBundlePatchRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDisplayName

`func (o *ProviderBundlePatchRequest) GetDisplayName() string`

GetDisplayName returns the DisplayName field if non-nil, zero value otherwise.

### GetDisplayNameOk

`func (o *ProviderBundlePatchRequest) GetDisplayNameOk() (*string, bool)`

GetDisplayNameOk returns a tuple with the DisplayName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisplayName

`func (o *ProviderBundlePatchRequest) SetDisplayName(v string)`

SetDisplayName sets DisplayName field to given value.

### HasDisplayName

`func (o *ProviderBundlePatchRequest) HasDisplayName() bool`

HasDisplayName returns a boolean if a field has been set.

### GetProviderPackages

`func (o *ProviderBundlePatchRequest) GetProviderPackages() []CloudProviderPackage`

GetProviderPackages returns the ProviderPackages field if non-nil, zero value otherwise.

### GetProviderPackagesOk

`func (o *ProviderBundlePatchRequest) GetProviderPackagesOk() (*[]CloudProviderPackage, bool)`

GetProviderPackagesOk returns a tuple with the ProviderPackages field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderPackages

`func (o *ProviderBundlePatchRequest) SetProviderPackages(v []CloudProviderPackage)`

SetProviderPackages sets ProviderPackages field to given value.

### HasProviderPackages

`func (o *ProviderBundlePatchRequest) HasProviderPackages() bool`

HasProviderPackages returns a boolean if a field has been set.

### GetProviderConfigApiVersion

`func (o *ProviderBundlePatchRequest) GetProviderConfigApiVersion() string`

GetProviderConfigApiVersion returns the ProviderConfigApiVersion field if non-nil, zero value otherwise.

### GetProviderConfigApiVersionOk

`func (o *ProviderBundlePatchRequest) GetProviderConfigApiVersionOk() (*string, bool)`

GetProviderConfigApiVersionOk returns a tuple with the ProviderConfigApiVersion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderConfigApiVersion

`func (o *ProviderBundlePatchRequest) SetProviderConfigApiVersion(v string)`

SetProviderConfigApiVersion sets ProviderConfigApiVersion field to given value.

### HasProviderConfigApiVersion

`func (o *ProviderBundlePatchRequest) HasProviderConfigApiVersion() bool`

HasProviderConfigApiVersion returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


