# PolicyEnforcementSummary


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**policy_mode** | **str** |  | 
**blocked** | **bool** |  | 
**reason** | **str** |  | 
**retriever_backend** | **str** |  | [optional] 
**legacy_backfill_required** | **bool** |  | [optional] [default to True]
**legacy_backfill_completed** | **bool** |  | [optional] [default to False]
**risk_acknowledged_at** | **str** |  | [optional] 

## Example

```python
from sami_rag_client.models.policy_enforcement_summary import PolicyEnforcementSummary

# TODO update the JSON string below
json = "{}"
# create an instance of PolicyEnforcementSummary from a JSON string
policy_enforcement_summary_instance = PolicyEnforcementSummary.from_json(json)
# print the JSON string representation of the object
print(PolicyEnforcementSummary.to_json())

# convert the object into a dict
policy_enforcement_summary_dict = policy_enforcement_summary_instance.to_dict()
# create an instance of PolicyEnforcementSummary from a dict
policy_enforcement_summary_from_dict = PolicyEnforcementSummary.from_dict(policy_enforcement_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


