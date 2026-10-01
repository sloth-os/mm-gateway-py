# RoutingInfo

How auto mode served a task (docs/design/auto-mode.md#fallbacks).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attempts** | **int** |  | [optional] [default to 1]
**budget** | [**BudgetState**](BudgetState.md) |  | [optional] 
**estimated_cost** | **float** |  | [optional] 
**fallback** | **bool** |  | [optional] [default to False]
**fallback_reason** | **str** |  | [optional] 
**optimize** | **str** |  | [optional] [default to 'balanced']
**requested_model** | **str** |  | 

## Example

```python
from mmgateway.models.routing_info import RoutingInfo

# TODO update the JSON string below
json = "{}"
# create an instance of RoutingInfo from a JSON string
routing_info_instance = RoutingInfo.from_json(json)
# print the JSON string representation of the object
print(RoutingInfo.to_json())

# convert the object into a dict
routing_info_dict = routing_info_instance.to_dict()
# create an instance of RoutingInfo from a dict
routing_info_from_dict = RoutingInfo.from_dict(routing_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


