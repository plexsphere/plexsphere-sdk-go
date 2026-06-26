# CloudCredentialIssueRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DisplayName** | **string** | Human-readable Cloud Credential name. Empty or whitespace-only is rejected with &#x60;400 invalid_display_name&#x60;.  | 
**Payload** | **string** | Base64-encoded secret bytes written under &#x60;data.payload&#x60; in KV-v2. An empty payload is rejected with &#x60;400 invalid_payload&#x60;.  | 
**KeyValues** | Pointer to **map[string]string** | Optional flat data map written alongside the payload in KV-v2. Keys and values are caller-owned and never returned.  | [optional] 

## Methods

### NewCloudCredentialIssueRequest

`func NewCloudCredentialIssueRequest(displayName string, payload string, ) *CloudCredentialIssueRequest`

NewCloudCredentialIssueRequest instantiates a new CloudCredentialIssueRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCloudCredentialIssueRequestWithDefaults

`func NewCloudCredentialIssueRequestWithDefaults() *CloudCredentialIssueRequest`

NewCloudCredentialIssueRequestWithDefaults instantiates a new CloudCredentialIssueRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDisplayName

`func (o *CloudCredentialIssueRequest) GetDisplayName() string`

GetDisplayName returns the DisplayName field if non-nil, zero value otherwise.

### GetDisplayNameOk

`func (o *CloudCredentialIssueRequest) GetDisplayNameOk() (*string, bool)`

GetDisplayNameOk returns a tuple with the DisplayName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisplayName

`func (o *CloudCredentialIssueRequest) SetDisplayName(v string)`

SetDisplayName sets DisplayName field to given value.


### GetPayload

`func (o *CloudCredentialIssueRequest) GetPayload() string`

GetPayload returns the Payload field if non-nil, zero value otherwise.

### GetPayloadOk

`func (o *CloudCredentialIssueRequest) GetPayloadOk() (*string, bool)`

GetPayloadOk returns a tuple with the Payload field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPayload

`func (o *CloudCredentialIssueRequest) SetPayload(v string)`

SetPayload sets Payload field to given value.


### GetKeyValues

`func (o *CloudCredentialIssueRequest) GetKeyValues() map[string]string`

GetKeyValues returns the KeyValues field if non-nil, zero value otherwise.

### GetKeyValuesOk

`func (o *CloudCredentialIssueRequest) GetKeyValuesOk() (*map[string]string, bool)`

GetKeyValuesOk returns a tuple with the KeyValues field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKeyValues

`func (o *CloudCredentialIssueRequest) SetKeyValues(v map[string]string)`

SetKeyValues sets KeyValues field to given value.

### HasKeyValues

`func (o *CloudCredentialIssueRequest) HasKeyValues() bool`

HasKeyValues returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


