# ProviderBundleCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DisplayName** | **string** | Human-readable bundle name. Whitespace-only is rejected. | 
**Slug** | **string** | Kebab-case URL handle. The aggregate&#39;s &#x60;ParseSlug&#x60; enforces the same regex; surfacing the pattern here lets the generated client validate before the round-trip.  | 
**Provider** | [**CloudProvider**](CloudProvider.md) |  | 
**ProviderPackages** | [**[]CloudProviderPackage**](CloudProviderPackage.md) | The Crossplane provider packages the bundle declares. At least one entry is required, and each &#x60;source&#x60; may appear only once. The read surfaces render the set in canonical source-ascending order, not in the order stated here.  | 
**ProviderConfigApiVersion** | **string** | The &#x60;&lt;group&gt;/&lt;version&gt;&#x60; every declared package serves its ProviderConfig under (e.g. &#x60;aws.m.upbound.io/v1beta1&#x60;).  | 

## Methods

### NewProviderBundleCreateRequest

`func NewProviderBundleCreateRequest(displayName string, slug string, provider CloudProvider, providerPackages []CloudProviderPackage, providerConfigApiVersion string, ) *ProviderBundleCreateRequest`

NewProviderBundleCreateRequest instantiates a new ProviderBundleCreateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewProviderBundleCreateRequestWithDefaults

`func NewProviderBundleCreateRequestWithDefaults() *ProviderBundleCreateRequest`

NewProviderBundleCreateRequestWithDefaults instantiates a new ProviderBundleCreateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDisplayName

`func (o *ProviderBundleCreateRequest) GetDisplayName() string`

GetDisplayName returns the DisplayName field if non-nil, zero value otherwise.

### GetDisplayNameOk

`func (o *ProviderBundleCreateRequest) GetDisplayNameOk() (*string, bool)`

GetDisplayNameOk returns a tuple with the DisplayName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisplayName

`func (o *ProviderBundleCreateRequest) SetDisplayName(v string)`

SetDisplayName sets DisplayName field to given value.


### GetSlug

`func (o *ProviderBundleCreateRequest) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *ProviderBundleCreateRequest) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *ProviderBundleCreateRequest) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetProvider

`func (o *ProviderBundleCreateRequest) GetProvider() CloudProvider`

GetProvider returns the Provider field if non-nil, zero value otherwise.

### GetProviderOk

`func (o *ProviderBundleCreateRequest) GetProviderOk() (*CloudProvider, bool)`

GetProviderOk returns a tuple with the Provider field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProvider

`func (o *ProviderBundleCreateRequest) SetProvider(v CloudProvider)`

SetProvider sets Provider field to given value.


### GetProviderPackages

`func (o *ProviderBundleCreateRequest) GetProviderPackages() []CloudProviderPackage`

GetProviderPackages returns the ProviderPackages field if non-nil, zero value otherwise.

### GetProviderPackagesOk

`func (o *ProviderBundleCreateRequest) GetProviderPackagesOk() (*[]CloudProviderPackage, bool)`

GetProviderPackagesOk returns a tuple with the ProviderPackages field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderPackages

`func (o *ProviderBundleCreateRequest) SetProviderPackages(v []CloudProviderPackage)`

SetProviderPackages sets ProviderPackages field to given value.


### GetProviderConfigApiVersion

`func (o *ProviderBundleCreateRequest) GetProviderConfigApiVersion() string`

GetProviderConfigApiVersion returns the ProviderConfigApiVersion field if non-nil, zero value otherwise.

### GetProviderConfigApiVersionOk

`func (o *ProviderBundleCreateRequest) GetProviderConfigApiVersionOk() (*string, bool)`

GetProviderConfigApiVersionOk returns a tuple with the ProviderConfigApiVersion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderConfigApiVersion

`func (o *ProviderBundleCreateRequest) SetProviderConfigApiVersion(v string)`

SetProviderConfigApiVersion sets ProviderConfigApiVersion field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


