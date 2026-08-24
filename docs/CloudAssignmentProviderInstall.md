# CloudAssignmentProviderInstall

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Source** | **string** | OCI repository of the declared package this entry reports on, without a tag or digest (e.g. &#x60;xpkg.upbound.io/upbound/provider-aws-s3&#x60;). It matches one of the &#x60;source&#x60; values in the Cloud&#39;s &#x60;provider_packages&#x60;.  | 
**Phase** | **string** | Lifecycle phase of the provider package on the hosting cluster, one of &#x60;Pending&#x60;, &#x60;Installing&#x60;, &#x60;Serving&#x60;, &#x60;Failed&#x60;, or &#x60;Conflict&#x60;. &#x60;Pending&#x60; means the platform has not yet reconciled the package — including the window before the Project has been placed on a management cluster. &#x60;Installing&#x60; means the package is applied and the package manager has not yet reported it healthy. &#x60;Serving&#x60; means the Project can provision against the Cloud. &#x60;Failed&#x60; means the package manager reported it unhealthy, with the reason in &#x60;message&#x60;. &#x60;Conflict&#x60; means the package cannot be applied without overwriting something the platform does not own — two Clouds naming the same package at different versions, or an existing provider serving a different package — and &#x60;message&#x60; names both sides.  | 
**Message** | Pointer to **string** | Operator-facing explanation behind the phase: the package manager&#39;s own condition message for &#x60;Failed&#x60;, the competing versions or sources for &#x60;Conflict&#x60;, and absent for &#x60;Serving&#x60;.  | [optional] 
**ObservedAt** | Pointer to **time.Time** | When the platform last observed the package on the cluster (UTC). Absent while the phase is &#x60;Pending&#x60;, which is the state that has not been observed yet.  | [optional] 

## Methods

### NewCloudAssignmentProviderInstall

`func NewCloudAssignmentProviderInstall(source string, phase string, ) *CloudAssignmentProviderInstall`

NewCloudAssignmentProviderInstall instantiates a new CloudAssignmentProviderInstall object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCloudAssignmentProviderInstallWithDefaults

`func NewCloudAssignmentProviderInstallWithDefaults() *CloudAssignmentProviderInstall`

NewCloudAssignmentProviderInstallWithDefaults instantiates a new CloudAssignmentProviderInstall object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSource

`func (o *CloudAssignmentProviderInstall) GetSource() string`

GetSource returns the Source field if non-nil, zero value otherwise.

### GetSourceOk

`func (o *CloudAssignmentProviderInstall) GetSourceOk() (*string, bool)`

GetSourceOk returns a tuple with the Source field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSource

`func (o *CloudAssignmentProviderInstall) SetSource(v string)`

SetSource sets Source field to given value.


### GetPhase

`func (o *CloudAssignmentProviderInstall) GetPhase() string`

GetPhase returns the Phase field if non-nil, zero value otherwise.

### GetPhaseOk

`func (o *CloudAssignmentProviderInstall) GetPhaseOk() (*string, bool)`

GetPhaseOk returns a tuple with the Phase field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPhase

`func (o *CloudAssignmentProviderInstall) SetPhase(v string)`

SetPhase sets Phase field to given value.


### GetMessage

`func (o *CloudAssignmentProviderInstall) GetMessage() string`

GetMessage returns the Message field if non-nil, zero value otherwise.

### GetMessageOk

`func (o *CloudAssignmentProviderInstall) GetMessageOk() (*string, bool)`

GetMessageOk returns a tuple with the Message field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessage

`func (o *CloudAssignmentProviderInstall) SetMessage(v string)`

SetMessage sets Message field to given value.

### HasMessage

`func (o *CloudAssignmentProviderInstall) HasMessage() bool`

HasMessage returns a boolean if a field has been set.

### GetObservedAt

`func (o *CloudAssignmentProviderInstall) GetObservedAt() time.Time`

GetObservedAt returns the ObservedAt field if non-nil, zero value otherwise.

### GetObservedAtOk

`func (o *CloudAssignmentProviderInstall) GetObservedAtOk() (*time.Time, bool)`

GetObservedAtOk returns a tuple with the ObservedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetObservedAt

`func (o *CloudAssignmentProviderInstall) SetObservedAt(v time.Time)`

SetObservedAt sets ObservedAt field to given value.

### HasObservedAt

`func (o *CloudAssignmentProviderInstall) HasObservedAt() bool`

HasObservedAt returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


