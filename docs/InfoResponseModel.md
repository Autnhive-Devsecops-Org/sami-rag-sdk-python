# InfoResponseModel

Response model for /info endpoint.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**version** | **str** |  | 
**description** | **str** |  | 
**supported_modes** | **List[str]** |  | 
**device** | **str** |  | 
**model** | **str** |  | 

## Example

```python
from sami_rag_client.models.info_response_model import InfoResponseModel

# TODO update the JSON string below
json = "{}"
# create an instance of InfoResponseModel from a JSON string
info_response_model_instance = InfoResponseModel.from_json(json)
# print the JSON string representation of the object
print(InfoResponseModel.to_json())

# convert the object into a dict
info_response_model_dict = info_response_model_instance.to_dict()
# create an instance of InfoResponseModel from a dict
info_response_model_from_dict = InfoResponseModel.from_dict(info_response_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


