# SinkTLS

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CaPem** | Pointer to **string** | PEM bundle the destination&#39;s certificate is verified against. Absent or empty selects the system trust store. A non-empty value decodes as PEM and holds at least one certificate.  | [optional] 
**InsecureSkipVerify** | Pointer to **bool** | Disable certificate verification altogether. Intended for a destination presenting a certificate the platform cannot be given a bundle for; it removes the guarantee that the telemetry reaches the endpoint it names.  | [optional] 

## Methods

### NewSinkTLS

`func NewSinkTLS() *SinkTLS`

NewSinkTLS instantiates a new SinkTLS object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSinkTLSWithDefaults

`func NewSinkTLSWithDefaults() *SinkTLS`

NewSinkTLSWithDefaults instantiates a new SinkTLS object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCaPem

`func (o *SinkTLS) GetCaPem() string`

GetCaPem returns the CaPem field if non-nil, zero value otherwise.

### GetCaPemOk

`func (o *SinkTLS) GetCaPemOk() (*string, bool)`

GetCaPemOk returns a tuple with the CaPem field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCaPem

`func (o *SinkTLS) SetCaPem(v string)`

SetCaPem sets CaPem field to given value.

### HasCaPem

`func (o *SinkTLS) HasCaPem() bool`

HasCaPem returns a boolean if a field has been set.

### GetInsecureSkipVerify

`func (o *SinkTLS) GetInsecureSkipVerify() bool`

GetInsecureSkipVerify returns the InsecureSkipVerify field if non-nil, zero value otherwise.

### GetInsecureSkipVerifyOk

`func (o *SinkTLS) GetInsecureSkipVerifyOk() (*bool, bool)`

GetInsecureSkipVerifyOk returns a tuple with the InsecureSkipVerify field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetInsecureSkipVerify

`func (o *SinkTLS) SetInsecureSkipVerify(v bool)`

SetInsecureSkipVerify sets InsecureSkipVerify field to given value.

### HasInsecureSkipVerify

`func (o *SinkTLS) HasInsecureSkipVerify() bool`

HasInsecureSkipVerify returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


