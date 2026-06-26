# Incident

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
**Timeline** | [**[]TimelineEvent**](TimelineEvent.md) | The incident&#39;s append-only timeline, ordered by &#x60;occurred_at&#x60; ascending. The list projection omits the timeline; the single-incident read includes it.  | 

## Methods

### NewIncident

`func NewIncident(id string, domainId string, title string, severity IncidentSeverity, status IncidentStatus, openedAt time.Time, timeline []TimelineEvent, ) *Incident`

NewIncident instantiates a new Incident object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewIncidentWithDefaults

`func NewIncidentWithDefaults() *Incident`

NewIncidentWithDefaults instantiates a new Incident object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *Incident) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *Incident) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *Incident) SetId(v string)`

SetId sets Id field to given value.


### GetDomainId

`func (o *Incident) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *Incident) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *Incident) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.


### GetTitle

`func (o *Incident) GetTitle() string`

GetTitle returns the Title field if non-nil, zero value otherwise.

### GetTitleOk

`func (o *Incident) GetTitleOk() (*string, bool)`

GetTitleOk returns a tuple with the Title field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTitle

`func (o *Incident) SetTitle(v string)`

SetTitle sets Title field to given value.


### GetSeverity

`func (o *Incident) GetSeverity() IncidentSeverity`

GetSeverity returns the Severity field if non-nil, zero value otherwise.

### GetSeverityOk

`func (o *Incident) GetSeverityOk() (*IncidentSeverity, bool)`

GetSeverityOk returns a tuple with the Severity field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSeverity

`func (o *Incident) SetSeverity(v IncidentSeverity)`

SetSeverity sets Severity field to given value.


### GetStatus

`func (o *Incident) GetStatus() IncidentStatus`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *Incident) GetStatusOk() (*IncidentStatus, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *Incident) SetStatus(v IncidentStatus)`

SetStatus sets Status field to given value.


### GetOpenedAt

`func (o *Incident) GetOpenedAt() time.Time`

GetOpenedAt returns the OpenedAt field if non-nil, zero value otherwise.

### GetOpenedAtOk

`func (o *Incident) GetOpenedAtOk() (*time.Time, bool)`

GetOpenedAtOk returns a tuple with the OpenedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOpenedAt

`func (o *Incident) SetOpenedAt(v time.Time)`

SetOpenedAt sets OpenedAt field to given value.


### GetResolvedAt

`func (o *Incident) GetResolvedAt() time.Time`

GetResolvedAt returns the ResolvedAt field if non-nil, zero value otherwise.

### GetResolvedAtOk

`func (o *Incident) GetResolvedAtOk() (*time.Time, bool)`

GetResolvedAtOk returns a tuple with the ResolvedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResolvedAt

`func (o *Incident) SetResolvedAt(v time.Time)`

SetResolvedAt sets ResolvedAt field to given value.

### HasResolvedAt

`func (o *Incident) HasResolvedAt() bool`

HasResolvedAt returns a boolean if a field has been set.

### GetTimeline

`func (o *Incident) GetTimeline() []TimelineEvent`

GetTimeline returns the Timeline field if non-nil, zero value otherwise.

### GetTimelineOk

`func (o *Incident) GetTimelineOk() (*[]TimelineEvent, bool)`

GetTimelineOk returns a tuple with the Timeline field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTimeline

`func (o *Incident) SetTimeline(v []TimelineEvent)`

SetTimeline sets Timeline field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


