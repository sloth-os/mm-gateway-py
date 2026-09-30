# mmgateway.ImagesApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_image**](ImagesApi.md#create_image) | **POST** /v1/images | Create an image task
[**get_image**](ImagesApi.md#get_image) | **GET** /v1/images/{image_id} | Retrieve an image task


# **create_image**
> ImageTaskResponse create_image(image_request, idempotency_key=idempotency_key)

Create an image task

### Example

* Bearer (API key) Authentication (BearerAuth):

```python
import mmgateway
from mmgateway.models.image_request import ImageRequest
from mmgateway.models.image_task_response import ImageTaskResponse
from mmgateway.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = mmgateway.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (API key): BearerAuth
configuration = mmgateway.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mmgateway.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mmgateway.ImagesApi(api_client)
    image_request = mmgateway.ImageRequest() # ImageRequest | 
    idempotency_key = 'idempotency_key_example' # str | Client-generated key used to safely retry this create request. Reuse with a different body returns 409. (optional)

    try:
        # Create an image task
        api_response = api_instance.create_image(image_request, idempotency_key=idempotency_key)
        print("The response of ImagesApi->create_image:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ImagesApi->create_image: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **image_request** | [**ImageRequest**](ImageRequest.md)|  | 
 **idempotency_key** | **str**| Client-generated key used to safely retry this create request. Reuse with a different body returns 409. | [optional] 

### Return type

[**ImageTaskResponse**](ImageTaskResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | The image task was accepted. |  * ETag - Version identifier for conditional retrieval. <br>  * Idempotency-Replayed - true when the response replays an earlier create request. <br>  * Link - Canonical task URL with rel&#x3D;\&quot;self\&quot;. <br>  * Location - Canonical URL of the created task resource. <br>  * Retry-After - Suggested number of seconds before polling again. <br>  |
**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
**401** | Missing or unknown API key (unauthorized). |  -  |
**403** | Key not allowed to perform the request (forbidden). |  -  |
**404** | Model or task not found. |  -  |
**409** | Idempotency key conflicts with an earlier request. |  -  |
**422** | Validation Error |  -  |
**502** | Generation service returned an error. |  -  |
**503** | No usable generation service is configured. |  -  |
**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_image**
> ImageTaskResponse get_image(image_id, if_none_match=if_none_match)

Retrieve an image task

### Example

* Bearer (API key) Authentication (BearerAuth):

```python
import mmgateway
from mmgateway.models.image_task_response import ImageTaskResponse
from mmgateway.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = mmgateway.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (API key): BearerAuth
configuration = mmgateway.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mmgateway.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mmgateway.ImagesApi(api_client)
    image_id = 'image_id_example' # str | Opaque image task id.
    if_none_match = 'if_none_match_example' # str | Previously returned ETag; unchanged resources return 304. (optional)

    try:
        # Retrieve an image task
        api_response = api_instance.get_image(image_id, if_none_match=if_none_match)
        print("The response of ImagesApi->get_image:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ImagesApi->get_image: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **image_id** | **str**| Opaque image task id. | 
 **if_none_match** | **str**| Previously returned ETag; unchanged resources return 304. | [optional] 

### Return type

[**ImageTaskResponse**](ImageTaskResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The latest image task state. |  * ETag - Version identifier for conditional polling. <br>  * Link - Canonical task URL with rel&#x3D;\&quot;self\&quot;. <br>  * Retry-After - Suggested number of seconds before polling again. <br>  |
**304** | The task representation has not changed. |  -  |
**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
**401** | Missing or unknown API key (unauthorized). |  -  |
**403** | Key not allowed to perform the request (forbidden). |  -  |
**404** | Unknown image task id. |  -  |
**422** | Validation Error |  -  |
**502** | Generation service returned an error. |  -  |
**503** | No usable generation service is configured. |  -  |
**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

