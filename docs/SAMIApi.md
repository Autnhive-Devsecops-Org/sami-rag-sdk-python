# sami_rag_client.SAMIApi

All URIs are relative to */rag-defender*

Method | HTTP request | Description
------------- | ------------- | -------------
[**approve_quarantine_doc**](SAMIApi.md#approve_quarantine_doc) | **POST** /v1/quarantine/{doc_id}/approve | Quarantine
[**ingest_commit**](SAMIApi.md#ingest_commit) | **POST** /v1/ingest | Data Ingestion
[**reject_quarantine_doc**](SAMIApi.md#reject_quarantine_doc) | **POST** /v1/quarantine/{doc_id}/reject | Reject Quarantine


# **approve_quarantine_doc**
> QuarantineReviewResponse approve_quarantine_doc(doc_id, quarantine_review_request, authorization=authorization)

Quarantine

Approve quarantined doc and move it to accepted status;
pushes to indexer when enabled.

### Example


```python
import sami_rag_client
from sami_rag_client.models.quarantine_review_request import QuarantineReviewRequest
from sami_rag_client.models.quarantine_review_response import QuarantineReviewResponse
from sami_rag_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /rag-defender
# See configuration.py for a list of all supported configuration parameters.
configuration = sami_rag_client.Configuration(
    host = "https://dev-sami.autnhive.net/rag-defender"
)


# Enter a context with an instance of the API client
with sami_rag_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sami_rag_client.SAMIApi(api_client)
    doc_id = '81cc99cd-2e43-464a-bc0b-18b941a6d4bb' # str | Document ID
    quarantine_review_request = sami_rag_client.QuarantineReviewRequest(reason="no malicious", retriever_backend="weaviate") # QuarantineReviewRequest | 
    authorization = 'Bearer sk_llm-XXXXXXXX-XXXXXXXX-XXXXXXXX-XXXXXXXX' # str | dummy token, replace with your API key (optional)

    try:
        # Quarantine
        api_response = api_instance.approve_quarantine_doc(doc_id, quarantine_review_request, authorization=authorization)
        print("The response of SAMIApi->approve_quarantine_doc:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SAMIApi->approve_quarantine_doc: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **doc_id** | **str**| Document ID | 
 **quarantine_review_request** | [**QuarantineReviewRequest**](QuarantineReviewRequest.md)|  | 
 **authorization** | **str**|  | [optional] 

### Return type

[**QuarantineReviewResponse**](QuarantineReviewResponse.md)

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

# **ingest_commit**
> IngestCommitResponse ingest_commit(file_url_ingest_request, authorization=authorization)

Data Ingestion

### Example


```python
import sami_rag_client
from sami_rag_client.models.file_url_ingest_request import FileUrlIngestRequest
from sami_rag_client.models.ingest_commit_response import IngestCommitResponse
from sami_rag_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /rag-defender
# See configuration.py for a list of all supported configuration parameters.
configuration = sami_rag_client.Configuration(
    host = "https://dev-sami.autnhive.net/rag-defender"
)


# Enter a context with an instance of the API client
with sami_rag_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sami_rag_client.SAMIApi(api_client)
    file_url_ingest_request = sami_rag_client.FileUrlIngestRequest(tenant_id="tenant-001", app_id="app-001", doc_id="doc-001", file_url="https://example.com/sample.pdf", metadata={"source":"upload"}, store_quarantine=True, retriever_backend="weaviate") # FileUrlIngestRequest | 
    authorization = 'Bearer sk_llm-XXXXXXXX-XXXXXXXX-XXXXXXXX-XXXXXXXX' # str | dummy token, replace with your API key (optional)

    try:
        # Data Ingestion
        api_response = api_instance.ingest_commit(file_url_ingest_request, authorization=authorization)
        print("The response of SAMIApi->ingest_commit:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SAMIApi->ingest_commit: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file_url_ingest_request** | [**FileUrlIngestRequest**](FileUrlIngestRequest.md)|  | 
 **authorization** | **str**|  | [optional] 

### Return type

[**IngestCommitResponse**](IngestCommitResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **reject_quarantine_doc**
> QuarantineReviewResponse reject_quarantine_doc(doc_id, quarantine_review_request, authorization=authorization)

Reject Quarantine

Reject quarantined doc and mark it as rejected.

### Example


```python
import sami_rag_client
from sami_rag_client.models.quarantine_review_request import QuarantineReviewRequest
from sami_rag_client.models.quarantine_review_response import QuarantineReviewResponse
from sami_rag_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /rag-defender
# See configuration.py for a list of all supported configuration parameters.
configuration = sami_rag_client.Configuration(
    host = "https://dev-sami.autnhive.net/rag-defender"
)


# Enter a context with an instance of the API client
with sami_rag_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sami_rag_client.SAMIApi(api_client)
    doc_id = 'c9fb9598-ebf2-41e3-9df3-90df13340813' # str | Document ID
    quarantine_review_request = sami_rag_client.QuarantineReviewRequest() # QuarantineReviewRequest | 
    authorization = 'Bearer sk_llm-XXXXXXXX-XXXXXXXX-XXXXXXXX-XXXXXXXX' # str | dummy token, replace with your API key (optional)

    try:
        # Reject Quarantine
        api_response = api_instance.reject_quarantine_doc(doc_id, quarantine_review_request, authorization=authorization)
        print("The response of SAMIApi->reject_quarantine_doc:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SAMIApi->reject_quarantine_doc: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **doc_id** | **str**| Document ID | 
 **quarantine_review_request** | [**QuarantineReviewRequest**](QuarantineReviewRequest.md)|  | 
 **authorization** | **str**|  | [optional] 

### Return type

[**QuarantineReviewResponse**](QuarantineReviewResponse.md)

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

