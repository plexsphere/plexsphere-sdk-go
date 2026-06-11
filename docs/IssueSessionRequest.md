# IssueSessionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ResourceId** | **string** | Identifier of the Resource to open a session against. | 
**Kind** | [**SessionKind**](SessionKind.md) |  | 
**Target** | [**SessionTarget**](SessionTarget.md) |  | 
**RequestedTtlSeconds** | Pointer to **int32** | Operator-requested TTL in whole seconds. Omitted falls back to the per-Domain default; a value above the per-Domain maximum is silently clamped, not rejected — the response &#x60;expires_at&#x60; reflects the effective TTL.  | [optional] 
**IdempotencyKey** | Pointer to **string** | Optional idempotency key. A repeat issuance with the same &#x60;(identity, idempotency_key)&#x60; within the dedupe window returns the original Session and token rather than minting a new one.  | [optional] 

## Methods

### NewIssueSessionRequest

`func NewIssueSessionRequest(resourceId string, kind SessionKind, target SessionTarget, ) *IssueSessionRequest`

NewIssueSessionRequest instantiates a new IssueSessionRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewIssueSessionRequestWithDefaults

`func NewIssueSessionRequestWithDefaults() *IssueSessionRequest`

NewIssueSessionRequestWithDefaults instantiates a new IssueSessionRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetResourceId

`func (o *IssueSessionRequest) GetResourceId() string`

GetResourceId returns the ResourceId field if non-nil, zero value otherwise.

### GetResourceIdOk

`func (o *IssueSessionRequest) GetResourceIdOk() (*string, bool)`

GetResourceIdOk returns a tuple with the ResourceId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResourceId

`func (o *IssueSessionRequest) SetResourceId(v string)`

SetResourceId sets ResourceId field to given value.


### GetKind

`func (o *IssueSessionRequest) GetKind() SessionKind`

GetKind returns the Kind field if non-nil, zero value otherwise.

### GetKindOk

`func (o *IssueSessionRequest) GetKindOk() (*SessionKind, bool)`

GetKindOk returns a tuple with the Kind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKind

`func (o *IssueSessionRequest) SetKind(v SessionKind)`

SetKind sets Kind field to given value.


### GetTarget

`func (o *IssueSessionRequest) GetTarget() SessionTarget`

GetTarget returns the Target field if non-nil, zero value otherwise.

### GetTargetOk

`func (o *IssueSessionRequest) GetTargetOk() (*SessionTarget, bool)`

GetTargetOk returns a tuple with the Target field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTarget

`func (o *IssueSessionRequest) SetTarget(v SessionTarget)`

SetTarget sets Target field to given value.


### GetRequestedTtlSeconds

`func (o *IssueSessionRequest) GetRequestedTtlSeconds() int32`

GetRequestedTtlSeconds returns the RequestedTtlSeconds field if non-nil, zero value otherwise.

### GetRequestedTtlSecondsOk

`func (o *IssueSessionRequest) GetRequestedTtlSecondsOk() (*int32, bool)`

GetRequestedTtlSecondsOk returns a tuple with the RequestedTtlSeconds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRequestedTtlSeconds

`func (o *IssueSessionRequest) SetRequestedTtlSeconds(v int32)`

SetRequestedTtlSeconds sets RequestedTtlSeconds field to given value.

### HasRequestedTtlSeconds

`func (o *IssueSessionRequest) HasRequestedTtlSeconds() bool`

HasRequestedTtlSeconds returns a boolean if a field has been set.

### GetIdempotencyKey

`func (o *IssueSessionRequest) GetIdempotencyKey() string`

GetIdempotencyKey returns the IdempotencyKey field if non-nil, zero value otherwise.

### GetIdempotencyKeyOk

`func (o *IssueSessionRequest) GetIdempotencyKeyOk() (*string, bool)`

GetIdempotencyKeyOk returns a tuple with the IdempotencyKey field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIdempotencyKey

`func (o *IssueSessionRequest) SetIdempotencyKey(v string)`

SetIdempotencyKey sets IdempotencyKey field to given value.

### HasIdempotencyKey

`func (o *IssueSessionRequest) HasIdempotencyKey() bool`

HasIdempotencyKey returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


