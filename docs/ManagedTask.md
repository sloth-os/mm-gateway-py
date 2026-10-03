# ManagedTask


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**backend** | **str** |  | 
**completed_at** | **int** |  | [optional] 
**created_at** | **int** |  | 
**id** | **str** |  | 
**modality** | **str** |  | 
**model** | **str** |  | 
**owner_key_id** | **str** |  | 
**status** | **str** |  | 

## Example

```python
from mmgateway.models.managed_task import ManagedTask

# TODO update the JSON string below
json = "{}"
# create an instance of ManagedTask from a JSON string
managed_task_instance = ManagedTask.from_json(json)
# print the JSON string representation of the object
print(ManagedTask.to_json())

# convert the object into a dict
managed_task_dict = managed_task_instance.to_dict()
# create an instance of ManagedTask from a dict
managed_task_from_dict = ManagedTask.from_dict(managed_task_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


