# ProxyRuntime


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**accounts** | **List[str]** |  | 
**active** | **bool** |  | 
**domain** | **str** |  | 
**enabled** | **bool** |  | 

## Example

```python
from mmgateway.models.proxy_runtime import ProxyRuntime

# TODO update the JSON string below
json = "{}"
# create an instance of ProxyRuntime from a JSON string
proxy_runtime_instance = ProxyRuntime.from_json(json)
# print the JSON string representation of the object
print(ProxyRuntime.to_json())

# convert the object into a dict
proxy_runtime_dict = proxy_runtime_instance.to_dict()
# create an instance of ProxyRuntime from a dict
proxy_runtime_from_dict = ProxyRuntime.from_dict(proxy_runtime_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


