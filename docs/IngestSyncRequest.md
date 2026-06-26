# IngestSyncRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tenant_id** | **str** |  | [optional] 
**app_id** | **str** |  | [optional] 
**store_quarantine** | **bool** |  | [optional] [default to True]
**bucket** | **str** |  | [optional] 
**data_source_id** | **str** |  | [optional] 
**files** | **List[str]** |  | [optional] 

## Example

```python
from sami_rag_client.models.ingest_sync_request import IngestSyncRequest

# TODO update the JSON string below
json = "{}"
# create an instance of IngestSyncRequest from a JSON string
ingest_sync_request_instance = IngestSyncRequest.from_json(json)
# print the JSON string representation of the object
print(IngestSyncRequest.to_json())

# convert the object into a dict
ingest_sync_request_dict = ingest_sync_request_instance.to_dict()
# create an instance of IngestSyncRequest from a dict
ingest_sync_request_from_dict = IngestSyncRequest.from_dict(ingest_sync_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


