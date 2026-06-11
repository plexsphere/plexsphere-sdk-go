# NodeStateReports

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Metadata** | [**[]StateEntry**](StateEntry.md) | Operator-visible, platform-owned metadata entries for the addressed Node, ordered by &#x60;key&#x60; ascending.  | 
**Data** | [**[]StateEntry**](StateEntry.md) | Platform-owned operational data entries for the addressed Node, ordered by &#x60;key&#x60; ascending.  | 
**Reports** | [**[]StateEntry**](StateEntry.md) | Upstream, workload-authored report entries for the addressed Node, ordered by &#x60;key&#x60; ascending.  | 

## Methods

### NewNodeStateReports

`func NewNodeStateReports(metadata []StateEntry, data []StateEntry, reports []StateEntry, ) *NodeStateReports`

NewNodeStateReports instantiates a new NodeStateReports object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewNodeStateReportsWithDefaults

`func NewNodeStateReportsWithDefaults() *NodeStateReports`

NewNodeStateReportsWithDefaults instantiates a new NodeStateReports object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetMetadata

`func (o *NodeStateReports) GetMetadata() []StateEntry`

GetMetadata returns the Metadata field if non-nil, zero value otherwise.

### GetMetadataOk

`func (o *NodeStateReports) GetMetadataOk() (*[]StateEntry, bool)`

GetMetadataOk returns a tuple with the Metadata field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMetadata

`func (o *NodeStateReports) SetMetadata(v []StateEntry)`

SetMetadata sets Metadata field to given value.


### GetData

`func (o *NodeStateReports) GetData() []StateEntry`

GetData returns the Data field if non-nil, zero value otherwise.

### GetDataOk

`func (o *NodeStateReports) GetDataOk() (*[]StateEntry, bool)`

GetDataOk returns a tuple with the Data field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetData

`func (o *NodeStateReports) SetData(v []StateEntry)`

SetData sets Data field to given value.


### GetReports

`func (o *NodeStateReports) GetReports() []StateEntry`

GetReports returns the Reports field if non-nil, zero value otherwise.

### GetReportsOk

`func (o *NodeStateReports) GetReportsOk() (*[]StateEntry, bool)`

GetReportsOk returns a tuple with the Reports field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetReports

`func (o *NodeStateReports) SetReports(v []StateEntry)`

SetReports sets Reports field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


