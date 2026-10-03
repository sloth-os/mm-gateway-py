# ProxyAccount


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**headers** | **Dict[str, str]** |  | [optional] 
**id** | **str** |  | 

## Example

```python
from mmgateway.models.proxy_account import ProxyAccount

# TODO update the JSON string below
json = "{}"
# create an instance of ProxyAccount from a JSON string
proxy_account_instance = ProxyAccount.from_json(json)
# print the JSON string representation of the object
print(ProxyAccount.to_json())

# convert the object into a dict
proxy_account_dict = proxy_account_instance.to_dict()
# create an instance of ProxyAccount from a dict
proxy_account_from_dict = ProxyAccount.from_dict(proxy_account_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


