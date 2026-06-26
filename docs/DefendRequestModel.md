# DefendRequestModel

Request model for /v1/defend endpoint.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**query** | **str** | The query string | 
**documents** | **List[str]** | List of retrieved documents | 
**mode** | **str** | Defense mode | [optional] [default to 'multihop']
**top_k** | **int** | Number of documents to return | [optional] 
**tenant_id** | **str** | Tenant identifier | [optional] 
**metadata** | **Dict[str, object]** | Additional metadata | [optional] 

## Example

```python
from sami_rag_client.models.defend_request_model import DefendRequestModel

# TODO update the JSON string below
json = "{}"
# create an instance of DefendRequestModel from a JSON string
defend_request_model_instance = DefendRequestModel.from_json(json)
# print the JSON string representation of the object
print(DefendRequestModel.to_json())

# convert the object into a dict
defend_request_model_dict = defend_request_model_instance.to_dict()
# create an instance of DefendRequestModel from a dict
defend_request_model_from_dict = DefendRequestModel.from_dict(defend_request_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


