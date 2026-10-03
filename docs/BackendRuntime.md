# BackendRuntime


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**accounts** | **List[str]** |  | 
**active** | **bool** |  | 
**configured** | **bool** |  | 
**enabled** | **bool** |  | 
**models** | **Dict[str, List[str]]** |  | 
**name** | **str** |  | 
**tags** | **List[str]** |  | 
**type** | **str** |  | 

## Example

```python
from mmgateway.models.backend_runtime import BackendRuntime

# TODO update the JSON string below
json = "{}"
# create an instance of BackendRuntime from a JSON string
backend_runtime_instance = BackendRuntime.from_json(json)
# print the JSON string representation of the object
print(BackendRuntime.to_json())

# convert the object into a dict
backend_runtime_dict = backend_runtime_instance.to_dict()
# create an instance of BackendRuntime from a dict
backend_runtime_from_dict = BackendRuntime.from_dict(backend_runtime_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


