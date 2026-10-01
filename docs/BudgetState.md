# BudgetState

The state of one budget (a key's period or a client scope).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**limit_usd** | **float** |  | [optional] 
**remaining_usd** | **float** |  | [optional] 
**reserved_usd** | **float** |  | [optional] [default to 0.0]
**scope** | **str** |  | [optional] 
**spent_usd** | **float** |  | [optional] [default to 0.0]
**tasks** | **int** |  | [optional] 

## Example

```python
from mmgateway.models.budget_state import BudgetState

# TODO update the JSON string below
json = "{}"
# create an instance of BudgetState from a JSON string
budget_state_instance = BudgetState.from_json(json)
# print the JSON string representation of the object
print(BudgetState.to_json())

# convert the object into a dict
budget_state_dict = budget_state_instance.to_dict()
# create an instance of BudgetState from a dict
budget_state_from_dict = BudgetState.from_dict(budget_state_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


