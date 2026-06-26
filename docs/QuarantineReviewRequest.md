# QuarantineReviewRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**reason** | **str** | Reviewer reason for approve/reject action | [optional] 
**retriever_backend** | **str** |  | [optional] 
**incident_id** | **str** |  | [optional] 
**bucket** | **str** |  | [optional] 
**data_source_id** | **str** |  | [optional] 

## Example

```python
from sami_rag_client.models.quarantine_review_request import QuarantineReviewRequest

# TODO update the JSON string below
json = "{}"
# create an instance of QuarantineReviewRequest from a JSON string
quarantine_review_request_instance = QuarantineReviewRequest.from_json(json)
# print the JSON string representation of the object
print(QuarantineReviewRequest.to_json())

# convert the object into a dict
quarantine_review_request_dict = quarantine_review_request_instance.to_dict()
# create an instance of QuarantineReviewRequest from a dict
quarantine_review_request_from_dict = QuarantineReviewRequest.from_dict(quarantine_review_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


