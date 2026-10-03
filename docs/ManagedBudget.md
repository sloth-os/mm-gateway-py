# ManagedBudget


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**limit_usd** | **float** |  | [optional] 
**period** | **str** |  | [optional] [default to 'month']
**scopes_limit_usd** | **float** |  | [optional] 

## Example

```python
from mmgateway.models.managed_budget import ManagedBudget

# TODO update the JSON string below
json = "{}"
# create an instance of ManagedBudget from a JSON string
managed_budget_instance = ManagedBudget.from_json(json)
# print the JSON string representation of the object
print(ManagedBudget.to_json())

# convert the object into a dict
managed_budget_dict = managed_budget_instance.to_dict()
# create an instance of ManagedBudget from a dict
managed_budget_from_dict = ManagedBudget.from_dict(managed_budget_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


