# FileUrlIngestRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tenant_id** | **str** |  | [optional] 
**app_id** | **str** |  | [optional] 
**doc_id** | **str** | Optional public document identifier. If omitted, a stable ID is derived from the file URL. | [optional] 
**file_url** | **str** |  | 
**metadata** | **Dict[str, object]** |  | [optional] 
**store_quarantine** | **bool** |  | [optional] [default to True]
**retriever_backend** | **str** |  | [optional] 

## Example

```python
from sami_rag_client.models.file_url_ingest_request import FileUrlIngestRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FileUrlIngestRequest from a JSON string
file_url_ingest_request_instance = FileUrlIngestRequest.from_json(json)
# print the JSON string representation of the object
print(FileUrlIngestRequest.to_json())

# convert the object into a dict
file_url_ingest_request_dict = file_url_ingest_request_instance.to_dict()
# create an instance of FileUrlIngestRequest from a dict
file_url_ingest_request_from_dict = FileUrlIngestRequest.from_dict(file_url_ingest_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


