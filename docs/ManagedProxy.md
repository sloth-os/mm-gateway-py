# ManagedProxy


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**accounts** | [**List[ProxyAccount]**](ProxyAccount.md) |  | [optional] 
**base_url** | **str** |  | 
**domain** | **str** |  | [optional] 
**enabled** | **bool** |  | [optional] [default to True]
**headers** | **Dict[str, str]** |  | [optional] 
**outbound_proxy** | **str** |  | [optional] 
**tags** | **List[str]** |  | [optional] 
**timeout** | **float** |  | [optional] [default to 120]

## Example

```python
from mmgateway.models.managed_proxy import ManagedProxy

# TODO update the JSON string below
json = "{}"
# create an instance of ManagedProxy from a JSON string
managed_proxy_instance = ManagedProxy.from_json(json)
# print the JSON string representation of the object
print(ManagedProxy.to_json())

# convert the object into a dict
managed_proxy_dict = managed_proxy_instance.to_dict()
# create an instance of ManagedProxy from a dict
managed_proxy_from_dict = ManagedProxy.from_dict(managed_proxy_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


