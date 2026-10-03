# mmgateway.ManagementApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_management_backend**](ManagementApi.md#delete_management_backend) | **DELETE** /v1/management/backends/{name} | Delete Backend
[**delete_management_key**](ManagementApi.md#delete_management_key) | **DELETE** /v1/management/keys/{key_id} | Delete Key
[**delete_management_proxy**](ManagementApi.md#delete_management_proxy) | **DELETE** /v1/management/proxies/{domain} | Delete Proxy
[**get_management_config**](ManagementApi.md#get_management_config) | **GET** /v1/management/config | Get Config
[**get_management_metrics**](ManagementApi.md#get_management_metrics) | **GET** /v1/management/metrics | Get Metrics
[**get_management_status**](ManagementApi.md#get_management_status) | **GET** /v1/management/status | Get Status
[**list_management_tasks**](ManagementApi.md#list_management_tasks) | **GET** /v1/management/tasks | List Tasks
[**list_management_usage**](ManagementApi.md#list_management_usage) | **GET** /v1/management/usage | List Usage
[**put_management_backend**](ManagementApi.md#put_management_backend) | **PUT** /v1/management/backends/{name} | Put Backend
[**put_management_key**](ManagementApi.md#put_management_key) | **PUT** /v1/management/keys/{key_id} | Put Key
[**put_management_proxy**](ManagementApi.md#put_management_proxy) | **PUT** /v1/management/proxies/{domain} | Put Proxy
[**replace_management_config**](ManagementApi.md#replace_management_config) | **PUT** /v1/management/config | Replace Config


# **delete_management_backend**
> ManagementConfigResponse delete_management_backend(name, if_match=if_match)

Delete Backend

### Example

* Bearer (Management API key) Authentication (ManagementAuth):

```python
import mmgateway
from mmgateway.models.management_config_response import ManagementConfigResponse
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

# Configure Bearer authorization (Management API key): ManagementAuth
configuration = mmgateway.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mmgateway.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mmgateway.ManagementApi(api_client)
    name = 'name_example' # str | 
    if_match = 'if_match_example' # str | Current configuration revision (ETag). (optional)

    try:
        # Delete Backend
        api_response = api_instance.delete_management_backend(name, if_match=if_match)
        print("The response of ManagementApi->delete_management_backend:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ManagementApi->delete_management_backend: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **str**|  | 
 **if_match** | **str**| Current configuration revision (ETag). | [optional] 

### Return type

[**ManagementConfigResponse**](ManagementConfigResponse.md)

### Authorization

[ManagementAuth](../README.md#ManagementAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**401** | Missing or unknown API key (unauthorized). |  -  |
**404** | Model or task not found. |  -  |
**412** | Configuration changed; reload before saving. |  -  |
**422** | Validation Error |  -  |
**428** | A current If-Match revision is required. |  -  |
**503** | No usable generation service is configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_management_key**
> ManagementConfigResponse delete_management_key(key_id, if_match=if_match)

Delete Key

### Example

* Bearer (Management API key) Authentication (ManagementAuth):

```python
import mmgateway
from mmgateway.models.management_config_response import ManagementConfigResponse
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

# Configure Bearer authorization (Management API key): ManagementAuth
configuration = mmgateway.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mmgateway.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mmgateway.ManagementApi(api_client)
    key_id = 'key_id_example' # str | 
    if_match = 'if_match_example' # str | Current configuration revision (ETag). (optional)

    try:
        # Delete Key
        api_response = api_instance.delete_management_key(key_id, if_match=if_match)
        print("The response of ManagementApi->delete_management_key:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ManagementApi->delete_management_key: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **key_id** | **str**|  | 
 **if_match** | **str**| Current configuration revision (ETag). | [optional] 

### Return type

[**ManagementConfigResponse**](ManagementConfigResponse.md)

### Authorization

[ManagementAuth](../README.md#ManagementAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**401** | Missing or unknown API key (unauthorized). |  -  |
**404** | Model or task not found. |  -  |
**412** | Configuration changed; reload before saving. |  -  |
**422** | Validation Error |  -  |
**428** | A current If-Match revision is required. |  -  |
**503** | No usable generation service is configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_management_proxy**
> ManagementConfigResponse delete_management_proxy(domain, if_match=if_match)

Delete Proxy

### Example

* Bearer (Management API key) Authentication (ManagementAuth):

```python
import mmgateway
from mmgateway.models.management_config_response import ManagementConfigResponse
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

# Configure Bearer authorization (Management API key): ManagementAuth
configuration = mmgateway.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mmgateway.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mmgateway.ManagementApi(api_client)
    domain = 'domain_example' # str | 
    if_match = 'if_match_example' # str | Current configuration revision (ETag). (optional)

    try:
        # Delete Proxy
        api_response = api_instance.delete_management_proxy(domain, if_match=if_match)
        print("The response of ManagementApi->delete_management_proxy:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ManagementApi->delete_management_proxy: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain** | **str**|  | 
 **if_match** | **str**| Current configuration revision (ETag). | [optional] 

### Return type

[**ManagementConfigResponse**](ManagementConfigResponse.md)

### Authorization

[ManagementAuth](../README.md#ManagementAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**401** | Missing or unknown API key (unauthorized). |  -  |
**404** | Model or task not found. |  -  |
**412** | Configuration changed; reload before saving. |  -  |
**422** | Validation Error |  -  |
**428** | A current If-Match revision is required. |  -  |
**503** | No usable generation service is configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_management_config**
> ManagementConfigResponse get_management_config()

Get Config

### Example

* Bearer (Management API key) Authentication (ManagementAuth):

```python
import mmgateway
from mmgateway.models.management_config_response import ManagementConfigResponse
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

# Configure Bearer authorization (Management API key): ManagementAuth
configuration = mmgateway.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mmgateway.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mmgateway.ManagementApi(api_client)

    try:
        # Get Config
        api_response = api_instance.get_management_config()
        print("The response of ManagementApi->get_management_config:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ManagementApi->get_management_config: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**ManagementConfigResponse**](ManagementConfigResponse.md)

### Authorization

[ManagementAuth](../README.md#ManagementAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**401** | Missing or unknown API key (unauthorized). |  -  |
**404** | Model or task not found. |  -  |
**422** | Request validation failed or a task failed. |  -  |
**503** | No usable generation service is configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_management_metrics**
> ManagementMetrics get_management_metrics()

Get Metrics

### Example

* Bearer (Management API key) Authentication (ManagementAuth):

```python
import mmgateway
from mmgateway.models.management_metrics import ManagementMetrics
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

# Configure Bearer authorization (Management API key): ManagementAuth
configuration = mmgateway.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mmgateway.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mmgateway.ManagementApi(api_client)

    try:
        # Get Metrics
        api_response = api_instance.get_management_metrics()
        print("The response of ManagementApi->get_management_metrics:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ManagementApi->get_management_metrics: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**ManagementMetrics**](ManagementMetrics.md)

### Authorization

[ManagementAuth](../README.md#ManagementAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**401** | Missing or unknown API key (unauthorized). |  -  |
**404** | Model or task not found. |  -  |
**422** | Request validation failed or a task failed. |  -  |
**503** | No usable generation service is configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_management_status**
> ManagementStatus get_management_status()

Get Status

### Example

* Bearer (Management API key) Authentication (ManagementAuth):

```python
import mmgateway
from mmgateway.models.management_status import ManagementStatus
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

# Configure Bearer authorization (Management API key): ManagementAuth
configuration = mmgateway.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mmgateway.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mmgateway.ManagementApi(api_client)

    try:
        # Get Status
        api_response = api_instance.get_management_status()
        print("The response of ManagementApi->get_management_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ManagementApi->get_management_status: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**ManagementStatus**](ManagementStatus.md)

### Authorization

[ManagementAuth](../README.md#ManagementAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**401** | Missing or unknown API key (unauthorized). |  -  |
**404** | Model or task not found. |  -  |
**422** | Request validation failed or a task failed. |  -  |
**503** | No usable generation service is configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_management_tasks**
> ManagementTaskList list_management_tasks(modality=modality, status=status, key_id=key_id, backend=backend, offset=offset, limit=limit)

List Tasks

### Example

* Bearer (Management API key) Authentication (ManagementAuth):

```python
import mmgateway
from mmgateway.models.management_task_list import ManagementTaskList
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

# Configure Bearer authorization (Management API key): ManagementAuth
configuration = mmgateway.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mmgateway.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mmgateway.ManagementApi(api_client)
    modality = 'modality_example' # str |  (optional)
    status = 'status_example' # str |  (optional)
    key_id = 'key_id_example' # str |  (optional)
    backend = 'backend_example' # str |  (optional)
    offset = 0 # int |  (optional) (default to 0)
    limit = 50 # int |  (optional) (default to 50)

    try:
        # List Tasks
        api_response = api_instance.list_management_tasks(modality=modality, status=status, key_id=key_id, backend=backend, offset=offset, limit=limit)
        print("The response of ManagementApi->list_management_tasks:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ManagementApi->list_management_tasks: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **modality** | **str**|  | [optional] 
 **status** | **str**|  | [optional] 
 **key_id** | **str**|  | [optional] 
 **backend** | **str**|  | [optional] 
 **offset** | **int**|  | [optional] [default to 0]
 **limit** | **int**|  | [optional] [default to 50]

### Return type

[**ManagementTaskList**](ManagementTaskList.md)

### Authorization

[ManagementAuth](../README.md#ManagementAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**401** | Missing or unknown API key (unauthorized). |  -  |
**404** | Model or task not found. |  -  |
**422** | Validation Error |  -  |
**503** | No usable generation service is configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_management_usage**
> ManagementUsageList list_management_usage(key_id=key_id)

List Usage

### Example

* Bearer (Management API key) Authentication (ManagementAuth):

```python
import mmgateway
from mmgateway.models.management_usage_list import ManagementUsageList
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

# Configure Bearer authorization (Management API key): ManagementAuth
configuration = mmgateway.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mmgateway.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mmgateway.ManagementApi(api_client)
    key_id = 'key_id_example' # str |  (optional)

    try:
        # List Usage
        api_response = api_instance.list_management_usage(key_id=key_id)
        print("The response of ManagementApi->list_management_usage:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ManagementApi->list_management_usage: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **key_id** | **str**|  | [optional] 

### Return type

[**ManagementUsageList**](ManagementUsageList.md)

### Authorization

[ManagementAuth](../README.md#ManagementAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**401** | Missing or unknown API key (unauthorized). |  -  |
**404** | Model or task not found. |  -  |
**422** | Validation Error |  -  |
**503** | No usable generation service is configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **put_management_backend**
> ManagementConfigResponse put_management_backend(name, managed_backend, if_match=if_match)

Put Backend

### Example

* Bearer (Management API key) Authentication (ManagementAuth):

```python
import mmgateway
from mmgateway.models.managed_backend import ManagedBackend
from mmgateway.models.management_config_response import ManagementConfigResponse
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

# Configure Bearer authorization (Management API key): ManagementAuth
configuration = mmgateway.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mmgateway.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mmgateway.ManagementApi(api_client)
    name = 'name_example' # str | 
    managed_backend = mmgateway.ManagedBackend() # ManagedBackend | 
    if_match = 'if_match_example' # str | Current configuration revision (ETag). (optional)

    try:
        # Put Backend
        api_response = api_instance.put_management_backend(name, managed_backend, if_match=if_match)
        print("The response of ManagementApi->put_management_backend:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ManagementApi->put_management_backend: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **str**|  | 
 **managed_backend** | [**ManagedBackend**](ManagedBackend.md)|  | 
 **if_match** | **str**| Current configuration revision (ETag). | [optional] 

### Return type

[**ManagementConfigResponse**](ManagementConfigResponse.md)

### Authorization

[ManagementAuth](../README.md#ManagementAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**401** | Missing or unknown API key (unauthorized). |  -  |
**404** | Model or task not found. |  -  |
**412** | Configuration changed; reload before saving. |  -  |
**422** | Validation Error |  -  |
**428** | A current If-Match revision is required. |  -  |
**503** | No usable generation service is configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **put_management_key**
> ManagementConfigResponse put_management_key(key_id, managed_key, if_match=if_match)

Put Key

### Example

* Bearer (Management API key) Authentication (ManagementAuth):

```python
import mmgateway
from mmgateway.models.managed_key import ManagedKey
from mmgateway.models.management_config_response import ManagementConfigResponse
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

# Configure Bearer authorization (Management API key): ManagementAuth
configuration = mmgateway.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mmgateway.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mmgateway.ManagementApi(api_client)
    key_id = 'key_id_example' # str | 
    managed_key = mmgateway.ManagedKey() # ManagedKey | 
    if_match = 'if_match_example' # str | Current configuration revision (ETag). (optional)

    try:
        # Put Key
        api_response = api_instance.put_management_key(key_id, managed_key, if_match=if_match)
        print("The response of ManagementApi->put_management_key:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ManagementApi->put_management_key: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **key_id** | **str**|  | 
 **managed_key** | [**ManagedKey**](ManagedKey.md)|  | 
 **if_match** | **str**| Current configuration revision (ETag). | [optional] 

### Return type

[**ManagementConfigResponse**](ManagementConfigResponse.md)

### Authorization

[ManagementAuth](../README.md#ManagementAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**401** | Missing or unknown API key (unauthorized). |  -  |
**404** | Model or task not found. |  -  |
**412** | Configuration changed; reload before saving. |  -  |
**422** | Validation Error |  -  |
**428** | A current If-Match revision is required. |  -  |
**503** | No usable generation service is configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **put_management_proxy**
> ManagementConfigResponse put_management_proxy(domain, managed_proxy, if_match=if_match)

Put Proxy

### Example

* Bearer (Management API key) Authentication (ManagementAuth):

```python
import mmgateway
from mmgateway.models.managed_proxy import ManagedProxy
from mmgateway.models.management_config_response import ManagementConfigResponse
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

# Configure Bearer authorization (Management API key): ManagementAuth
configuration = mmgateway.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mmgateway.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mmgateway.ManagementApi(api_client)
    domain = 'domain_example' # str | 
    managed_proxy = mmgateway.ManagedProxy() # ManagedProxy | 
    if_match = 'if_match_example' # str | Current configuration revision (ETag). (optional)

    try:
        # Put Proxy
        api_response = api_instance.put_management_proxy(domain, managed_proxy, if_match=if_match)
        print("The response of ManagementApi->put_management_proxy:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ManagementApi->put_management_proxy: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain** | **str**|  | 
 **managed_proxy** | [**ManagedProxy**](ManagedProxy.md)|  | 
 **if_match** | **str**| Current configuration revision (ETag). | [optional] 

### Return type

[**ManagementConfigResponse**](ManagementConfigResponse.md)

### Authorization

[ManagementAuth](../README.md#ManagementAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**401** | Missing or unknown API key (unauthorized). |  -  |
**404** | Model or task not found. |  -  |
**412** | Configuration changed; reload before saving. |  -  |
**422** | Validation Error |  -  |
**428** | A current If-Match revision is required. |  -  |
**503** | No usable generation service is configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **replace_management_config**
> ManagementConfigResponse replace_management_config(management_config_input, if_match=if_match)

Replace Config

### Example

* Bearer (Management API key) Authentication (ManagementAuth):

```python
import mmgateway
from mmgateway.models.management_config_input import ManagementConfigInput
from mmgateway.models.management_config_response import ManagementConfigResponse
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

# Configure Bearer authorization (Management API key): ManagementAuth
configuration = mmgateway.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mmgateway.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mmgateway.ManagementApi(api_client)
    management_config_input = mmgateway.ManagementConfigInput() # ManagementConfigInput | 
    if_match = 'if_match_example' # str | Current configuration revision (ETag). (optional)

    try:
        # Replace Config
        api_response = api_instance.replace_management_config(management_config_input, if_match=if_match)
        print("The response of ManagementApi->replace_management_config:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ManagementApi->replace_management_config: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **management_config_input** | [**ManagementConfigInput**](ManagementConfigInput.md)|  | 
 **if_match** | **str**| Current configuration revision (ETag). | [optional] 

### Return type

[**ManagementConfigResponse**](ManagementConfigResponse.md)

### Authorization

[ManagementAuth](../README.md#ManagementAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**401** | Missing or unknown API key (unauthorized). |  -  |
**404** | Model or task not found. |  -  |
**412** | Configuration changed; reload before saving. |  -  |
**422** | Validation Error |  -  |
**428** | A current If-Match revision is required. |  -  |
**503** | No usable generation service is configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

