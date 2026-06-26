# sami_rag_client.ORCHESTRATORApi

All URIs are relative to */rag-defender*

Method | HTTP request | Description
------------- | ------------- | -------------
[**rag_query**](ORCHESTRATORApi.md#rag_query) | **POST** /v1/rag/query | Rag Query


# **rag_query**
> RagQueryResponse rag_query(rag_query_request, authorization=authorization, x_request_id=x_request_id)

Rag Query

Main RAG endpoint.

Now delegates the core RAG work to the Orchestrator service:
  SAMI API -> Orchestrator /v1/rag/execute -> Retriever + RAGDefender + LLM

### Example


```python
import sami_rag_client
from sami_rag_client.models.rag_query_request import RagQueryRequest
from sami_rag_client.models.rag_query_response import RagQueryResponse
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
    api_instance = sami_rag_client.ORCHESTRATORApi(api_client)
    rag_query_request = sami_rag_client.RagQueryRequest() # RagQueryRequest | 
    authorization = 'authorization_example' # str |  (optional)
    x_request_id = 'x_request_id_example' # str |  (optional)

    try:
        # Rag Query
        api_response = api_instance.rag_query(rag_query_request, authorization=authorization, x_request_id=x_request_id)
        print("The response of ORCHESTRATORApi->rag_query:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ORCHESTRATORApi->rag_query: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **rag_query_request** | [**RagQueryRequest**](RagQueryRequest.md)|  | 
 **authorization** | **str**|  | [optional] 
 **x_request_id** | **str**|  | [optional] 

### Return type

[**RagQueryResponse**](RagQueryResponse.md)

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

