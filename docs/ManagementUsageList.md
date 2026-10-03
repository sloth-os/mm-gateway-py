# ManagementUsageList


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**List[ManagedUsage]**](ManagedUsage.md) |  | 
**object** | **str** |  | [optional] [default to 'list']

## Example

```python
from mmgateway.models.management_usage_list import ManagementUsageList

# TODO update the JSON string below
json = "{}"
# create an instance of ManagementUsageList from a JSON string
management_usage_list_instance = ManagementUsageList.from_json(json)
# print the JSON string representation of the object
print(ManagementUsageList.to_json())

# convert the object into a dict
management_usage_list_dict = management_usage_list_instance.to_dict()
# create an instance of ManagementUsageList from a dict
management_usage_list_from_dict = ManagementUsageList.from_dict(management_usage_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


