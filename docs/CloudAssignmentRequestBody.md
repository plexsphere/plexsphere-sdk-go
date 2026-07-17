# CloudAssignmentRequestBody

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CloudId** | **string** | Identifier of the Cloud to request. Must be a non-zero UUID — a malformed value is rejected with &#x60;400 invalid_cloud_id&#x60;.  | 

## Methods

### NewCloudAssignmentRequestBody

`func NewCloudAssignmentRequestBody(cloudId string, ) *CloudAssignmentRequestBody`

NewCloudAssignmentRequestBody instantiates a new CloudAssignmentRequestBody object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCloudAssignmentRequestBodyWithDefaults

`func NewCloudAssignmentRequestBodyWithDefaults() *CloudAssignmentRequestBody`

NewCloudAssignmentRequestBodyWithDefaults instantiates a new CloudAssignmentRequestBody object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCloudId

`func (o *CloudAssignmentRequestBody) GetCloudId() string`

GetCloudId returns the CloudId field if non-nil, zero value otherwise.

### GetCloudIdOk

`func (o *CloudAssignmentRequestBody) GetCloudIdOk() (*string, bool)`

GetCloudIdOk returns a tuple with the CloudId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCloudId

`func (o *CloudAssignmentRequestBody) SetCloudId(v string)`

SetCloudId sets CloudId field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


