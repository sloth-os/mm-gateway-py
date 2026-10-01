# EstimateResponse

The routing and cost a create would get, without creating a task.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**budget** | [**BudgetState**](BudgetState.md) |  | [optional] 
**candidates** | [**List[EstimateCandidate]**](EstimateCandidate.md) |  | [optional] 
**currency** | **str** |  | [optional] [default to 'USD']
**estimated_cost** | **float** |  | [optional] 
**modality** | **str** |  | 
**model** | **str** |  | [optional] 
**object** | **str** |  | [optional] [default to 'estimate']

## Example

```python
from mmgateway.models.estimate_response import EstimateResponse

# TODO update the JSON string below
json = "{}"
# create an instance of EstimateResponse from a JSON string
estimate_response_instance = EstimateResponse.from_json(json)
# print the JSON string representation of the object
print(EstimateResponse.to_json())

# convert the object into a dict
estimate_response_dict = estimate_response_instance.to_dict()
# create an instance of EstimateResponse from a dict
estimate_response_from_dict = EstimateResponse.from_dict(estimate_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


