# sami_rag_client.DEFENDERApi

All URIs are relative to */rag-defender*

Method | HTTP request | Description
------------- | ------------- | -------------
[**defend_v1_defend_post**](DEFENDERApi.md#defend_v1_defend_post) | **POST** /v1/defend | Defend


# **defend_v1_defend_post**
> DefendResponseModel defend_v1_defend_post(defend_request_model, x_request_id=x_request_id, x_tenant_id=x_tenant_id)

Defend

### Example


```python
import sami_rag_client
from sami_rag_client.models.defend_request_model import DefendRequestModel
from sami_rag_client.models.defend_response_model import DefendResponseModel
from sami_rag_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /rag-defender
# See configuration.py for a list of all supported configuration parameters.
configuration = sami_rag_client.Configuration(
    host = "/rag-defender"
)


# Enter a context with an instance of the API client
with sami_rag_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sami_rag_client.DEFENDERApi(api_client)
    defend_request_model = sami_rag_client.DefendRequestModel() # DefendRequestModel | 
    x_request_id = 'x_request_id_example' # str |  (optional)
    x_tenant_id = 'x_tenant_id_example' # str |  (optional)

    try:
        # Defend
        api_response = api_instance.defend_v1_defend_post(defend_request_model, x_request_id=x_request_id, x_tenant_id=x_tenant_id)
        print("The response of DEFENDERApi->defend_v1_defend_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DEFENDERApi->defend_v1_defend_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **defend_request_model** | [**DefendRequestModel**](DefendRequestModel.md)|  | 
 **x_request_id** | **str**|  | [optional] 
 **x_tenant_id** | **str**|  | [optional] 

### Return type

[**DefendResponseModel**](DefendResponseModel.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

