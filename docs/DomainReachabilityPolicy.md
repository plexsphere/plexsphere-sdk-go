# DomainReachabilityPolicy

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**HeartbeatInterval** | **string** | Cadence agents must honour. Floor 10s, ceiling 1h. Encoded as a Go duration string (e.g. &#x60;30s&#x60;, &#x60;1m&#x60;).  | 
**StaleAfter** | **string** | Grace window before a Node is declared stale. Must be at least &#x60;3 × heartbeat_interval&#x60; and at most 1h.  | 
**UnreachableAfter** | **string** | Grace window before a Node is declared unreachable. Must be at least &#x60;2 × stale_after&#x60; and at most 1h.  | 

## Methods

### NewDomainReachabilityPolicy

`func NewDomainReachabilityPolicy(heartbeatInterval string, staleAfter string, unreachableAfter string, ) *DomainReachabilityPolicy`

NewDomainReachabilityPolicy instantiates a new DomainReachabilityPolicy object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDomainReachabilityPolicyWithDefaults

`func NewDomainReachabilityPolicyWithDefaults() *DomainReachabilityPolicy`

NewDomainReachabilityPolicyWithDefaults instantiates a new DomainReachabilityPolicy object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetHeartbeatInterval

`func (o *DomainReachabilityPolicy) GetHeartbeatInterval() string`

GetHeartbeatInterval returns the HeartbeatInterval field if non-nil, zero value otherwise.

### GetHeartbeatIntervalOk

`func (o *DomainReachabilityPolicy) GetHeartbeatIntervalOk() (*string, bool)`

GetHeartbeatIntervalOk returns a tuple with the HeartbeatInterval field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetHeartbeatInterval

`func (o *DomainReachabilityPolicy) SetHeartbeatInterval(v string)`

SetHeartbeatInterval sets HeartbeatInterval field to given value.


### GetStaleAfter

`func (o *DomainReachabilityPolicy) GetStaleAfter() string`

GetStaleAfter returns the StaleAfter field if non-nil, zero value otherwise.

### GetStaleAfterOk

`func (o *DomainReachabilityPolicy) GetStaleAfterOk() (*string, bool)`

GetStaleAfterOk returns a tuple with the StaleAfter field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStaleAfter

`func (o *DomainReachabilityPolicy) SetStaleAfter(v string)`

SetStaleAfter sets StaleAfter field to given value.


### GetUnreachableAfter

`func (o *DomainReachabilityPolicy) GetUnreachableAfter() string`

GetUnreachableAfter returns the UnreachableAfter field if non-nil, zero value otherwise.

### GetUnreachableAfterOk

`func (o *DomainReachabilityPolicy) GetUnreachableAfterOk() (*string, bool)`

GetUnreachableAfterOk returns a tuple with the UnreachableAfter field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUnreachableAfter

`func (o *DomainReachabilityPolicy) SetUnreachableAfter(v string)`

SetUnreachableAfter sets UnreachableAfter field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


