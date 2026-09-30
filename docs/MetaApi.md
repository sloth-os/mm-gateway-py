# mmgateway.MetaApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_health**](MetaApi.md#get_health) | **GET** /health | Health
[**get_metrics**](MetaApi.md#get_metrics) | **GET** /metrics | Metrics
[**list_model_limits**](MetaApi.md#list_model_limits) | **GET** /v1/models/limits | List Model Limits
[**list_models**](MetaApi.md#list_models) | **GET** /v1/models | List Models


# **get_health**
> HealthResponse get_health()

Health

### Example


```python
import mmgateway
from mmgateway.models.health_response import HealthResponse
from mmgateway.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = mmgateway.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with mmgateway.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mmgateway.MetaApi(api_client)

    try:
        # Health
        api_response = api_instance.get_health()
        print("The response of MetaApi->get_health:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MetaApi->get_health: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**HealthResponse**](HealthResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Gateway is healthy |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_metrics**
> str get_metrics()

Metrics

### Example


```python
import mmgateway
from mmgateway.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = mmgateway.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with mmgateway.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mmgateway.MetaApi(api_client)

    try:
        # Metrics
        api_response = api_instance.get_metrics()
        print("The response of MetaApi->get_metrics:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MetaApi->get_metrics: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

**str**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Prometheus exposition |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_model_limits**
> ModelLimitsListResponse list_model_limits(modality=modality, authorization=authorization, x_request_id=x_request_id, if_none_match=if_none_match)

List Model Limits

List usable models with their documented input/output limits.

Use this to pick a model and craft a prompt that fits: each entry's
``limits`` carries the input modalities accepted, the max prompt length,
the max output count, supported sizes/durations, and per-role support
flags (image-to-image, first/last frame, reference audio, lyrics, ...).
The same catalogue drives auto-routing when a request omits ``model``.

### Example

* Bearer (API key) Authentication (BearerAuth):

```python
import mmgateway
from mmgateway.models.model_limits_list_response import ModelLimitsListResponse
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
    api_instance = mmgateway.MetaApi(api_client)
    modality = 'modality_example' # str | Filter models by output modality. (optional)
    authorization = 'authorization_example' # str | Bearer token: \"Bearer <api-key>\". (optional)
    x_request_id = 'x_request_id_example' # str | Client-supplied request id (echoed back). (optional)
    if_none_match = 'if_none_match_example' # str | Previously returned ETag; unchanged resources return 304. (optional)

    try:
        # List Model Limits
        api_response = api_instance.list_model_limits(modality=modality, authorization=authorization, x_request_id=x_request_id, if_none_match=if_none_match)
        print("The response of MetaApi->list_model_limits:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MetaApi->list_model_limits: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **modality** | **str**| Filter models by output modality. | [optional] 
 **authorization** | **str**| Bearer token: \&quot;Bearer &lt;api-key&gt;\&quot;. | [optional] 
 **x_request_id** | **str**| Client-supplied request id (echoed back). | [optional] 
 **if_none_match** | **str**| Previously returned ETag; unchanged resources return 304. | [optional] 

### Return type

[**ModelLimitsListResponse**](ModelLimitsListResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Models available to the authenticated client with their input/output limits. |  * ETag - Version identifier for conditional polling. <br>  |
**304** | The model catalogue has not changed. |  -  |
**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
**401** | Missing or unknown API key |  -  |
**403** | Key not allowed to use any generation service |  -  |
**404** | Model or task not found. |  -  |
**422** | Validation Error |  -  |
**502** | Generation service returned an error. |  -  |
**503** | No usable generation service is configured. |  -  |
**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_models**
> ModelListResponse list_models(modality=modality, authorization=authorization, x_request_id=x_request_id, if_none_match=if_none_match)

List Models

### Example

* Bearer (API key) Authentication (BearerAuth):

```python
import mmgateway
from mmgateway.models.model_list_response import ModelListResponse
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
    api_instance = mmgateway.MetaApi(api_client)
    modality = 'modality_example' # str | Filter models by output modality. (optional)
    authorization = 'authorization_example' # str | Bearer token: \"Bearer <api-key>\". (optional)
    x_request_id = 'x_request_id_example' # str | Client-supplied request id (echoed back). (optional)
    if_none_match = 'if_none_match_example' # str | Previously returned ETag; unchanged resources return 304. (optional)

    try:
        # List Models
        api_response = api_instance.list_models(modality=modality, authorization=authorization, x_request_id=x_request_id, if_none_match=if_none_match)
        print("The response of MetaApi->list_models:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MetaApi->list_models: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **modality** | **str**| Filter models by output modality. | [optional] 
 **authorization** | **str**| Bearer token: \&quot;Bearer &lt;api-key&gt;\&quot;. | [optional] 
 **x_request_id** | **str**| Client-supplied request id (echoed back). | [optional] 
 **if_none_match** | **str**| Previously returned ETag; unchanged resources return 304. | [optional] 

### Return type

[**ModelListResponse**](ModelListResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Models available to the authenticated client. |  * ETag - Version identifier for conditional retrieval. <br>  |
**304** | The model catalogue has not changed. |  -  |
**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
**401** | Missing or unknown API key |  -  |
**403** | Key not allowed to use any generation service |  -  |
**404** | Model or task not found. |  -  |
**422** | Validation Error |  -  |
**502** | Generation service returned an error. |  -  |
**503** | No usable generation service is configured. |  -  |
**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

