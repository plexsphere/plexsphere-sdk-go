# EndpointResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AcceptedAt** | **time.Time** | Server-side timestamp at which the endpoint observation was committed. Distinct from &#x60;reported_at&#x60; so the caller can estimate one-way latency and clock-skew.  | 
**StaleAfter** | **time.Time** | Server-side deadline by which the agent must submit a fresh observation before the per-Domain endpoint sweeper stamps the endpoint as stale and emits a tombstone event. Equal to &#x60;accepted_at&#x60; plus the per-Domain endpoint TTL (defaults to 5 minutes).  | 

## Methods

### NewEndpointResponse

`func NewEndpointResponse(acceptedAt time.Time, staleAfter time.Time, ) *EndpointResponse`

NewEndpointResponse instantiates a new EndpointResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewEndpointResponseWithDefaults

`func NewEndpointResponseWithDefaults() *EndpointResponse`

NewEndpointResponseWithDefaults instantiates a new EndpointResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetAcceptedAt

`func (o *EndpointResponse) GetAcceptedAt() time.Time`

GetAcceptedAt returns the AcceptedAt field if non-nil, zero value otherwise.

### GetAcceptedAtOk

`func (o *EndpointResponse) GetAcceptedAtOk() (*time.Time, bool)`

GetAcceptedAtOk returns a tuple with the AcceptedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAcceptedAt

`func (o *EndpointResponse) SetAcceptedAt(v time.Time)`

SetAcceptedAt sets AcceptedAt field to given value.


### GetStaleAfter

`func (o *EndpointResponse) GetStaleAfter() time.Time`

GetStaleAfter returns the StaleAfter field if non-nil, zero value otherwise.

### GetStaleAfterOk

`func (o *EndpointResponse) GetStaleAfterOk() (*time.Time, bool)`

GetStaleAfterOk returns a tuple with the StaleAfter field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStaleAfter

`func (o *EndpointResponse) SetStaleAfter(v time.Time)`

SetStaleAfter sets StaleAfter field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


