# ManagementStatus


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**backend_types** | **List[str]** |  | 
**backends** | [**List[BackendRuntime]**](BackendRuntime.md) |  | 
**enabled_keys_count** | **int** |  | 
**keys_count** | **int** |  | 
**metrics_enabled** | **bool** |  | 
**persistent** | **bool** |  | 
**proxies** | [**List[ProxyRuntime]**](ProxyRuntime.md) |  | 
**revision** | **str** |  | 
**status** | **str** |  | [optional] [default to 'ok']
**tasks_by_status** | **Dict[str, int]** |  | 
**uptime_seconds** | **float** |  | 
**version** | **str** |  | 

## Example

```python
from mmgateway.models.management_status import ManagementStatus

# TODO update the JSON string below
json = "{}"
# create an instance of ManagementStatus from a JSON string
management_status_instance = ManagementStatus.from_json(json)
# print the JSON string representation of the object
print(ManagementStatus.to_json())

# convert the object into a dict
management_status_dict = management_status_instance.to_dict()
# create an instance of ManagementStatus from a dict
management_status_from_dict = ManagementStatus.from_dict(management_status_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


