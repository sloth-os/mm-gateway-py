# ManagementTaskList


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**List[ManagedTask]**](ManagedTask.md) |  | 
**limit** | **int** |  | 
**object** | **str** |  | [optional] [default to 'list']
**offset** | **int** |  | 
**total** | **int** |  | 

## Example

```python
from mmgateway.models.management_task_list import ManagementTaskList

# TODO update the JSON string below
json = "{}"
# create an instance of ManagementTaskList from a JSON string
management_task_list_instance = ManagementTaskList.from_json(json)
# print the JSON string representation of the object
print(ManagementTaskList.to_json())

# convert the object into a dict
management_task_list_dict = management_task_list_instance.to_dict()
# create an instance of ManagementTaskList from a dict
management_task_list_from_dict = ManagementTaskList.from_dict(management_task_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


