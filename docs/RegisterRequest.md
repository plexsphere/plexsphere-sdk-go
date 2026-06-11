# RegisterRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProjectId** | **string** | Project the redeeming substrate is enrolling into. Must match the &#x60;project_id&#x60; segment of the plaintext &#x60;bootstrap_token&#x60;; a mismatch surfaces as 403 with &#x60;reason&#x3D;project_mismatch&#x60;.  | 
**ResourceId** | **string** | Human-readable Resource handle (e.g. &#x60;edge-router-01&#x60;) the registering Node binds to. The handler resolves this against the Resource aggregate; an unknown handle surfaces as 404 with &#x60;code&#x3D;resource_not_found&#x60;.  | 
**BootstrapToken** | **string** | Plaintext BootstrapToken in the documented &#x60;psb_&lt;env&gt;_&lt;projectId&gt;_&lt;kind&gt;_&lt;random&gt;&#x60; format (matches &#x60;^psb_[a-z]+_[a-z2-7]+_(node|bridge)_[a-z2-7]{20,}$&#x60;) . The Validator parses the prefix to discover the env + project-id + kind triple before running the candidate scan.  | 
**Nonce** | **string** | Request-side replay-protection nonce. The persistence layer holds a partial UNIQUE on (project_id, consumed_nonce); a duplicate surfaces as 403 with &#x60;reason&#x3D;nonce_collision&#x60;.  | 
**PublicKey** | **string** | 32-byte X25519 (WireGuard) public key, base64-encoded with standard padding. RFC 7748 §5 fixes the curve to a 32-byte little-endian point encoding so any other byte length surfaces as 400 with &#x60;code&#x3D;public_key_invalid&#x60;; the all-zero degenerate value (a known small-order point) is also rejected with the same code. The fixed length-44 base64 canonical form is the standard &#x60;RawStdEncoding&#x60;-with-padding result for a 32-byte payload.  | 
**RequestedResourceId** | Pointer to **string** | Optional override the operator can supply when the substrate&#39;s own naming differs from the platform handle (e.g. the Node identifies itself as &#x60;node-12&#x60; while the platform Resource is &#x60;edge-router-01&#x60;). Empty or omitted means \&quot;no override; use &#x60;resource_id&#x60; verbatim\&quot; .  | [optional] 

## Methods

### NewRegisterRequest

`func NewRegisterRequest(projectId string, resourceId string, bootstrapToken string, nonce string, publicKey string, ) *RegisterRequest`

NewRegisterRequest instantiates a new RegisterRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewRegisterRequestWithDefaults

`func NewRegisterRequestWithDefaults() *RegisterRequest`

NewRegisterRequestWithDefaults instantiates a new RegisterRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetProjectId

`func (o *RegisterRequest) GetProjectId() string`

GetProjectId returns the ProjectId field if non-nil, zero value otherwise.

### GetProjectIdOk

`func (o *RegisterRequest) GetProjectIdOk() (*string, bool)`

GetProjectIdOk returns a tuple with the ProjectId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProjectId

`func (o *RegisterRequest) SetProjectId(v string)`

SetProjectId sets ProjectId field to given value.


### GetResourceId

`func (o *RegisterRequest) GetResourceId() string`

GetResourceId returns the ResourceId field if non-nil, zero value otherwise.

### GetResourceIdOk

`func (o *RegisterRequest) GetResourceIdOk() (*string, bool)`

GetResourceIdOk returns a tuple with the ResourceId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResourceId

`func (o *RegisterRequest) SetResourceId(v string)`

SetResourceId sets ResourceId field to given value.


### GetBootstrapToken

`func (o *RegisterRequest) GetBootstrapToken() string`

GetBootstrapToken returns the BootstrapToken field if non-nil, zero value otherwise.

### GetBootstrapTokenOk

`func (o *RegisterRequest) GetBootstrapTokenOk() (*string, bool)`

GetBootstrapTokenOk returns a tuple with the BootstrapToken field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBootstrapToken

`func (o *RegisterRequest) SetBootstrapToken(v string)`

SetBootstrapToken sets BootstrapToken field to given value.


### GetNonce

`func (o *RegisterRequest) GetNonce() string`

GetNonce returns the Nonce field if non-nil, zero value otherwise.

### GetNonceOk

`func (o *RegisterRequest) GetNonceOk() (*string, bool)`

GetNonceOk returns a tuple with the Nonce field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNonce

`func (o *RegisterRequest) SetNonce(v string)`

SetNonce sets Nonce field to given value.


### GetPublicKey

`func (o *RegisterRequest) GetPublicKey() string`

GetPublicKey returns the PublicKey field if non-nil, zero value otherwise.

### GetPublicKeyOk

`func (o *RegisterRequest) GetPublicKeyOk() (*string, bool)`

GetPublicKeyOk returns a tuple with the PublicKey field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPublicKey

`func (o *RegisterRequest) SetPublicKey(v string)`

SetPublicKey sets PublicKey field to given value.


### GetRequestedResourceId

`func (o *RegisterRequest) GetRequestedResourceId() string`

GetRequestedResourceId returns the RequestedResourceId field if non-nil, zero value otherwise.

### GetRequestedResourceIdOk

`func (o *RegisterRequest) GetRequestedResourceIdOk() (*string, bool)`

GetRequestedResourceIdOk returns a tuple with the RequestedResourceId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRequestedResourceId

`func (o *RegisterRequest) SetRequestedResourceId(v string)`

SetRequestedResourceId sets RequestedResourceId field to given value.

### HasRequestedResourceId

`func (o *RegisterRequest) HasRequestedResourceId() bool`

HasRequestedResourceId returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


