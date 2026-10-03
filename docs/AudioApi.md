# mmgateway.AudioApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_audio**](AudioApi.md#create_audio) | **POST** /v1/audio | Create a speech task
[**create_voice**](AudioApi.md#create_voice) | **POST** /v1/voices | Clone a reusable voice
[**estimate_audio**](AudioApi.md#estimate_audio) | **POST** /v1/audio/estimate | Estimate a speech request
[**estimate_voice**](AudioApi.md#estimate_voice) | **POST** /v1/voices/estimate | Estimate voice cloning
[**get_audio**](AudioApi.md#get_audio) | **GET** /v1/audio/{audio_id} | Retrieve a speech task
[**get_voice**](AudioApi.md#get_voice) | **GET** /v1/voices/{voice_id} | Retrieve a voice or clone task
[**list_voices**](AudioApi.md#list_voices) | **GET** /v1/voices | List usable voice presets and owned clones


# **create_audio**
> AudioTaskResponse create_audio(audio_request, idempotency_key=idempotency_key)

Create a speech task

### Example

* Bearer (API key) Authentication (BearerAuth):

```python
import mmgateway
from mmgateway.models.audio_request import AudioRequest
from mmgateway.models.audio_task_response import AudioTaskResponse
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
    api_instance = mmgateway.AudioApi(api_client)
    audio_request = mmgateway.AudioRequest() # AudioRequest | 
    idempotency_key = 'idempotency_key_example' # str | Client-generated key used to safely retry this create request. Reuse with a different body returns 409. (optional)

    try:
        # Create a speech task
        api_response = api_instance.create_audio(audio_request, idempotency_key=idempotency_key)
        print("The response of AudioApi->create_audio:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AudioApi->create_audio: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **audio_request** | [**AudioRequest**](AudioRequest.md)|  | 
 **idempotency_key** | **str**| Client-generated key used to safely retry this create request. Reuse with a different body returns 409. | [optional] 

### Return type

[**AudioTaskResponse**](AudioTaskResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Speech synthesis accepted. |  * ETag - Version identifier for conditional retrieval. <br>  * Idempotency-Replayed - true when the response replays an earlier create request. <br>  * Link - Canonical task URL with rel&#x3D;\&quot;self\&quot;. <br>  * Location - Canonical URL of the created task resource. <br>  * Retry-After - Suggested number of seconds before polling again. <br>  |
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

# **create_voice**
> VoiceResponse create_voice(voice_clone_request, idempotency_key=idempotency_key)

Clone a reusable voice

### Example

* Bearer (API key) Authentication (BearerAuth):

```python
import mmgateway
from mmgateway.models.voice_clone_request import VoiceCloneRequest
from mmgateway.models.voice_response import VoiceResponse
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
    api_instance = mmgateway.AudioApi(api_client)
    voice_clone_request = mmgateway.VoiceCloneRequest() # VoiceCloneRequest | 
    idempotency_key = 'idempotency_key_example' # str | Client-generated key used to safely retry this create request. Reuse with a different body returns 409. (optional)

    try:
        # Clone a reusable voice
        api_response = api_instance.create_voice(voice_clone_request, idempotency_key=idempotency_key)
        print("The response of AudioApi->create_voice:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AudioApi->create_voice: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **voice_clone_request** | [**VoiceCloneRequest**](VoiceCloneRequest.md)|  | 
 **idempotency_key** | **str**| Client-generated key used to safely retry this create request. Reuse with a different body returns 409. | [optional] 

### Return type

[**VoiceResponse**](VoiceResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Voice cloning accepted. |  * ETag - Version identifier for conditional polling. <br>  * Idempotency-Replayed - true when the response replays an earlier create request. <br>  * Link - Canonical task URL with rel&#x3D;\&quot;self\&quot;. <br>  * Location - Canonical URL of the created task resource. <br>  * Retry-After - Suggested number of seconds before polling again. <br>  |
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

# **estimate_audio**
> EstimateResponse estimate_audio(audio_request)

Estimate a speech request

### Example

* Bearer (API key) Authentication (BearerAuth):

```python
import mmgateway
from mmgateway.models.audio_request import AudioRequest
from mmgateway.models.estimate_response import EstimateResponse
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
    api_instance = mmgateway.AudioApi(api_client)
    audio_request = mmgateway.AudioRequest() # AudioRequest | 

    try:
        # Estimate a speech request
        api_response = api_instance.estimate_audio(audio_request)
        print("The response of AudioApi->estimate_audio:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AudioApi->estimate_audio: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **audio_request** | [**AudioRequest**](AudioRequest.md)|  | 

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

# **estimate_voice**
> EstimateResponse estimate_voice(voice_clone_request)

Estimate voice cloning

### Example

* Bearer (API key) Authentication (BearerAuth):

```python
import mmgateway
from mmgateway.models.estimate_response import EstimateResponse
from mmgateway.models.voice_clone_request import VoiceCloneRequest
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
    api_instance = mmgateway.AudioApi(api_client)
    voice_clone_request = mmgateway.VoiceCloneRequest() # VoiceCloneRequest | 

    try:
        # Estimate voice cloning
        api_response = api_instance.estimate_voice(voice_clone_request)
        print("The response of AudioApi->estimate_voice:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AudioApi->estimate_voice: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **voice_clone_request** | [**VoiceCloneRequest**](VoiceCloneRequest.md)|  | 

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

# **get_audio**
> AudioTaskResponse get_audio(audio_id, if_none_match=if_none_match)

Retrieve a speech task

### Example

* Bearer (API key) Authentication (BearerAuth):

```python
import mmgateway
from mmgateway.models.audio_task_response import AudioTaskResponse
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
    api_instance = mmgateway.AudioApi(api_client)
    audio_id = 'audio_id_example' # str | Opaque speech task id.
    if_none_match = 'if_none_match_example' # str | Previously returned ETag; unchanged resources return 304. (optional)

    try:
        # Retrieve a speech task
        api_response = api_instance.get_audio(audio_id, if_none_match=if_none_match)
        print("The response of AudioApi->get_audio:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AudioApi->get_audio: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **audio_id** | **str**| Opaque speech task id. | 
 **if_none_match** | **str**| Previously returned ETag; unchanged resources return 304. | [optional] 

### Return type

[**AudioTaskResponse**](AudioTaskResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Current speech task state. |  * ETag - Version identifier for conditional polling. <br>  * Link - Canonical task URL with rel&#x3D;\&quot;self\&quot;. <br>  * Retry-After - Suggested number of seconds before polling again. <br>  |
**304** | Unchanged speech task. |  -  |
**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
**401** | Missing or unknown API key (unauthorized). |  -  |
**403** | Key not allowed to perform the request (forbidden). |  -  |
**404** | Model or task not found. |  -  |
**422** | Validation Error |  -  |
**502** | Generation service returned an error. |  -  |
**503** | No usable generation service is configured. |  -  |
**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_voice**
> VoiceResponse get_voice(voice_id, if_none_match=if_none_match)

Retrieve a voice or clone task

### Example

* Bearer (API key) Authentication (BearerAuth):

```python
import mmgateway
from mmgateway.models.voice_response import VoiceResponse
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
    api_instance = mmgateway.AudioApi(api_client)
    voice_id = 'voice_id_example' # str | Gateway voice id.
    if_none_match = 'if_none_match_example' # str | Previously returned ETag; unchanged resources return 304. (optional)

    try:
        # Retrieve a voice or clone task
        api_response = api_instance.get_voice(voice_id, if_none_match=if_none_match)
        print("The response of AudioApi->get_voice:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AudioApi->get_voice: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **voice_id** | **str**| Gateway voice id. | 
 **if_none_match** | **str**| Previously returned ETag; unchanged resources return 304. | [optional] 

### Return type

[**VoiceResponse**](VoiceResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Current voice state. |  * ETag - Version identifier for conditional polling. <br>  * Link - Canonical task URL with rel&#x3D;\&quot;self\&quot;. <br>  * Retry-After - Suggested number of seconds before polling again. <br>  |
**304** | Unchanged voice. |  -  |
**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
**401** | Missing or unknown API key (unauthorized). |  -  |
**403** | Key not allowed to perform the request (forbidden). |  -  |
**404** | Model or task not found. |  -  |
**422** | Validation Error |  -  |
**502** | Generation service returned an error. |  -  |
**503** | No usable generation service is configured. |  -  |
**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_voices**
> VoiceListResponse list_voices(if_none_match=if_none_match)

List usable voice presets and owned clones

### Example

* Bearer (API key) Authentication (BearerAuth):

```python
import mmgateway
from mmgateway.models.voice_list_response import VoiceListResponse
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
    api_instance = mmgateway.AudioApi(api_client)
    if_none_match = 'if_none_match_example' # str | Previously returned ETag; unchanged resources return 304. (optional)

    try:
        # List usable voice presets and owned clones
        api_response = api_instance.list_voices(if_none_match=if_none_match)
        print("The response of AudioApi->list_voices:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AudioApi->list_voices: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **if_none_match** | **str**| Previously returned ETag; unchanged resources return 304. | [optional] 

### Return type

[**VoiceListResponse**](VoiceListResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Voices available to this key. |  * ETag - Version identifier for conditional polling. <br>  |
**304** | Unchanged voice list. |  -  |
**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
**401** | Missing or unknown API key (unauthorized). |  -  |
**403** | Key not allowed to perform the request (forbidden). |  -  |
**404** | Model or task not found. |  -  |
**422** | Validation Error |  -  |
**502** | Generation service returned an error. |  -  |
**503** | No usable generation service is configured. |  -  |
**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

