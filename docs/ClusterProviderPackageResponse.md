# ClusterProviderPackageResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Source** | **string** | OCI repository of the provider package, without a tag or digest (for example &#x60;xpkg.upbound.io/upbound/provider-aws-s3&#x60;). Together with the cluster it identifies the record.  | 
**Version** | **string** | Package version the platform converged the cluster to — an OCI tag, optionally pinned with a digest.  | 
**Phase** | **string** | Lifecycle phase of the package on this cluster, one of &#x60;Pending&#x60;, &#x60;Installing&#x60;, &#x60;Serving&#x60;, &#x60;Failed&#x60;, or &#x60;Conflict&#x60;. The values carry the meanings documented on &#x60;CloudAssignmentProviderInstall.phase&#x60;.  | 
**Message** | Pointer to **string** | Operator-facing explanation behind the phase: the package manager&#39;s own condition message for &#x60;Failed&#x60;, the competing versions or sources for &#x60;Conflict&#x60;, and absent for &#x60;Serving&#x60;.  | [optional] 
**ObservedAt** | Pointer to **time.Time** | When the platform last observed the package on the cluster (UTC).  | [optional] 

## Methods

### NewClusterProviderPackageResponse

`func NewClusterProviderPackageResponse(source string, version string, phase string, ) *ClusterProviderPackageResponse`

NewClusterProviderPackageResponse instantiates a new ClusterProviderPackageResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewClusterProviderPackageResponseWithDefaults

`func NewClusterProviderPackageResponseWithDefaults() *ClusterProviderPackageResponse`

NewClusterProviderPackageResponseWithDefaults instantiates a new ClusterProviderPackageResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSource

`func (o *ClusterProviderPackageResponse) GetSource() string`

GetSource returns the Source field if non-nil, zero value otherwise.

### GetSourceOk

`func (o *ClusterProviderPackageResponse) GetSourceOk() (*string, bool)`

GetSourceOk returns a tuple with the Source field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSource

`func (o *ClusterProviderPackageResponse) SetSource(v string)`

SetSource sets Source field to given value.


### GetVersion

`func (o *ClusterProviderPackageResponse) GetVersion() string`

GetVersion returns the Version field if non-nil, zero value otherwise.

### GetVersionOk

`func (o *ClusterProviderPackageResponse) GetVersionOk() (*string, bool)`

GetVersionOk returns a tuple with the Version field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetVersion

`func (o *ClusterProviderPackageResponse) SetVersion(v string)`

SetVersion sets Version field to given value.


### GetPhase

`func (o *ClusterProviderPackageResponse) GetPhase() string`

GetPhase returns the Phase field if non-nil, zero value otherwise.

### GetPhaseOk

`func (o *ClusterProviderPackageResponse) GetPhaseOk() (*string, bool)`

GetPhaseOk returns a tuple with the Phase field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPhase

`func (o *ClusterProviderPackageResponse) SetPhase(v string)`

SetPhase sets Phase field to given value.


### GetMessage

`func (o *ClusterProviderPackageResponse) GetMessage() string`

GetMessage returns the Message field if non-nil, zero value otherwise.

### GetMessageOk

`func (o *ClusterProviderPackageResponse) GetMessageOk() (*string, bool)`

GetMessageOk returns a tuple with the Message field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessage

`func (o *ClusterProviderPackageResponse) SetMessage(v string)`

SetMessage sets Message field to given value.

### HasMessage

`func (o *ClusterProviderPackageResponse) HasMessage() bool`

HasMessage returns a boolean if a field has been set.

### GetObservedAt

`func (o *ClusterProviderPackageResponse) GetObservedAt() time.Time`

GetObservedAt returns the ObservedAt field if non-nil, zero value otherwise.

### GetObservedAtOk

`func (o *ClusterProviderPackageResponse) GetObservedAtOk() (*time.Time, bool)`

GetObservedAtOk returns a tuple with the ObservedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetObservedAt

`func (o *ClusterProviderPackageResponse) SetObservedAt(v time.Time)`

SetObservedAt sets ObservedAt field to given value.

### HasObservedAt

`func (o *ClusterProviderPackageResponse) HasObservedAt() bool`

HasObservedAt returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


