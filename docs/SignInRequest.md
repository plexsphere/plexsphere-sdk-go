# SignInRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DomainId** | Pointer to **string** | Domain the user is signing into. | [optional] 
**IdpBindingId** | Pointer to **string** | Explicit IdP binding override within a Domain. | [optional] 
**ReturnTo** | Pointer to **string** | Post-sign-in redirect target. Must be an allow-listed relative path or absolute URL.  | [optional] 
**Prompt** | Pointer to **string** | Optional OIDC &#x60;prompt&#x60; parameter forwarded to the IdP (e.g. \&quot;login\&quot;, \&quot;consent\&quot;).  | [optional] 

## Methods

### NewSignInRequest

`func NewSignInRequest() *SignInRequest`

NewSignInRequest instantiates a new SignInRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSignInRequestWithDefaults

`func NewSignInRequestWithDefaults() *SignInRequest`

NewSignInRequestWithDefaults instantiates a new SignInRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDomainId

`func (o *SignInRequest) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *SignInRequest) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *SignInRequest) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.

### HasDomainId

`func (o *SignInRequest) HasDomainId() bool`

HasDomainId returns a boolean if a field has been set.

### GetIdpBindingId

`func (o *SignInRequest) GetIdpBindingId() string`

GetIdpBindingId returns the IdpBindingId field if non-nil, zero value otherwise.

### GetIdpBindingIdOk

`func (o *SignInRequest) GetIdpBindingIdOk() (*string, bool)`

GetIdpBindingIdOk returns a tuple with the IdpBindingId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIdpBindingId

`func (o *SignInRequest) SetIdpBindingId(v string)`

SetIdpBindingId sets IdpBindingId field to given value.

### HasIdpBindingId

`func (o *SignInRequest) HasIdpBindingId() bool`

HasIdpBindingId returns a boolean if a field has been set.

### GetReturnTo

`func (o *SignInRequest) GetReturnTo() string`

GetReturnTo returns the ReturnTo field if non-nil, zero value otherwise.

### GetReturnToOk

`func (o *SignInRequest) GetReturnToOk() (*string, bool)`

GetReturnToOk returns a tuple with the ReturnTo field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetReturnTo

`func (o *SignInRequest) SetReturnTo(v string)`

SetReturnTo sets ReturnTo field to given value.

### HasReturnTo

`func (o *SignInRequest) HasReturnTo() bool`

HasReturnTo returns a boolean if a field has been set.

### GetPrompt

`func (o *SignInRequest) GetPrompt() string`

GetPrompt returns the Prompt field if non-nil, zero value otherwise.

### GetPromptOk

`func (o *SignInRequest) GetPromptOk() (*string, bool)`

GetPromptOk returns a tuple with the Prompt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPrompt

`func (o *SignInRequest) SetPrompt(v string)`

SetPrompt sets Prompt field to given value.

### HasPrompt

`func (o *SignInRequest) HasPrompt() bool`

HasPrompt returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


