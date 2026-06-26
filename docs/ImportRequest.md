# ImportRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Slugs** | Pointer to **[]string** | The subset of offered Blueprint slugs to import. Mutually exclusive with &#x60;all&#x60;; must be non-empty when present and may carry at most 256 entries — the server caps the per-request import subset so one call cannot fan out into an unbounded number of upstream registry round-trips.  | [optional] 
**All** | Pointer to **bool** | Import every Blueprint the source offers. Mutually exclusive with &#x60;slugs&#x60;.  | [optional] 

## Methods

### NewImportRequest

`func NewImportRequest() *ImportRequest`

NewImportRequest instantiates a new ImportRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewImportRequestWithDefaults

`func NewImportRequestWithDefaults() *ImportRequest`

NewImportRequestWithDefaults instantiates a new ImportRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSlugs

`func (o *ImportRequest) GetSlugs() []string`

GetSlugs returns the Slugs field if non-nil, zero value otherwise.

### GetSlugsOk

`func (o *ImportRequest) GetSlugsOk() (*[]string, bool)`

GetSlugsOk returns a tuple with the Slugs field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlugs

`func (o *ImportRequest) SetSlugs(v []string)`

SetSlugs sets Slugs field to given value.

### HasSlugs

`func (o *ImportRequest) HasSlugs() bool`

HasSlugs returns a boolean if a field has been set.

### GetAll

`func (o *ImportRequest) GetAll() bool`

GetAll returns the All field if non-nil, zero value otherwise.

### GetAllOk

`func (o *ImportRequest) GetAllOk() (*bool, bool)`

GetAllOk returns a tuple with the All field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAll

`func (o *ImportRequest) SetAll(v bool)`

SetAll sets All field to given value.

### HasAll

`func (o *ImportRequest) HasAll() bool`

HasAll returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


