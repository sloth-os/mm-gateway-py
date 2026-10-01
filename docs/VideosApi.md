# mmgateway.VideosApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_video**](VideosApi.md#create_video) | **POST** /v1/videos | Create a video task
[**estimate_video**](VideosApi.md#estimate_video) | **POST** /v1/videos/estimate | Estimate a video request
[**get_video**](VideosApi.md#get_video) | **GET** /v1/videos/{video_id} | Retrieve a video task


# **create_video**
> VideoTaskResponse create_video(video_request, idempotency_key=idempotency_key)

Create a video task

### Example

* Bearer (API key) Authentication (BearerAuth):

```python
import mmgateway
from mmgateway.models.video_request import VideoRequest
from mmgateway.models.video_task_response import VideoTaskResponse
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
    api_instance = mmgateway.VideosApi(api_client)
    video_request = mmgateway.VideoRequest() # VideoRequest | 
    idempotency_key = 'idempotency_key_example' # str | Client-generated key used to safely retry this create request. Reuse with a different body returns 409. (optional)

    try:
        # Create a video task
        api_response = api_instance.create_video(video_request, idempotency_key=idempotency_key)
        print("The response of VideosApi->create_video:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling VideosApi->create_video: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **video_request** | [**VideoRequest**](VideoRequest.md)|  | 
 **idempotency_key** | **str**| Client-generated key used to safely retry this create request. Reuse with a different body returns 409. | [optional] 

### Return type

[**VideoTaskResponse**](VideoTaskResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | The video task was accepted. |  * ETag - Version identifier for conditional polling. <br>  * Idempotency-Replayed - true when the response replays an earlier create request. <br>  * Link - Canonical task URL with rel&#x3D;\&quot;self\&quot;. <br>  * Location - Canonical URL of the created task resource. <br>  * Retry-After - Suggested number of seconds before polling again. <br>  |
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

# **estimate_video**
> EstimateResponse estimate_video(video_request)

Estimate a video request

### Example

* Bearer (API key) Authentication (BearerAuth):

```python
import mmgateway
from mmgateway.models.estimate_response import EstimateResponse
from mmgateway.models.video_request import VideoRequest
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
    api_instance = mmgateway.VideosApi(api_client)
    video_request = mmgateway.VideoRequest() # VideoRequest | 

    try:
        # Estimate a video request
        api_response = api_instance.estimate_video(video_request)
        print("The response of VideosApi->estimate_video:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling VideosApi->estimate_video: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **video_request** | [**VideoRequest**](VideoRequest.md)|  | 

### Return type

[**EstimateResponse**](EstimateResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | How auto mode would route the request, and its estimated cost. |  -  |
**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
**401** | Missing or unknown API key (unauthorized). |  -  |
**403** | Key not allowed to perform the request (forbidden). |  -  |
**404** | Model or task not found. |  -  |
**422** | Validation Error |  -  |
**502** | Generation service returned an error. |  -  |
**503** | No usable generation service is configured. |  -  |
**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_video**
> VideoTaskResponse get_video(video_id, if_none_match=if_none_match)

Retrieve a video task

### Example

* Bearer (API key) Authentication (BearerAuth):

```python
import mmgateway
from mmgateway.models.video_task_response import VideoTaskResponse
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
    api_instance = mmgateway.VideosApi(api_client)
    video_id = 'video_id_example' # str | Opaque video task id.
    if_none_match = 'if_none_match_example' # str | Previously returned ETag; unchanged resources return 304. (optional)

    try:
        # Retrieve a video task
        api_response = api_instance.get_video(video_id, if_none_match=if_none_match)
        print("The response of VideosApi->get_video:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling VideosApi->get_video: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **video_id** | **str**| Opaque video task id. | 
 **if_none_match** | **str**| Previously returned ETag; unchanged resources return 304. | [optional] 

### Return type

[**VideoTaskResponse**](VideoTaskResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The latest video task state. |  * ETag - Version identifier for conditional polling. <br>  * Link - Canonical task URL with rel&#x3D;\&quot;self\&quot;. <br>  * Retry-After - Suggested number of seconds before polling again. <br>  |
**304** | The task representation has not changed. |  -  |
**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
**401** | Missing or unknown API key (unauthorized). |  -  |
**403** | Key not allowed to perform the request (forbidden). |  -  |
**404** | Unknown video task id. |  -  |
**422** | Validation Error |  -  |
**502** | Generation service returned an error. |  -  |
**503** | No usable generation service is configured. |  -  |
**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

