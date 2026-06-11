# IngestReceipt

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AcceptedAt** | **time.Time** | Server-side timestamp at which the batch was accepted and handed to the ingest buffer.  | 
**Records** | **int32** | Number of records accepted from the batch. Matches the number of array elements (metrics) or non-blank NDJSON lines (logs / audit) on input.  | 

## Methods

### NewIngestReceipt

`func NewIngestReceipt(acceptedAt time.Time, records int32, ) *IngestReceipt`

NewIngestReceipt instantiates a new IngestReceipt object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewIngestReceiptWithDefaults

`func NewIngestReceiptWithDefaults() *IngestReceipt`

NewIngestReceiptWithDefaults instantiates a new IngestReceipt object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetAcceptedAt

`func (o *IngestReceipt) GetAcceptedAt() time.Time`

GetAcceptedAt returns the AcceptedAt field if non-nil, zero value otherwise.

### GetAcceptedAtOk

`func (o *IngestReceipt) GetAcceptedAtOk() (*time.Time, bool)`

GetAcceptedAtOk returns a tuple with the AcceptedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAcceptedAt

`func (o *IngestReceipt) SetAcceptedAt(v time.Time)`

SetAcceptedAt sets AcceptedAt field to given value.


### GetRecords

`func (o *IngestReceipt) GetRecords() int32`

GetRecords returns the Records field if non-nil, zero value otherwise.

### GetRecordsOk

`func (o *IngestReceipt) GetRecordsOk() (*int32, bool)`

GetRecordsOk returns a tuple with the Records field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRecords

`func (o *IngestReceipt) SetRecords(v int32)`

SetRecords sets Records field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


