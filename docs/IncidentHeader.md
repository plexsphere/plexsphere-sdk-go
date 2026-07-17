# IncidentHeader

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable identifier of the incident (UUIDv7). | 
**DomainId** | **string** | Domain the incident is scoped to. | 
**Title** | **string** | Short human-readable title of the incident. | 
**Severity** | [**IncidentSeverity**](IncidentSeverity.md) |  | 
**Status** | [**IncidentStatus**](IncidentStatus.md) |  | 
**OpenedAt** | **time.Time** | RFC 3339 instant the incident was opened. | 
**ResolvedAt** | Pointer to **time.Time** | RFC 3339 instant the incident was resolved, or absent while it is still open.  | [optional] 

## Methods

### NewIncidentHeader

`func NewIncidentHeader(id string, domainId string, title string, severity IncidentSeverity, status IncidentStatus, openedAt time.Time, ) *IncidentHeader`

NewIncidentHeader instantiates a new IncidentHeader object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewIncidentHeaderWithDefaults

`func NewIncidentHeaderWithDefaults() *IncidentHeader`

NewIncidentHeaderWithDefaults instantiates a new IncidentHeader object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *IncidentHeader) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *IncidentHeader) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *IncidentHeader) SetId(v string)`

SetId sets Id field to given value.


### GetDomainId

`func (o *IncidentHeader) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *IncidentHeader) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *IncidentHeader) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.


### GetTitle

`func (o *IncidentHeader) GetTitle() string`

GetTitle returns the Title field if non-nil, zero value otherwise.

### GetTitleOk

`func (o *IncidentHeader) GetTitleOk() (*string, bool)`

GetTitleOk returns a tuple with the Title field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTitle

`func (o *IncidentHeader) SetTitle(v string)`

SetTitle sets Title field to given value.


### GetSeverity

`func (o *IncidentHeader) GetSeverity() IncidentSeverity`

GetSeverity returns the Severity field if non-nil, zero value otherwise.

### GetSeverityOk

`func (o *IncidentHeader) GetSeverityOk() (*IncidentSeverity, bool)`

GetSeverityOk returns a tuple with the Severity field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSeverity

`func (o *IncidentHeader) SetSeverity(v IncidentSeverity)`

SetSeverity sets Severity field to given value.


### GetStatus

`func (o *IncidentHeader) GetStatus() IncidentStatus`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *IncidentHeader) GetStatusOk() (*IncidentStatus, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *IncidentHeader) SetStatus(v IncidentStatus)`

SetStatus sets Status field to given value.


### GetOpenedAt

`func (o *IncidentHeader) GetOpenedAt() time.Time`

GetOpenedAt returns the OpenedAt field if non-nil, zero value otherwise.

### GetOpenedAtOk

`func (o *IncidentHeader) GetOpenedAtOk() (*time.Time, bool)`

GetOpenedAtOk returns a tuple with the OpenedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOpenedAt

`func (o *IncidentHeader) SetOpenedAt(v time.Time)`

SetOpenedAt sets OpenedAt field to given value.


### GetResolvedAt

`func (o *IncidentHeader) GetResolvedAt() time.Time`

GetResolvedAt returns the ResolvedAt field if non-nil, zero value otherwise.

### GetResolvedAtOk

`func (o *IncidentHeader) GetResolvedAtOk() (*time.Time, bool)`

GetResolvedAtOk returns a tuple with the ResolvedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResolvedAt

`func (o *IncidentHeader) SetResolvedAt(v time.Time)`

SetResolvedAt sets ResolvedAt field to given value.

### HasResolvedAt

`func (o *IncidentHeader) HasResolvedAt() bool`

HasResolvedAt returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


