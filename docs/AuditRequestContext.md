# AuditRequestContext

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Ip** | Pointer to **string** | Client IP after proxy unwrapping (IPv4 or IPv6 textual form). | [optional] 
**UserAgent** | Pointer to **string** | Verbatim &#x60;User-Agent&#x60; header value. | [optional] 

## Methods

### NewAuditRequestContext

`func NewAuditRequestContext() *AuditRequestContext`

NewAuditRequestContext instantiates a new AuditRequestContext object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewAuditRequestContextWithDefaults

`func NewAuditRequestContextWithDefaults() *AuditRequestContext`

NewAuditRequestContextWithDefaults instantiates a new AuditRequestContext object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetIp

`func (o *AuditRequestContext) GetIp() string`

GetIp returns the Ip field if non-nil, zero value otherwise.

### GetIpOk

`func (o *AuditRequestContext) GetIpOk() (*string, bool)`

GetIpOk returns a tuple with the Ip field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIp

`func (o *AuditRequestContext) SetIp(v string)`

SetIp sets Ip field to given value.

### HasIp

`func (o *AuditRequestContext) HasIp() bool`

HasIp returns a boolean if a field has been set.

### GetUserAgent

`func (o *AuditRequestContext) GetUserAgent() string`

GetUserAgent returns the UserAgent field if non-nil, zero value otherwise.

### GetUserAgentOk

`func (o *AuditRequestContext) GetUserAgentOk() (*string, bool)`

GetUserAgentOk returns a tuple with the UserAgent field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserAgent

`func (o *AuditRequestContext) SetUserAgent(v string)`

SetUserAgent sets UserAgent field to given value.

### HasUserAgent

`func (o *AuditRequestContext) HasUserAgent() bool`

HasUserAgent returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


