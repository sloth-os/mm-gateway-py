# EstimateCandidate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**admissible** | **bool** |  | [optional] [default to True]
**estimated_cost** | **float** |  | [optional] 
**lifecycle** | **str** |  | [optional] [default to 'active']
**model** | **str** |  | 
**reason** | **str** | Why the candidate is not admissible: limits, retired, max_cost, unpriced or budget. | [optional] 

## Example

```python
from mmgateway.models.estimate_candidate import EstimateCandidate

# TODO update the JSON string below
json = "{}"
# create an instance of EstimateCandidate from a JSON string
estimate_candidate_instance = EstimateCandidate.from_json(json)
# print the JSON string representation of the object
print(EstimateCandidate.to_json())

# convert the object into a dict
estimate_candidate_dict = estimate_candidate_instance.to_dict()
# create an instance of EstimateCandidate from a dict
estimate_candidate_from_dict = EstimateCandidate.from_dict(estimate_candidate_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


