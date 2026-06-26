# HealthResponseModel

Response model for /health endpoint.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** |  | 
**version** | **str** |  | 
**model_loaded** | **bool** |  | 
**device** | **str** |  | 
**uptime_seconds** | **float** |  | 
**total_requests** | **int** |  | 
**avg_latency_ms** | **float** |  | 

## Example

```python
from sami_rag_client.models.health_response_model import HealthResponseModel

# TODO update the JSON string below
json = "{}"
# create an instance of HealthResponseModel from a JSON string
health_response_model_instance = HealthResponseModel.from_json(json)
# print the JSON string representation of the object
print(HealthResponseModel.to_json())

# convert the object into a dict
health_response_model_dict = health_response_model_instance.to_dict()
# create an instance of HealthResponseModel from a dict
health_response_model_from_dict = HealthResponseModel.from_dict(health_response_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


