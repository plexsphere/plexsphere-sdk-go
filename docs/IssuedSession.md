# IssuedSession

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**SessionId** | **string** | Identifier of the issued Session (UUIDv7). Equals the token&#39;s &#x60;jti&#x60;.  | 
**Token** | **string** | The signed, session-scoped EdDSA JWT. Delivered exactly once, in this response. Treat as a bearer secret.  | 
**ExpiresAt** | **time.Time** | Expiry timestamp (UTC) of the issued Session and its token.  | 
**ListenerEndpoint** | Pointer to **string** | The on-Node endpoint (&#x60;host:port&#x60;) the operator&#39;s client connects to for this session kind.  | [optional] 
**Session** | [**Session**](Session.md) |  | 

## Methods

### NewIssuedSession

`func NewIssuedSession(sessionId string, token string, expiresAt time.Time, session Session, ) *IssuedSession`

NewIssuedSession instantiates a new IssuedSession object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewIssuedSessionWithDefaults

`func NewIssuedSessionWithDefaults() *IssuedSession`

NewIssuedSessionWithDefaults instantiates a new IssuedSession object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSessionId

`func (o *IssuedSession) GetSessionId() string`

GetSessionId returns the SessionId field if non-nil, zero value otherwise.

### GetSessionIdOk

`func (o *IssuedSession) GetSessionIdOk() (*string, bool)`

GetSessionIdOk returns a tuple with the SessionId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSessionId

`func (o *IssuedSession) SetSessionId(v string)`

SetSessionId sets SessionId field to given value.


### GetToken

`func (o *IssuedSession) GetToken() string`

GetToken returns the Token field if non-nil, zero value otherwise.

### GetTokenOk

`func (o *IssuedSession) GetTokenOk() (*string, bool)`

GetTokenOk returns a tuple with the Token field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetToken

`func (o *IssuedSession) SetToken(v string)`

SetToken sets Token field to given value.


### GetExpiresAt

`func (o *IssuedSession) GetExpiresAt() time.Time`

GetExpiresAt returns the ExpiresAt field if non-nil, zero value otherwise.

### GetExpiresAtOk

`func (o *IssuedSession) GetExpiresAtOk() (*time.Time, bool)`

GetExpiresAtOk returns a tuple with the ExpiresAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExpiresAt

`func (o *IssuedSession) SetExpiresAt(v time.Time)`

SetExpiresAt sets ExpiresAt field to given value.


### GetListenerEndpoint

`func (o *IssuedSession) GetListenerEndpoint() string`

GetListenerEndpoint returns the ListenerEndpoint field if non-nil, zero value otherwise.

### GetListenerEndpointOk

`func (o *IssuedSession) GetListenerEndpointOk() (*string, bool)`

GetListenerEndpointOk returns a tuple with the ListenerEndpoint field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetListenerEndpoint

`func (o *IssuedSession) SetListenerEndpoint(v string)`

SetListenerEndpoint sets ListenerEndpoint field to given value.

### HasListenerEndpoint

`func (o *IssuedSession) HasListenerEndpoint() bool`

HasListenerEndpoint returns a boolean if a field has been set.

### GetSession

`func (o *IssuedSession) GetSession() Session`

GetSession returns the Session field if non-nil, zero value otherwise.

### GetSessionOk

`func (o *IssuedSession) GetSessionOk() (*Session, bool)`

GetSessionOk returns a tuple with the Session field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSession

`func (o *IssuedSession) SetSession(v Session)`

SetSession sets Session field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


