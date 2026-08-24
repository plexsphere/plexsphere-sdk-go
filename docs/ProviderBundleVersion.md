# ProviderBundleVersion

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Version** | **int64** | The content version number. Numbering starts at 1 and each content patch on the bundle publishes the next one. This is the value a Cloud carries as &#x60;provider_bundle_version&#x60;.  | 
**ProviderPackages** | [**[]CloudProviderPackage**](CloudProviderPackage.md) | The Crossplane provider packages this version declares, rendered in canonical source-ascending order.  | 
**ProviderConfigApiVersion** | **string** | The &#x60;&lt;group&gt;/&lt;version&gt;&#x60; every package of this version serves its ProviderConfig under (e.g. &#x60;aws.m.upbound.io/v1beta1&#x60;).  | 
**CreatedBy** | **string** | The subject that published the version. Empty for the versions the schema migration backfilled from the bundles that existed before the history was recorded — there is no publishing principal to attribute those to.  | 
**CreatedAt** | **time.Time** | Publication timestamp of this version (UTC). | 

## Methods

### NewProviderBundleVersion

`func NewProviderBundleVersion(version int64, providerPackages []CloudProviderPackage, providerConfigApiVersion string, createdBy string, createdAt time.Time, ) *ProviderBundleVersion`

NewProviderBundleVersion instantiates a new ProviderBundleVersion object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewProviderBundleVersionWithDefaults

`func NewProviderBundleVersionWithDefaults() *ProviderBundleVersion`

NewProviderBundleVersionWithDefaults instantiates a new ProviderBundleVersion object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetVersion

`func (o *ProviderBundleVersion) GetVersion() int64`

GetVersion returns the Version field if non-nil, zero value otherwise.

### GetVersionOk

`func (o *ProviderBundleVersion) GetVersionOk() (*int64, bool)`

GetVersionOk returns a tuple with the Version field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetVersion

`func (o *ProviderBundleVersion) SetVersion(v int64)`

SetVersion sets Version field to given value.


### GetProviderPackages

`func (o *ProviderBundleVersion) GetProviderPackages() []CloudProviderPackage`

GetProviderPackages returns the ProviderPackages field if non-nil, zero value otherwise.

### GetProviderPackagesOk

`func (o *ProviderBundleVersion) GetProviderPackagesOk() (*[]CloudProviderPackage, bool)`

GetProviderPackagesOk returns a tuple with the ProviderPackages field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderPackages

`func (o *ProviderBundleVersion) SetProviderPackages(v []CloudProviderPackage)`

SetProviderPackages sets ProviderPackages field to given value.


### GetProviderConfigApiVersion

`func (o *ProviderBundleVersion) GetProviderConfigApiVersion() string`

GetProviderConfigApiVersion returns the ProviderConfigApiVersion field if non-nil, zero value otherwise.

### GetProviderConfigApiVersionOk

`func (o *ProviderBundleVersion) GetProviderConfigApiVersionOk() (*string, bool)`

GetProviderConfigApiVersionOk returns a tuple with the ProviderConfigApiVersion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderConfigApiVersion

`func (o *ProviderBundleVersion) SetProviderConfigApiVersion(v string)`

SetProviderConfigApiVersion sets ProviderConfigApiVersion field to given value.


### GetCreatedBy

`func (o *ProviderBundleVersion) GetCreatedBy() string`

GetCreatedBy returns the CreatedBy field if non-nil, zero value otherwise.

### GetCreatedByOk

`func (o *ProviderBundleVersion) GetCreatedByOk() (*string, bool)`

GetCreatedByOk returns a tuple with the CreatedBy field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedBy

`func (o *ProviderBundleVersion) SetCreatedBy(v string)`

SetCreatedBy sets CreatedBy field to given value.


### GetCreatedAt

`func (o *ProviderBundleVersion) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *ProviderBundleVersion) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *ProviderBundleVersion) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


