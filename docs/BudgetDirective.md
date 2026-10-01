# BudgetDirective

A client-chosen spend bucket within the key, optionally self-capped.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**limit_usd** | **float** | Self-imposed cap for the scope in USD (the operator&#39;s scope cap still applies). | [optional] 
**scope** | **str** | Spend bucket name (a project, a customer, a batch). | 

## Example

```python
from mmgateway.models.budget_directive import BudgetDirective

# TODO update the JSON string below
json = "{}"
# create an instance of BudgetDirective from a JSON string
budget_directive_instance = BudgetDirective.from_json(json)
# print the JSON string representation of the object
print(BudgetDirective.to_json())

# convert the object into a dict
budget_directive_dict = budget_directive_instance.to_dict()
# create an instance of BudgetDirective from a dict
budget_directive_from_dict = BudgetDirective.from_dict(budget_directive_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


