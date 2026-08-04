# HeartbeatRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ClientNow** | **time.Time** | Client wall-clock timestamp at the moment the heartbeat was assembled. The handler rejects the request with 400 &#x60;clock_skew&#x60; if the value drifts more than 60 seconds from server now.  | 
**BinaryChecksum** | **string** | SHA-256 digest of the running plexd binary, 32 bytes base64-encoded with standard padding (44 characters). Anything that does not decode to exactly 32 bytes is rejected with 400 &#x60;binary_checksum_empty&#x60;.  Base64 is the only accepted encoding, here and on &#x60;CapabilityManifestRequest.binary_checksum&#x60; and &#x60;DeclaredHook.checksum&#x60;. An earlier revision of this description also offered lowercase hex; no handler ever decoded it. &#x60;format: byte&#x60; means the generated server type is &#x60;[]byte&#x60; and the JSON decoder base64-decodes the value before any handler sees it, so a 64-character hex digest — itself valid base64 — arrives as 48 bytes and fails the length check with a message about the byte count that never mentions the encoding. The offer is withdrawn rather than implemented so one encoding holds across every checksum field on the node-facing surface.  | 
**BinaryVersion** | **string** | Human-readable plexd version string (e.g. &#x60;plexd-v0.4.2-ge5f3a1c&#x60;). Non-empty per the application- boundary invariants — the handler rejects an empty value with 400 &#x60;binary_version_empty&#x60;.  | 
**NatSummary** | **map[string]interface{}** | Free-form NAT discovery summary produced by plexd. Empty object is permitted — later stories define the schema once the per-Domain bridge orchestrator lands.  | 

## Methods

### NewHeartbeatRequest

`func NewHeartbeatRequest(clientNow time.Time, binaryChecksum string, binaryVersion string, natSummary map[string]interface{}, ) *HeartbeatRequest`

NewHeartbeatRequest instantiates a new HeartbeatRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewHeartbeatRequestWithDefaults

`func NewHeartbeatRequestWithDefaults() *HeartbeatRequest`

NewHeartbeatRequestWithDefaults instantiates a new HeartbeatRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetClientNow

`func (o *HeartbeatRequest) GetClientNow() time.Time`

GetClientNow returns the ClientNow field if non-nil, zero value otherwise.

### GetClientNowOk

`func (o *HeartbeatRequest) GetClientNowOk() (*time.Time, bool)`

GetClientNowOk returns a tuple with the ClientNow field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetClientNow

`func (o *HeartbeatRequest) SetClientNow(v time.Time)`

SetClientNow sets ClientNow field to given value.


### GetBinaryChecksum

`func (o *HeartbeatRequest) GetBinaryChecksum() string`

GetBinaryChecksum returns the BinaryChecksum field if non-nil, zero value otherwise.

### GetBinaryChecksumOk

`func (o *HeartbeatRequest) GetBinaryChecksumOk() (*string, bool)`

GetBinaryChecksumOk returns a tuple with the BinaryChecksum field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBinaryChecksum

`func (o *HeartbeatRequest) SetBinaryChecksum(v string)`

SetBinaryChecksum sets BinaryChecksum field to given value.


### GetBinaryVersion

`func (o *HeartbeatRequest) GetBinaryVersion() string`

GetBinaryVersion returns the BinaryVersion field if non-nil, zero value otherwise.

### GetBinaryVersionOk

`func (o *HeartbeatRequest) GetBinaryVersionOk() (*string, bool)`

GetBinaryVersionOk returns a tuple with the BinaryVersion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBinaryVersion

`func (o *HeartbeatRequest) SetBinaryVersion(v string)`

SetBinaryVersion sets BinaryVersion field to given value.


### GetNatSummary

`func (o *HeartbeatRequest) GetNatSummary() map[string]interface{}`

GetNatSummary returns the NatSummary field if non-nil, zero value otherwise.

### GetNatSummaryOk

`func (o *HeartbeatRequest) GetNatSummaryOk() (*map[string]interface{}, bool)`

GetNatSummaryOk returns a tuple with the NatSummary field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNatSummary

`func (o *HeartbeatRequest) SetNatSummary(v map[string]interface{})`

SetNatSummary sets NatSummary field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


