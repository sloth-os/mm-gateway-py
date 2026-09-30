# ProblemDetail

RFC 9457 problem details with stable gateway extensions.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **str** | Stable machine-readable gateway error code. | 
**detail** | **str** | Human-readable detail for this occurrence. | 
**errors** | **List[Dict[str, object]]** | Field-level validation errors, when applicable. | [optional] 
**instance** | **str** | Previously returned ETag; unchanged resources return 304. | [optional] 
**request_id** | **str** | Previously returned ETag; unchanged resources return 304. | [optional] 
**status** | **int** | HTTP response status code. | 
**title** | **str** | Short, stable summary of the problem type. | 
**type** | **str** | URI identifying the problem type. | 

## Example

```python
from mmgateway.models.problem_detail import ProblemDetail

# TODO update the JSON string below
json = "{}"
# create an instance of ProblemDetail from a JSON string
problem_detail_instance = ProblemDetail.from_json(json)
# print the JSON string representation of the object
print(ProblemDetail.to_json())

# convert the object into a dict
problem_detail_dict = problem_detail_instance.to_dict()
# create an instance of ProblemDetail from a dict
problem_detail_from_dict = ProblemDetail.from_dict(problem_detail_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


