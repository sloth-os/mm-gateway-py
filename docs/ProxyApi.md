# mmgateway.ProxyApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**proxy_request_delete**](ProxyApi.md#proxy_request_delete) | **DELETE** /proxy/{domain}/{path} | Forward a request through a domain-matched proxy
[**proxy_request_get**](ProxyApi.md#proxy_request_get) | **GET** /proxy/{domain}/{path} | Forward a request through a domain-matched proxy
[**proxy_request_head**](ProxyApi.md#proxy_request_head) | **HEAD** /proxy/{domain}/{path} | Forward a request through a domain-matched proxy
[**proxy_request_options**](ProxyApi.md#proxy_request_options) | **OPTIONS** /proxy/{domain}/{path} | Forward a request through a domain-matched proxy
[**proxy_request_patch**](ProxyApi.md#proxy_request_patch) | **PATCH** /proxy/{domain}/{path} | Forward a request through a domain-matched proxy
[**proxy_request_post**](ProxyApi.md#proxy_request_post) | **POST** /proxy/{domain}/{path} | Forward a request through a domain-matched proxy
[**proxy_request_put**](ProxyApi.md#proxy_request_put) | **PUT** /proxy/{domain}/{path} | Forward a request through a domain-matched proxy


# **proxy_request_delete**
> proxy_request_delete(domain, path)

Forward a request through a domain-matched proxy

Forward an HTTP request through a domain-matched proxy to its upstream.

The path, query string, body, and most client headers are forwarded
verbatim to ``{base_url}/{path}``; the configured account's credential is
injected from the account's ``headers`` and the upstream response (including
event streams) is streamed back. Retries across accounts on a rate-limit /
timeout / 5xx.

### Example

* Bearer (API key) Authentication (BearerAuth):

```python
import mmgateway
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
    api_instance = mmgateway.ProxyApi(api_client)
    domain = 'domain_example' # str | Configured proxy domain (the upstream host segment selecting the proxy).
    path = 'path_example' # str | Path forwarded to the upstream root URL.

    try:
        # Forward a request through a domain-matched proxy
        api_instance.proxy_request_delete(domain, path)
    except Exception as e:
        print("Exception when calling ProxyApi->proxy_request_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain** | **str**| Configured proxy domain (the upstream host segment selecting the proxy). | 
 **path** | **str**| Path forwarded to the upstream root URL. | 

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The upstream response, streamed back verbatim (any media type). |  -  |
**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
**401** | Missing or unknown API key. |  -  |
**403** | Key not allowed to use this proxy. |  -  |
**404** | No proxy configured for this domain. |  -  |
**422** | Validation Error |  -  |
**502** | Every upstream account failed. |  -  |
**503** | The proxy has no configured account. |  -  |
**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **proxy_request_get**
> proxy_request_get(domain, path)

Forward a request through a domain-matched proxy

Forward an HTTP request through a domain-matched proxy to its upstream.

The path, query string, body, and most client headers are forwarded
verbatim to ``{base_url}/{path}``; the configured account's credential is
injected from the account's ``headers`` and the upstream response (including
event streams) is streamed back. Retries across accounts on a rate-limit /
timeout / 5xx.

### Example

* Bearer (API key) Authentication (BearerAuth):

```python
import mmgateway
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
    api_instance = mmgateway.ProxyApi(api_client)
    domain = 'domain_example' # str | Configured proxy domain (the upstream host segment selecting the proxy).
    path = 'path_example' # str | Path forwarded to the upstream root URL.

    try:
        # Forward a request through a domain-matched proxy
        api_instance.proxy_request_get(domain, path)
    except Exception as e:
        print("Exception when calling ProxyApi->proxy_request_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain** | **str**| Configured proxy domain (the upstream host segment selecting the proxy). | 
 **path** | **str**| Path forwarded to the upstream root URL. | 

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The upstream response, streamed back verbatim (any media type). |  -  |
**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
**401** | Missing or unknown API key. |  -  |
**403** | Key not allowed to use this proxy. |  -  |
**404** | No proxy configured for this domain. |  -  |
**422** | Validation Error |  -  |
**502** | Every upstream account failed. |  -  |
**503** | The proxy has no configured account. |  -  |
**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **proxy_request_head**
> proxy_request_head(domain, path)

Forward a request through a domain-matched proxy

Forward an HTTP request through a domain-matched proxy to its upstream.

The path, query string, body, and most client headers are forwarded
verbatim to ``{base_url}/{path}``; the configured account's credential is
injected from the account's ``headers`` and the upstream response (including
event streams) is streamed back. Retries across accounts on a rate-limit /
timeout / 5xx.

### Example

* Bearer (API key) Authentication (BearerAuth):

```python
import mmgateway
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
    api_instance = mmgateway.ProxyApi(api_client)
    domain = 'domain_example' # str | Configured proxy domain (the upstream host segment selecting the proxy).
    path = 'path_example' # str | Path forwarded to the upstream root URL.

    try:
        # Forward a request through a domain-matched proxy
        api_instance.proxy_request_head(domain, path)
    except Exception as e:
        print("Exception when calling ProxyApi->proxy_request_head: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain** | **str**| Configured proxy domain (the upstream host segment selecting the proxy). | 
 **path** | **str**| Path forwarded to the upstream root URL. | 

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The upstream response, streamed back verbatim (any media type). |  -  |
**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
**401** | Missing or unknown API key. |  -  |
**403** | Key not allowed to use this proxy. |  -  |
**404** | No proxy configured for this domain. |  -  |
**422** | Validation Error |  -  |
**502** | Every upstream account failed. |  -  |
**503** | The proxy has no configured account. |  -  |
**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **proxy_request_options**
> proxy_request_options(domain, path)

Forward a request through a domain-matched proxy

Forward an HTTP request through a domain-matched proxy to its upstream.

The path, query string, body, and most client headers are forwarded
verbatim to ``{base_url}/{path}``; the configured account's credential is
injected from the account's ``headers`` and the upstream response (including
event streams) is streamed back. Retries across accounts on a rate-limit /
timeout / 5xx.

### Example

* Bearer (API key) Authentication (BearerAuth):

```python
import mmgateway
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
    api_instance = mmgateway.ProxyApi(api_client)
    domain = 'domain_example' # str | Configured proxy domain (the upstream host segment selecting the proxy).
    path = 'path_example' # str | Path forwarded to the upstream root URL.

    try:
        # Forward a request through a domain-matched proxy
        api_instance.proxy_request_options(domain, path)
    except Exception as e:
        print("Exception when calling ProxyApi->proxy_request_options: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain** | **str**| Configured proxy domain (the upstream host segment selecting the proxy). | 
 **path** | **str**| Path forwarded to the upstream root URL. | 

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The upstream response, streamed back verbatim (any media type). |  -  |
**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
**401** | Missing or unknown API key. |  -  |
**403** | Key not allowed to use this proxy. |  -  |
**404** | No proxy configured for this domain. |  -  |
**422** | Validation Error |  -  |
**502** | Every upstream account failed. |  -  |
**503** | The proxy has no configured account. |  -  |
**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **proxy_request_patch**
> proxy_request_patch(domain, path)

Forward a request through a domain-matched proxy

Forward an HTTP request through a domain-matched proxy to its upstream.

The path, query string, body, and most client headers are forwarded
verbatim to ``{base_url}/{path}``; the configured account's credential is
injected from the account's ``headers`` and the upstream response (including
event streams) is streamed back. Retries across accounts on a rate-limit /
timeout / 5xx.

### Example

* Bearer (API key) Authentication (BearerAuth):

```python
import mmgateway
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
    api_instance = mmgateway.ProxyApi(api_client)
    domain = 'domain_example' # str | Configured proxy domain (the upstream host segment selecting the proxy).
    path = 'path_example' # str | Path forwarded to the upstream root URL.

    try:
        # Forward a request through a domain-matched proxy
        api_instance.proxy_request_patch(domain, path)
    except Exception as e:
        print("Exception when calling ProxyApi->proxy_request_patch: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain** | **str**| Configured proxy domain (the upstream host segment selecting the proxy). | 
 **path** | **str**| Path forwarded to the upstream root URL. | 

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The upstream response, streamed back verbatim (any media type). |  -  |
**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
**401** | Missing or unknown API key. |  -  |
**403** | Key not allowed to use this proxy. |  -  |
**404** | No proxy configured for this domain. |  -  |
**422** | Validation Error |  -  |
**502** | Every upstream account failed. |  -  |
**503** | The proxy has no configured account. |  -  |
**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **proxy_request_post**
> proxy_request_post(domain, path)

Forward a request through a domain-matched proxy

Forward an HTTP request through a domain-matched proxy to its upstream.

The path, query string, body, and most client headers are forwarded
verbatim to ``{base_url}/{path}``; the configured account's credential is
injected from the account's ``headers`` and the upstream response (including
event streams) is streamed back. Retries across accounts on a rate-limit /
timeout / 5xx.

### Example

* Bearer (API key) Authentication (BearerAuth):

```python
import mmgateway
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
    api_instance = mmgateway.ProxyApi(api_client)
    domain = 'domain_example' # str | Configured proxy domain (the upstream host segment selecting the proxy).
    path = 'path_example' # str | Path forwarded to the upstream root URL.

    try:
        # Forward a request through a domain-matched proxy
        api_instance.proxy_request_post(domain, path)
    except Exception as e:
        print("Exception when calling ProxyApi->proxy_request_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain** | **str**| Configured proxy domain (the upstream host segment selecting the proxy). | 
 **path** | **str**| Path forwarded to the upstream root URL. | 

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The upstream response, streamed back verbatim (any media type). |  -  |
**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
**401** | Missing or unknown API key. |  -  |
**403** | Key not allowed to use this proxy. |  -  |
**404** | No proxy configured for this domain. |  -  |
**422** | Validation Error |  -  |
**502** | Every upstream account failed. |  -  |
**503** | The proxy has no configured account. |  -  |
**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **proxy_request_put**
> proxy_request_put(domain, path)

Forward a request through a domain-matched proxy

Forward an HTTP request through a domain-matched proxy to its upstream.

The path, query string, body, and most client headers are forwarded
verbatim to ``{base_url}/{path}``; the configured account's credential is
injected from the account's ``headers`` and the upstream response (including
event streams) is streamed back. Retries across accounts on a rate-limit /
timeout / 5xx.

### Example

* Bearer (API key) Authentication (BearerAuth):

```python
import mmgateway
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
    api_instance = mmgateway.ProxyApi(api_client)
    domain = 'domain_example' # str | Configured proxy domain (the upstream host segment selecting the proxy).
    path = 'path_example' # str | Path forwarded to the upstream root URL.

    try:
        # Forward a request through a domain-matched proxy
        api_instance.proxy_request_put(domain, path)
    except Exception as e:
        print("Exception when calling ProxyApi->proxy_request_put: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain** | **str**| Configured proxy domain (the upstream host segment selecting the proxy). | 
 **path** | **str**| Path forwarded to the upstream root URL. | 

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The upstream response, streamed back verbatim (any media type). |  -  |
**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
**401** | Missing or unknown API key. |  -  |
**403** | Key not allowed to use this proxy. |  -  |
**404** | No proxy configured for this domain. |  -  |
**422** | Validation Error |  -  |
**502** | Every upstream account failed. |  -  |
**503** | The proxy has no configured account. |  -  |
**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

