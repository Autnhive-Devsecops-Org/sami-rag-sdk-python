# DefendResponseModel

Response model for /v1/defend endpoint.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**clean_documents** | **List[str]** |  | 
**kept_indices** | **List[int]** |  | 
**removed_indices** | **List[int]** |  | 
**document_scores** | [**List[DocumentScoreModel]**](DocumentScoreModel.md) |  | 
**stats** | **Dict[str, object]** |  | 
**request_id** | **str** |  | [optional] 
**processing_time_ms** | **float** |  | 
**error** | **str** |  | [optional] 

## Example

```python
from sami_rag_client.models.defend_response_model import DefendResponseModel

# TODO update the JSON string below
json = "{}"
# create an instance of DefendResponseModel from a JSON string
defend_response_model_instance = DefendResponseModel.from_json(json)
# print the JSON string representation of the object
print(DefendResponseModel.to_json())

# convert the object into a dict
defend_response_model_dict = defend_response_model_instance.to_dict()
# create an instance of DefendResponseModel from a dict
defend_response_model_from_dict = DefendResponseModel.from_dict(defend_response_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


