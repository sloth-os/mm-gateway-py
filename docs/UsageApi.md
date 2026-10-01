# mmgateway.UsageApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_usage**](UsageApi.md#get_usage) | **GET** /v1/usage | Spend and budgets of the authenticated key


# **get_usage**
> UsageResponse get_usage(scope=scope)

Spend and budgets of the authenticated key

### Example

* Bearer (API key) Authentication (BearerAuth):

```python
import mmgateway
from mmgateway.models.usage_response import UsageResponse
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
    api_instance = mmgateway.UsageApi(api_client)
    scope = 'scope_example' # str | Report only this budget scope. (optional)

    try:
        # Spend and budgets of the authenticated key
        api_response = api_instance.get_usage(scope=scope)
        print("The response of UsageApi->get_usage:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsageApi->get_usage: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **scope** | **str**| Report only this budget scope. | [optional] 

### Return type

[**UsageResponse**](UsageResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Spend, reservations and budgets for the current period. |  -  |
**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
**401** | Missing or unknown API key (unauthorized). |  -  |
**403** | Key not allowed to perform the request (forbidden). |  -  |
**404** | Model or task not found. |  -  |
**422** | Validation Error |  -  |
**502** | Generation service returned an error. |  -  |
**503** | No usable generation service is configured. |  -  |
**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

