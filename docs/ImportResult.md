# ImportResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Outcomes** | [**[]ImportOutcome**](ImportOutcome.md) | One entry per requested Blueprint slug. | 

## Methods

### NewImportResult

`func NewImportResult(outcomes []ImportOutcome, ) *ImportResult`

NewImportResult instantiates a new ImportResult object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewImportResultWithDefaults

`func NewImportResultWithDefaults() *ImportResult`

NewImportResultWithDefaults instantiates a new ImportResult object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetOutcomes

`func (o *ImportResult) GetOutcomes() []ImportOutcome`

GetOutcomes returns the Outcomes field if non-nil, zero value otherwise.

### GetOutcomesOk

`func (o *ImportResult) GetOutcomesOk() (*[]ImportOutcome, bool)`

GetOutcomesOk returns a tuple with the Outcomes field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOutcomes

`func (o *ImportResult) SetOutcomes(v []ImportOutcome)`

SetOutcomes sets Outcomes field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


