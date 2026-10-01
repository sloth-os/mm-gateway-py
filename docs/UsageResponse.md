# UsageResponse

Spend, reservations and budgets of the authenticated key.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency** | **str** |  | [optional] [default to 'USD']
**key** | [**BudgetState**](BudgetState.md) |  | 
**models** | [**List[ModelSpend]**](ModelSpend.md) |  | [optional] 
**object** | **str** |  | [optional] [default to 'usage']
**period** | [**UsagePeriod**](UsagePeriod.md) |  | 
**scopes** | [**List[BudgetState]**](BudgetState.md) |  | [optional] 

## Example

```python
from mmgateway.models.usage_response import UsageResponse

# TODO update the JSON string below
json = "{}"
# create an instance of UsageResponse from a JSON string
usage_response_instance = UsageResponse.from_json(json)
# print the JSON string representation of the object
print(UsageResponse.to_json())

# convert the object into a dict
usage_response_dict = usage_response_instance.to_dict()
# create an instance of UsageResponse from a dict
usage_response_from_dict = UsageResponse.from_dict(usage_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


