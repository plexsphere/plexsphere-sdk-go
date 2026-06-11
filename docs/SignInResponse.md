# SignInResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AuthorizationUrl** | **string** | OIDC authorization URL the caller redirects to. | 
**State** | **string** | Opaque state value correlated on the callback. | 
**CodeVerifierHandle** | **string** | Opaque handle that resolves the PKCE verifier. | 
**Nonce** | **string** | OIDC nonce passed into the ID token. | 

## Methods

### NewSignInResponse

`func NewSignInResponse(authorizationUrl string, state string, codeVerifierHandle string, nonce string, ) *SignInResponse`

NewSignInResponse instantiates a new SignInResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSignInResponseWithDefaults

`func NewSignInResponseWithDefaults() *SignInResponse`

NewSignInResponseWithDefaults instantiates a new SignInResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetAuthorizationUrl

`func (o *SignInResponse) GetAuthorizationUrl() string`

GetAuthorizationUrl returns the AuthorizationUrl field if non-nil, zero value otherwise.

### GetAuthorizationUrlOk

`func (o *SignInResponse) GetAuthorizationUrlOk() (*string, bool)`

GetAuthorizationUrlOk returns a tuple with the AuthorizationUrl field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAuthorizationUrl

`func (o *SignInResponse) SetAuthorizationUrl(v string)`

SetAuthorizationUrl sets AuthorizationUrl field to given value.


### GetState

`func (o *SignInResponse) GetState() string`

GetState returns the State field if non-nil, zero value otherwise.

### GetStateOk

`func (o *SignInResponse) GetStateOk() (*string, bool)`

GetStateOk returns a tuple with the State field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetState

`func (o *SignInResponse) SetState(v string)`

SetState sets State field to given value.


### GetCodeVerifierHandle

`func (o *SignInResponse) GetCodeVerifierHandle() string`

GetCodeVerifierHandle returns the CodeVerifierHandle field if non-nil, zero value otherwise.

### GetCodeVerifierHandleOk

`func (o *SignInResponse) GetCodeVerifierHandleOk() (*string, bool)`

GetCodeVerifierHandleOk returns a tuple with the CodeVerifierHandle field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCodeVerifierHandle

`func (o *SignInResponse) SetCodeVerifierHandle(v string)`

SetCodeVerifierHandle sets CodeVerifierHandle field to given value.


### GetNonce

`func (o *SignInResponse) GetNonce() string`

GetNonce returns the Nonce field if non-nil, zero value otherwise.

### GetNonceOk

`func (o *SignInResponse) GetNonceOk() (*string, bool)`

GetNonceOk returns a tuple with the Nonce field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNonce

`func (o *SignInResponse) SetNonce(v string)`

SetNonce sets Nonce field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


