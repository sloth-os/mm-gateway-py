# TaskError


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **str** |  | 
**message** | **str** |  | 

## Example

```python
from mmgateway.models.task_error import TaskError

# TODO update the JSON string below
json = "{}"
# create an instance of TaskError from a JSON string
task_error_instance = TaskError.from_json(json)
# print the JSON string representation of the object
print(TaskError.to_json())

# convert the object into a dict
task_error_dict = task_error_instance.to_dict()
# create an instance of TaskError from a dict
task_error_from_dict = TaskError.from_dict(task_error_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


