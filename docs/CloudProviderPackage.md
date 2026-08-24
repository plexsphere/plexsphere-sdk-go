# CloudProviderPackage

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Source** | **string** | OCI repository the provider package is pulled from, without a tag or digest (e.g. &#x60;xpkg.upbound.io/upbound/provider-aws-s3&#x60;). A tag belongs in &#x60;version&#x60;.  | 
**Version** | **string** | Package version: an OCI tag, optionally pinned with a sha256 digest (e.g. &#x60;v2.6.1&#x60; or &#x60;v2.6.1@sha256:&lt;64 hex&gt;&#x60;). The combined tag-and-digest form is accepted because the Crossplane package manager consumes it verbatim.  | 
**Origin** | Pointer to [**CloudProviderPackageOrigin**](CloudProviderPackageOrigin.md) |  | [optional] 

## Methods

### NewCloudProviderPackage

`func NewCloudProviderPackage(source string, version string, ) *CloudProviderPackage`

NewCloudProviderPackage instantiates a new CloudProviderPackage object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCloudProviderPackageWithDefaults

`func NewCloudProviderPackageWithDefaults() *CloudProviderPackage`

NewCloudProviderPackageWithDefaults instantiates a new CloudProviderPackage object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSource

`func (o *CloudProviderPackage) GetSource() string`

GetSource returns the Source field if non-nil, zero value otherwise.

### GetSourceOk

`func (o *CloudProviderPackage) GetSourceOk() (*string, bool)`

GetSourceOk returns a tuple with the Source field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSource

`func (o *CloudProviderPackage) SetSource(v string)`

SetSource sets Source field to given value.


### GetVersion

`func (o *CloudProviderPackage) GetVersion() string`

GetVersion returns the Version field if non-nil, zero value otherwise.

### GetVersionOk

`func (o *CloudProviderPackage) GetVersionOk() (*string, bool)`

GetVersionOk returns a tuple with the Version field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetVersion

`func (o *CloudProviderPackage) SetVersion(v string)`

SetVersion sets Version field to given value.


### GetOrigin

`func (o *CloudProviderPackage) GetOrigin() CloudProviderPackageOrigin`

GetOrigin returns the Origin field if non-nil, zero value otherwise.

### GetOriginOk

`func (o *CloudProviderPackage) GetOriginOk() (*CloudProviderPackageOrigin, bool)`

GetOriginOk returns a tuple with the Origin field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOrigin

`func (o *CloudProviderPackage) SetOrigin(v CloudProviderPackageOrigin)`

SetOrigin sets Origin field to given value.

### HasOrigin

`func (o *CloudProviderPackage) HasOrigin() bool`

HasOrigin returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


