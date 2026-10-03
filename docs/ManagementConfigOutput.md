# ManagementConfigOutput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**backends** | [**List[ManagedBackend]**](ManagedBackend.md) |  | [optional] 
**budget_allow_unpriced** | **bool** |  | [optional] [default to False]
**catalog_models** | **Dict[str, object]** |  | [optional] 
**keys** | [**List[ManagedKey]**](ManagedKey.md) |  | [optional] 
**outbound_proxy** | **str** |  | [optional] 
**proxies** | [**List[ManagedProxy]**](ManagedProxy.md) |  | [optional] 
**routing_default_optimize** | **str** |  | [optional] [default to 'balanced']
**routing_profiles** | [**Dict[str, ManagedRoutingProfile]**](ManagedRoutingProfile.md) |  | [optional] 

## Example

```python
from mmgateway.models.management_config_output import ManagementConfigOutput

# TODO update the JSON string below
json = "{}"
# create an instance of ManagementConfigOutput from a JSON string
management_config_output_instance = ManagementConfigOutput.from_json(json)
# print the JSON string representation of the object
print(ManagementConfigOutput.to_json())

# convert the object into a dict
management_config_output_dict = management_config_output_instance.to_dict()
# create an instance of ManagementConfigOutput from a dict
management_config_output_from_dict = ManagementConfigOutput.from_dict(management_config_output_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


