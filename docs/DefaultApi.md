# sami_rag_client.DefaultApi

All URIs are relative to */rag-defender*

Method | HTTP request | Description
------------- | ------------- | -------------
[**file_sanitization**](DefaultApi.md#file_sanitization) | **POST** /ai-firewall/firewall/v1/file/sanitization | Replace content in uploaded files
[**multimodal_chat**](DefaultApi.md#multimodal_chat) | **POST** /ai-firewall/firewall/v1/prompt | Multimodal chat completions


# **file_sanitization**
> List[str] file_sanitization(signed_url_payload)

Replace content in uploaded files

### Example

* Bearer Authentication (HTTPBearer):

```python
import sami_firewall_client
from sami_firewall_client.models.signed_url_payload import SignedUrlPayload
from sami_firewall_client.models.job import Job
from sami_firewall_client.rest import ApiException
from pprint import pprint

# Configuration: host + bearer token (single source of truth)
HOST = "https://dev-sami.autnhive.net"
BEARER_TOKEN = "sk_llm-XXXXXXXX-XXXXXXXX-XXXXXXXX-XXXXXXXX"  # dummy token, replace with your API key

configuration = sami_firewall_client.Configuration(host=HOST)
# Keep the token on the Configuration object as the single source of truth.
configuration.access_token = BEARER_TOKEN

# Build an ApiClient that applies the Authorization header on every request.
api_client = sami_firewall_client.ApiClient(
    configuration,
    header_name="Authorization",
    header_value=f"Bearer {configuration.access_token}",
)

# Enter a context with an instance of the API client
with api_client:
    # Create an instance of the API class
    api_instance = sami_firewall_client.DefaultApi(api_client)
    signed_url_payload = SignedUrlPayload(
        jobs=[
            Job(
                id="89f0b583-3833-4ce0-9c15-93a1dd3a0f5d",
                signed_url="https://example-object-storage/path/to/Test_Profile_by_QA.docx",
                file_name="Test_Profile_by_QA.docx",
                file_size=16357,
                policy_packs=["default"],
                enhanced_privacy_mode=False,
            )
        ]
    ) # SignedUrlPayload | 

    try:
        # Replace content in uploaded files
        api_response = api_instance.file_sanitization(signed_url_payload)
        print("The response of DefaultApi->file_sanitization:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->file_sanitization: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **signed_url_payload** | [**SignedUrlPayload**](SignedUrlPayload.md)|  | 

### Return type

**List[str]**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | file replacement results |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **multimodal_chat**
> Dict[str, object] multimodal_chat(prompt=prompt, content=content, text=text, input=input, file=file, docx=docx, pdf=pdf, image=image, audio=audio, model=model)

Multimodal chat completions

### Example

* Bearer Authentication (HTTPBearer):

```python
import sami_rag_client
from sami_rag_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /rag-defender
# See configuration.py for a list of all supported configuration parameters.
configuration = sami_rag_client.Configuration(
    host = "/rag-defender"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: HTTPBearer
configuration = sami_rag_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with sami_rag_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sami_rag_client.DefaultApi(api_client)
    prompt = 'prompt_example' # str | Free-form prompt text (optional)
    content = 'content_example' # str | Optional content payload (optional)
    text = 'text_example' # str | Optional text input (optional)
    input = 'input_example' # str | Optional input input (optional)
    file = 'file_example' # str | Generic file upload (optional) (optional)
    docx = 'docx_example' # str | DOCX upload (optional) (optional)
    pdf = 'pdf_example' # str | PDF upload (optional) (optional)
    image = 'image_example' # str | Image upload (optional) (optional)
    audio = 'audio_example' # str | Audio upload (optional) (optional)
    model = 'model_example' # str | Optional model name (optional)

    try:
        # Multimodal chat completions
        api_response = api_instance.multimodal_chat(prompt=prompt, content=content, text=text, input=input, file=file, docx=docx, pdf=pdf, image=image, audio=audio, model=model)
        print("The response of DefaultApi->multimodal_chat:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->multimodal_chat: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **prompt** | **str**| Free-form prompt text | [optional] 
 **content** | **str**| Optional content payload | [optional] 
 **text** | **str**| Optional text input | [optional] 
 **input** | **str**| Optional input input | [optional] 
 **file** | **str**| Generic file upload (optional) | [optional] 
 **docx** | **str**| DOCX upload (optional) | [optional] 
 **pdf** | **str**| PDF upload (optional) | [optional] 
 **image** | **str**| Image upload (optional) | [optional] 
 **audio** | **str**| Audio upload (optional) | [optional] 
 **model** | **str**| Optional model name | [optional] 

### Return type

**Dict[str, object]**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | AI firewall chat completion response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

