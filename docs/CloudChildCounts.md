# CloudChildCounts

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CloudCredentials** | **int32** | Number of &#x60;CloudCredential&#x60; rows whose home Cloud is this Cloud (the &#x60;cloud_credential.cloud_id&#x60; anchor).  | 
**CloudCredentialUsages** | **int32** | Number of usage edges that attach a &#x60;CloudCredential&#x60; homed on another Cloud to this Cloud. A delete blocked solely by usage edges reports &#x60;cloud_credentials: 0&#x60; here, so a machine consumer keys on this field to know it must detach usage edges rather than home credentials.  | 

## Methods

### NewCloudChildCounts

`func NewCloudChildCounts(cloudCredentials int32, cloudCredentialUsages int32, ) *CloudChildCounts`

NewCloudChildCounts instantiates a new CloudChildCounts object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCloudChildCountsWithDefaults

`func NewCloudChildCountsWithDefaults() *CloudChildCounts`

NewCloudChildCountsWithDefaults instantiates a new CloudChildCounts object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCloudCredentials

`func (o *CloudChildCounts) GetCloudCredentials() int32`

GetCloudCredentials returns the CloudCredentials field if non-nil, zero value otherwise.

### GetCloudCredentialsOk

`func (o *CloudChildCounts) GetCloudCredentialsOk() (*int32, bool)`

GetCloudCredentialsOk returns a tuple with the CloudCredentials field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCloudCredentials

`func (o *CloudChildCounts) SetCloudCredentials(v int32)`

SetCloudCredentials sets CloudCredentials field to given value.


### GetCloudCredentialUsages

`func (o *CloudChildCounts) GetCloudCredentialUsages() int32`

GetCloudCredentialUsages returns the CloudCredentialUsages field if non-nil, zero value otherwise.

### GetCloudCredentialUsagesOk

`func (o *CloudChildCounts) GetCloudCredentialUsagesOk() (*int32, bool)`

GetCloudCredentialUsagesOk returns a tuple with the CloudCredentialUsages field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCloudCredentialUsages

`func (o *CloudChildCounts) SetCloudCredentialUsages(v int32)`

SetCloudCredentialUsages sets CloudCredentialUsages field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


