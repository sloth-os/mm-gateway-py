# ManagedRoutingProfile


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fallback** | **str** |  | [optional] 
**max_cost_usd** | **float** |  | [optional] 
**optimize** | **str** |  | [optional] 
**tags** | **List[str]** |  | [optional] 

## Example

```python
from mmgateway.models.managed_routing_profile import ManagedRoutingProfile

# TODO update the JSON string below
json = "{}"
# create an instance of ManagedRoutingProfile from a JSON string
managed_routing_profile_instance = ManagedRoutingProfile.from_json(json)
# print the JSON string representation of the object
print(ManagedRoutingProfile.to_json())

# convert the object into a dict
managed_routing_profile_dict = managed_routing_profile_instance.to_dict()
# create an instance of ManagedRoutingProfile from a dict
managed_routing_profile_from_dict = ManagedRoutingProfile.from_dict(managed_routing_profile_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


