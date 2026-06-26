# IngestCommitResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**accepted** | **int** |  | 
**quarantined** | **int** |  | 
**rejected** | **int** |  | 
**accepted_doc_ids** | **List[str]** |  | 
**quarantined_doc_ids** | **List[str]** |  | 
**rejected_doc_ids** | **List[str]** |  | 

## Example

```python
from sami_rag_client.models.ingest_commit_response import IngestCommitResponse

# TODO update the JSON string below
json = "{}"
# create an instance of IngestCommitResponse from a JSON string
ingest_commit_response_instance = IngestCommitResponse.from_json(json)
# print the JSON string representation of the object
print(IngestCommitResponse.to_json())

# convert the object into a dict
ingest_commit_response_dict = ingest_commit_response_instance.to_dict()
# create an instance of IngestCommitResponse from a dict
ingest_commit_response_from_dict = IngestCommitResponse.from_dict(ingest_commit_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


