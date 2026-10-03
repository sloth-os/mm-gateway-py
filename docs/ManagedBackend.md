# ManagedBackend


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**api_key** | **str** |  | [optional] 
**base_url** | **str** |  | [optional] 
**credentials** | [**List[BackendCredential]**](BackendCredential.md) |  | [optional] 
**enabled** | **bool** |  | [optional] [default to True]
**extra** | **Dict[str, object]** |  | [optional] 
**name** | **str** |  | 
**tags** | **List[str]** |  | [optional] 
**type** | **str** |  | 

## Example

```python
from mmgateway.models.managed_backend import ManagedBackend

# TODO update the JSON string below
json = "{}"
# create an instance of ManagedBackend from a JSON string
managed_backend_instance = ManagedBackend.from_json(json)
# print the JSON string representation of the object
print(ManagedBackend.to_json())

# convert the object into a dict
managed_backend_dict = managed_backend_instance.to_dict()
# create an instance of ManagedBackend from a dict
managed_backend_from_dict = ManagedBackend.from_dict(managed_backend_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


