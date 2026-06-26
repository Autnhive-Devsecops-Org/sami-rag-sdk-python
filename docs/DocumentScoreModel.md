# DocumentScoreModel

Score information for a document.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**index** | **int** |  | 
**risk_score** | **float** |  | 
**is_removed** | **bool** |  | 
**reason** | **str** |  | [optional] 

## Example

```python
from sami_rag_client.models.document_score_model import DocumentScoreModel

# TODO update the JSON string below
json = "{}"
# create an instance of DocumentScoreModel from a JSON string
document_score_model_instance = DocumentScoreModel.from_json(json)
# print the JSON string representation of the object
print(DocumentScoreModel.to_json())

# convert the object into a dict
document_score_model_dict = document_score_model_instance.to_dict()
# create an instance of DocumentScoreModel from a dict
document_score_model_from_dict = DocumentScoreModel.from_dict(document_score_model_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


