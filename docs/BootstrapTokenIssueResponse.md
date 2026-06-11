# BootstrapTokenIssueResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**TokenId** | **string** | BootstrapToken identifier (UUIDv7). | 
**Token** | **string** | Plaintext bearer string in the documented &#x60;psb_&lt;env&gt;_&lt;projectId&gt;_&lt;kind&gt;_&lt;random&gt;&#x60; format (matches &#x60;^psb_[a-z]+_[a-z2-7]+_(node|bridge)_[a-z2-7]{20,}$&#x60;). **Shown exactly once** — there is no API surface that ever returns the plaintext again. The Spectral rule policed by task 4.2 keys off the &#x60;x-plexsphere-once: true&#x60; extension on this property.  | 
**IssuedAt** | **time.Time** | Issuance timestamp (UTC). | 
**ExpiresAt** | **time.Time** | Absolute expiry derived from &#x60;issued_at + ttl_seconds&#x60;. After this point the token is no longer redeemable.  | 

## Methods

### NewBootstrapTokenIssueResponse

`func NewBootstrapTokenIssueResponse(tokenId string, token string, issuedAt time.Time, expiresAt time.Time, ) *BootstrapTokenIssueResponse`

NewBootstrapTokenIssueResponse instantiates a new BootstrapTokenIssueResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBootstrapTokenIssueResponseWithDefaults

`func NewBootstrapTokenIssueResponseWithDefaults() *BootstrapTokenIssueResponse`

NewBootstrapTokenIssueResponseWithDefaults instantiates a new BootstrapTokenIssueResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetTokenId

`func (o *BootstrapTokenIssueResponse) GetTokenId() string`

GetTokenId returns the TokenId field if non-nil, zero value otherwise.

### GetTokenIdOk

`func (o *BootstrapTokenIssueResponse) GetTokenIdOk() (*string, bool)`

GetTokenIdOk returns a tuple with the TokenId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTokenId

`func (o *BootstrapTokenIssueResponse) SetTokenId(v string)`

SetTokenId sets TokenId field to given value.


### GetToken

`func (o *BootstrapTokenIssueResponse) GetToken() string`

GetToken returns the Token field if non-nil, zero value otherwise.

### GetTokenOk

`func (o *BootstrapTokenIssueResponse) GetTokenOk() (*string, bool)`

GetTokenOk returns a tuple with the Token field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetToken

`func (o *BootstrapTokenIssueResponse) SetToken(v string)`

SetToken sets Token field to given value.


### GetIssuedAt

`func (o *BootstrapTokenIssueResponse) GetIssuedAt() time.Time`

GetIssuedAt returns the IssuedAt field if non-nil, zero value otherwise.

### GetIssuedAtOk

`func (o *BootstrapTokenIssueResponse) GetIssuedAtOk() (*time.Time, bool)`

GetIssuedAtOk returns a tuple with the IssuedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIssuedAt

`func (o *BootstrapTokenIssueResponse) SetIssuedAt(v time.Time)`

SetIssuedAt sets IssuedAt field to given value.


### GetExpiresAt

`func (o *BootstrapTokenIssueResponse) GetExpiresAt() time.Time`

GetExpiresAt returns the ExpiresAt field if non-nil, zero value otherwise.

### GetExpiresAtOk

`func (o *BootstrapTokenIssueResponse) GetExpiresAtOk() (*time.Time, bool)`

GetExpiresAtOk returns a tuple with the ExpiresAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExpiresAt

`func (o *BootstrapTokenIssueResponse) SetExpiresAt(v time.Time)`

SetExpiresAt sets ExpiresAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


