# DefenseSummary

Summary of RAGDefender behavior for response.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**applied** | **bool** |  | 
**success** | **bool** |  | 
**error** | **str** |  | 
**removed_indices** | **List[int]** |  | 
**risk_scores** | **List[float]** |  | 
**processing_time_ms** | **float** |  | 

## Example

```python
from sami_rag_client.models.defense_summary import DefenseSummary

# TODO update the JSON string below
json = "{}"
# create an instance of DefenseSummary from a JSON string
defense_summary_instance = DefenseSummary.from_json(json)
# print the JSON string representation of the object
print(DefenseSummary.to_json())

# convert the object into a dict
defense_summary_dict = defense_summary_instance.to_dict()
# create an instance of DefenseSummary from a dict
defense_summary_from_dict = DefenseSummary.from_dict(defense_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


