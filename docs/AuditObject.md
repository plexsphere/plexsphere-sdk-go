# AuditObject

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** | SpiceDB object type (e.g. &#x60;domain&#x60;, &#x60;node&#x60;, &#x60;resource&#x60;). | 
**Id** | **string** | Opaque object identifier within &#x60;type&#x60;. | 

## Methods

### NewAuditObject

`func NewAuditObject(type_ string, id string, ) *AuditObject`

NewAuditObject instantiates a new AuditObject object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewAuditObjectWithDefaults

`func NewAuditObjectWithDefaults() *AuditObject`

NewAuditObjectWithDefaults instantiates a new AuditObject object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetType

`func (o *AuditObject) GetType() string`

GetType returns the Type field if non-nil, zero value otherwise.

### GetTypeOk

`func (o *AuditObject) GetTypeOk() (*string, bool)`

GetTypeOk returns a tuple with the Type field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetType

`func (o *AuditObject) SetType(v string)`

SetType sets Type field to given value.


### GetId

`func (o *AuditObject) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *AuditObject) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *AuditObject) SetId(v string)`

SetId sets Id field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


