# QuarantineReviewResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**doc_id** | **str** |  | 
**previous_status** | **str** |  | 
**new_status** | **str** |  | 
**indexed** | **bool** |  | [optional] [default to False]
**index_error** | **str** |  | [optional] 
**review** | **Dict[str, object]** |  | [optional] 

## Example

```python
from sami_rag_client.models.quarantine_review_response import QuarantineReviewResponse

# TODO update the JSON string below
json = "{}"
# create an instance of QuarantineReviewResponse from a JSON string
quarantine_review_response_instance = QuarantineReviewResponse.from_json(json)
# print the JSON string representation of the object
print(QuarantineReviewResponse.to_json())

# convert the object into a dict
quarantine_review_response_dict = quarantine_review_response_instance.to_dict()
# create an instance of QuarantineReviewResponse from a dict
quarantine_review_response_from_dict = QuarantineReviewResponse.from_dict(quarantine_review_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


