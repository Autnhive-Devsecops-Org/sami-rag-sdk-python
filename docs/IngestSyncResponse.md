# IngestSyncResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**source_adapter** | **str** |  | 
**synced_count** | **int** |  | 
**accepted** | **int** |  | 
**quarantined** | **int** |  | 
**rejected** | **int** |  | 
**accepted_doc_ids** | **List[str]** |  | 
**quarantined_doc_ids** | **List[str]** |  | 
**rejected_doc_ids** | **List[str]** |  | 

## Example

```python
from sami_rag_client.models.ingest_sync_response import IngestSyncResponse

# TODO update the JSON string below
json = "{}"
# create an instance of IngestSyncResponse from a JSON string
ingest_sync_response_instance = IngestSyncResponse.from_json(json)
# print the JSON string representation of the object
print(IngestSyncResponse.to_json())

# convert the object into a dict
ingest_sync_response_dict = ingest_sync_response_instance.to_dict()
# create an instance of IngestSyncResponse from a dict
ingest_sync_response_from_dict = IngestSyncResponse.from_dict(ingest_sync_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


