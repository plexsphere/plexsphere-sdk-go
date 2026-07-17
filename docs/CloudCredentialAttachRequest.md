# CloudCredentialAttachRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CloudId** | **string** | Identifier of the usage Cloud to attach. Must be a non-zero UUID — a malformed value is rejected with &#x60;400 invalid_cloud_id&#x60;.  | 

## Methods

### NewCloudCredentialAttachRequest

`func NewCloudCredentialAttachRequest(cloudId string, ) *CloudCredentialAttachRequest`

NewCloudCredentialAttachRequest instantiates a new CloudCredentialAttachRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCloudCredentialAttachRequestWithDefaults

`func NewCloudCredentialAttachRequestWithDefaults() *CloudCredentialAttachRequest`

NewCloudCredentialAttachRequestWithDefaults instantiates a new CloudCredentialAttachRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCloudId

`func (o *CloudCredentialAttachRequest) GetCloudId() string`

GetCloudId returns the CloudId field if non-nil, zero value otherwise.

### GetCloudIdOk

`func (o *CloudCredentialAttachRequest) GetCloudIdOk() (*string, bool)`

GetCloudIdOk returns a tuple with the CloudId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCloudId

`func (o *CloudCredentialAttachRequest) SetCloudId(v string)`

SetCloudId sets CloudId field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


