# RagQueryRequest

Request body for RAG query.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**query** | **str** | User query | 
**top_k** | **int** | Number of documents to retrieve (mock retriever) | [optional] [default to 10]
**channel** | **str** | Channel identifier (web, api, mobile, etc.) | [optional] 
**retriever_backend** | **str** |  | [optional] 

## Example

```python
from sami_rag_client.models.rag_query_request import RagQueryRequest

# TODO update the JSON string below
json = "{}"
# create an instance of RagQueryRequest from a JSON string
rag_query_request_instance = RagQueryRequest.from_json(json)
# print the JSON string representation of the object
print(RagQueryRequest.to_json())

# convert the object into a dict
rag_query_request_dict = rag_query_request_instance.to_dict()
# create an instance of RagQueryRequest from a dict
rag_query_request_from_dict = RagQueryRequest.from_dict(rag_query_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


