# RagQueryResponse

Response body for RAG query.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**request_id** | **str** |  | 
**tenant_id** | **str** |  | 
**app_id** | **str** |  | 
**query** | **str** |  | 
**answer** | **str** |  | 
**context_docs** | **List[str]** |  | 
**defense** | [**DefenseSummary**](DefenseSummary.md) |  | 
**policy_enforcement** | [**PolicyEnforcementSummary**](PolicyEnforcementSummary.md) |  | 

## Example

```python
from sami_rag_client.models.rag_query_response import RagQueryResponse

# TODO update the JSON string below
json = "{}"
# create an instance of RagQueryResponse from a JSON string
rag_query_response_instance = RagQueryResponse.from_json(json)
# print the JSON string representation of the object
print(RagQueryResponse.to_json())

# convert the object into a dict
rag_query_response_dict = rag_query_response_instance.to_dict()
# create an instance of RagQueryResponse from a dict
rag_query_response_from_dict = RagQueryResponse.from_dict(rag_query_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


