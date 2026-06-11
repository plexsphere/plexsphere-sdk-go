# EndpointRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Endpoint** | **string** | Canonical &#x60;host:port&#x60; wire form of the observed transport endpoint. The host is an IPv4 dotted quad or an IPv6 address bracketed per RFC 5952 (&#x60;[2001:db8::1]:51820&#x60;); the port is in the RFC 6056 ephemeral range 1..65535. Loopback, link-local, and unspecified addresses are refused with 400 &#x60;endpoint_unparseable&#x60;.  | 
**NatType** | [**EndpointRequestNatType**](EndpointRequestNatType.md) |  | 
**ReportedAt** | **time.Time** | Agent wall-clock at the moment the observation was made. The handler rejects the request with 400 &#x60;endpoint_clock_skew&#x60; if the value drifts more than 60 seconds from server now.  | 

## Methods

### NewEndpointRequest

`func NewEndpointRequest(endpoint string, natType EndpointRequestNatType, reportedAt time.Time, ) *EndpointRequest`

NewEndpointRequest instantiates a new EndpointRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewEndpointRequestWithDefaults

`func NewEndpointRequestWithDefaults() *EndpointRequest`

NewEndpointRequestWithDefaults instantiates a new EndpointRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetEndpoint

`func (o *EndpointRequest) GetEndpoint() string`

GetEndpoint returns the Endpoint field if non-nil, zero value otherwise.

### GetEndpointOk

`func (o *EndpointRequest) GetEndpointOk() (*string, bool)`

GetEndpointOk returns a tuple with the Endpoint field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEndpoint

`func (o *EndpointRequest) SetEndpoint(v string)`

SetEndpoint sets Endpoint field to given value.


### GetNatType

`func (o *EndpointRequest) GetNatType() EndpointRequestNatType`

GetNatType returns the NatType field if non-nil, zero value otherwise.

### GetNatTypeOk

`func (o *EndpointRequest) GetNatTypeOk() (*EndpointRequestNatType, bool)`

GetNatTypeOk returns a tuple with the NatType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNatType

`func (o *EndpointRequest) SetNatType(v EndpointRequestNatType)`

SetNatType sets NatType field to given value.


### GetReportedAt

`func (o *EndpointRequest) GetReportedAt() time.Time`

GetReportedAt returns the ReportedAt field if non-nil, zero value otherwise.

### GetReportedAtOk

`func (o *EndpointRequest) GetReportedAtOk() (*time.Time, bool)`

GetReportedAtOk returns a tuple with the ReportedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetReportedAt

`func (o *EndpointRequest) SetReportedAt(v time.Time)`

SetReportedAt sets ReportedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


