# PermissionDenied

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** | URI reference that identifies the problem type. | 
**Title** | **string** | Short, human-readable summary of the problem. | 
**Status** | **int32** | HTTP status code generated for this occurrence (always 403). | 
**Detail** | **string** | Human-readable explanation for this occurrence. | 
**Instance** | **string** | URI reference identifying the specific occurrence. | 
**Code** | Pointer to **string** | Optional machine-readable error code (shared with &#x60;Problem&#x60;).  | [optional] 
**Reason** | [**PermissionDeniedReason**](PermissionDeniedReason.md) |  | 
**RelationPath** | Pointer to **[]string** | Ordered sequence of relations the authorizer traversed while evaluating the Check. Empty when the denial was decided before any relation lookup (typically &#x60;out_of_scope&#x60;).  | [optional] 
**CorrelationId** | **string** | Correlation id that pairs this denial with the matching audit entry emitted by &#x60;internal/audit&#x60;.  | 

## Methods

### NewPermissionDenied

`func NewPermissionDenied(type_ string, title string, status int32, detail string, instance string, reason PermissionDeniedReason, correlationId string, ) *PermissionDenied`

NewPermissionDenied instantiates a new PermissionDenied object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewPermissionDeniedWithDefaults

`func NewPermissionDeniedWithDefaults() *PermissionDenied`

NewPermissionDeniedWithDefaults instantiates a new PermissionDenied object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetType

`func (o *PermissionDenied) GetType() string`

GetType returns the Type field if non-nil, zero value otherwise.

### GetTypeOk

`func (o *PermissionDenied) GetTypeOk() (*string, bool)`

GetTypeOk returns a tuple with the Type field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetType

`func (o *PermissionDenied) SetType(v string)`

SetType sets Type field to given value.


### GetTitle

`func (o *PermissionDenied) GetTitle() string`

GetTitle returns the Title field if non-nil, zero value otherwise.

### GetTitleOk

`func (o *PermissionDenied) GetTitleOk() (*string, bool)`

GetTitleOk returns a tuple with the Title field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTitle

`func (o *PermissionDenied) SetTitle(v string)`

SetTitle sets Title field to given value.


### GetStatus

`func (o *PermissionDenied) GetStatus() int32`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *PermissionDenied) GetStatusOk() (*int32, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *PermissionDenied) SetStatus(v int32)`

SetStatus sets Status field to given value.


### GetDetail

`func (o *PermissionDenied) GetDetail() string`

GetDetail returns the Detail field if non-nil, zero value otherwise.

### GetDetailOk

`func (o *PermissionDenied) GetDetailOk() (*string, bool)`

GetDetailOk returns a tuple with the Detail field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDetail

`func (o *PermissionDenied) SetDetail(v string)`

SetDetail sets Detail field to given value.


### GetInstance

`func (o *PermissionDenied) GetInstance() string`

GetInstance returns the Instance field if non-nil, zero value otherwise.

### GetInstanceOk

`func (o *PermissionDenied) GetInstanceOk() (*string, bool)`

GetInstanceOk returns a tuple with the Instance field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetInstance

`func (o *PermissionDenied) SetInstance(v string)`

SetInstance sets Instance field to given value.


### GetCode

`func (o *PermissionDenied) GetCode() string`

GetCode returns the Code field if non-nil, zero value otherwise.

### GetCodeOk

`func (o *PermissionDenied) GetCodeOk() (*string, bool)`

GetCodeOk returns a tuple with the Code field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCode

`func (o *PermissionDenied) SetCode(v string)`

SetCode sets Code field to given value.

### HasCode

`func (o *PermissionDenied) HasCode() bool`

HasCode returns a boolean if a field has been set.

### GetReason

`func (o *PermissionDenied) GetReason() PermissionDeniedReason`

GetReason returns the Reason field if non-nil, zero value otherwise.

### GetReasonOk

`func (o *PermissionDenied) GetReasonOk() (*PermissionDeniedReason, bool)`

GetReasonOk returns a tuple with the Reason field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetReason

`func (o *PermissionDenied) SetReason(v PermissionDeniedReason)`

SetReason sets Reason field to given value.


### GetRelationPath

`func (o *PermissionDenied) GetRelationPath() []string`

GetRelationPath returns the RelationPath field if non-nil, zero value otherwise.

### GetRelationPathOk

`func (o *PermissionDenied) GetRelationPathOk() (*[]string, bool)`

GetRelationPathOk returns a tuple with the RelationPath field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRelationPath

`func (o *PermissionDenied) SetRelationPath(v []string)`

SetRelationPath sets RelationPath field to given value.

### HasRelationPath

`func (o *PermissionDenied) HasRelationPath() bool`

HasRelationPath returns a boolean if a field has been set.

### GetCorrelationId

`func (o *PermissionDenied) GetCorrelationId() string`

GetCorrelationId returns the CorrelationId field if non-nil, zero value otherwise.

### GetCorrelationIdOk

`func (o *PermissionDenied) GetCorrelationIdOk() (*string, bool)`

GetCorrelationIdOk returns a tuple with the CorrelationId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCorrelationId

`func (o *PermissionDenied) SetCorrelationId(v string)`

SetCorrelationId sets CorrelationId field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


