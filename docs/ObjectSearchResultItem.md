# ObjectSearchResultItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Kind** | **string** | Lowercase object-kind discriminator (e.g. &#x60;project&#x60;, &#x60;node&#x60;). | 
**Id** | **string** | Object UUID. | 

## Methods

### NewObjectSearchResultItem

`func NewObjectSearchResultItem(kind string, id string, ) *ObjectSearchResultItem`

NewObjectSearchResultItem instantiates a new ObjectSearchResultItem object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewObjectSearchResultItemWithDefaults

`func NewObjectSearchResultItemWithDefaults() *ObjectSearchResultItem`

NewObjectSearchResultItemWithDefaults instantiates a new ObjectSearchResultItem object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetKind

`func (o *ObjectSearchResultItem) GetKind() string`

GetKind returns the Kind field if non-nil, zero value otherwise.

### GetKindOk

`func (o *ObjectSearchResultItem) GetKindOk() (*string, bool)`

GetKindOk returns a tuple with the Kind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKind

`func (o *ObjectSearchResultItem) SetKind(v string)`

SetKind sets Kind field to given value.


### GetId

`func (o *ObjectSearchResultItem) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *ObjectSearchResultItem) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *ObjectSearchResultItem) SetId(v string)`

SetId sets Id field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


