# CatalogSourceResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Catalog source identifier (UUIDv7). | 
**Name** | **string** | Human-facing label. | 
**OciReference** | [**OciReference**](OciReference.md) |  | 
**Verification** | [**VerificationPolicy**](VerificationPolicy.md) |  | 
**Tracking** | [**TrackingPolicy**](TrackingPolicy.md) |  | 
**CredentialRef** | Pointer to **string** | &#x60;namespace/name&#x60; reference to the registry-credential Secret, or &#x60;null&#x60; when the source needs none.  | [optional] 
**DomainId** | Pointer to **string** | Owning Domain, or &#x60;null&#x60; for a catalog-global source.  | [optional] 
**LastResolvedDigest** | Pointer to **string** | The bundle digest the source last resolved to, or &#x60;null&#x60; before the first resolution.  | [optional] 
**Status** | [**CatalogSourceResponseStatus**](CatalogSourceResponseStatus.md) |  | 
**CreatedAt** | **time.Time** | Catalog source creation timestamp (UTC). | 
**UpdatedAt** | **time.Time** | Last-modified timestamp (UTC). | 

## Methods

### NewCatalogSourceResponse

`func NewCatalogSourceResponse(id string, name string, ociReference OciReference, verification VerificationPolicy, tracking TrackingPolicy, status CatalogSourceResponseStatus, createdAt time.Time, updatedAt time.Time, ) *CatalogSourceResponse`

NewCatalogSourceResponse instantiates a new CatalogSourceResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCatalogSourceResponseWithDefaults

`func NewCatalogSourceResponseWithDefaults() *CatalogSourceResponse`

NewCatalogSourceResponseWithDefaults instantiates a new CatalogSourceResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *CatalogSourceResponse) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *CatalogSourceResponse) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *CatalogSourceResponse) SetId(v string)`

SetId sets Id field to given value.


### GetName

`func (o *CatalogSourceResponse) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *CatalogSourceResponse) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *CatalogSourceResponse) SetName(v string)`

SetName sets Name field to given value.


### GetOciReference

`func (o *CatalogSourceResponse) GetOciReference() OciReference`

GetOciReference returns the OciReference field if non-nil, zero value otherwise.

### GetOciReferenceOk

`func (o *CatalogSourceResponse) GetOciReferenceOk() (*OciReference, bool)`

GetOciReferenceOk returns a tuple with the OciReference field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOciReference

`func (o *CatalogSourceResponse) SetOciReference(v OciReference)`

SetOciReference sets OciReference field to given value.


### GetVerification

`func (o *CatalogSourceResponse) GetVerification() VerificationPolicy`

GetVerification returns the Verification field if non-nil, zero value otherwise.

### GetVerificationOk

`func (o *CatalogSourceResponse) GetVerificationOk() (*VerificationPolicy, bool)`

GetVerificationOk returns a tuple with the Verification field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetVerification

`func (o *CatalogSourceResponse) SetVerification(v VerificationPolicy)`

SetVerification sets Verification field to given value.


### GetTracking

`func (o *CatalogSourceResponse) GetTracking() TrackingPolicy`

GetTracking returns the Tracking field if non-nil, zero value otherwise.

### GetTrackingOk

`func (o *CatalogSourceResponse) GetTrackingOk() (*TrackingPolicy, bool)`

GetTrackingOk returns a tuple with the Tracking field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTracking

`func (o *CatalogSourceResponse) SetTracking(v TrackingPolicy)`

SetTracking sets Tracking field to given value.


### GetCredentialRef

`func (o *CatalogSourceResponse) GetCredentialRef() string`

GetCredentialRef returns the CredentialRef field if non-nil, zero value otherwise.

### GetCredentialRefOk

`func (o *CatalogSourceResponse) GetCredentialRefOk() (*string, bool)`

GetCredentialRefOk returns a tuple with the CredentialRef field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCredentialRef

`func (o *CatalogSourceResponse) SetCredentialRef(v string)`

SetCredentialRef sets CredentialRef field to given value.

### HasCredentialRef

`func (o *CatalogSourceResponse) HasCredentialRef() bool`

HasCredentialRef returns a boolean if a field has been set.

### GetDomainId

`func (o *CatalogSourceResponse) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *CatalogSourceResponse) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *CatalogSourceResponse) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.

### HasDomainId

`func (o *CatalogSourceResponse) HasDomainId() bool`

HasDomainId returns a boolean if a field has been set.

### GetLastResolvedDigest

`func (o *CatalogSourceResponse) GetLastResolvedDigest() string`

GetLastResolvedDigest returns the LastResolvedDigest field if non-nil, zero value otherwise.

### GetLastResolvedDigestOk

`func (o *CatalogSourceResponse) GetLastResolvedDigestOk() (*string, bool)`

GetLastResolvedDigestOk returns a tuple with the LastResolvedDigest field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLastResolvedDigest

`func (o *CatalogSourceResponse) SetLastResolvedDigest(v string)`

SetLastResolvedDigest sets LastResolvedDigest field to given value.

### HasLastResolvedDigest

`func (o *CatalogSourceResponse) HasLastResolvedDigest() bool`

HasLastResolvedDigest returns a boolean if a field has been set.

### GetStatus

`func (o *CatalogSourceResponse) GetStatus() CatalogSourceResponseStatus`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *CatalogSourceResponse) GetStatusOk() (*CatalogSourceResponseStatus, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *CatalogSourceResponse) SetStatus(v CatalogSourceResponseStatus)`

SetStatus sets Status field to given value.


### GetCreatedAt

`func (o *CatalogSourceResponse) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *CatalogSourceResponse) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *CatalogSourceResponse) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetUpdatedAt

`func (o *CatalogSourceResponse) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *CatalogSourceResponse) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *CatalogSourceResponse) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


