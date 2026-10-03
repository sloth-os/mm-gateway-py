# ManagedUsage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** |  | 
**key_id** | **str** |  | 
**usage** | [**UsageResponse**](UsageResponse.md) |  | 

## Example

```python
from mmgateway.models.managed_usage import ManagedUsage

# TODO update the JSON string below
json = "{}"
# create an instance of ManagedUsage from a JSON string
managed_usage_instance = ManagedUsage.from_json(json)
# print the JSON string representation of the object
print(ManagedUsage.to_json())

# convert the object into a dict
managed_usage_dict = managed_usage_instance.to_dict()
# create an instance of ManagedUsage from a dict
managed_usage_from_dict = ManagedUsage.from_dict(managed_usage_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


