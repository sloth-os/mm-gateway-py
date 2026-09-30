# ModelLimitsListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**List[ModelLimitsEntry]**](ModelLimitsEntry.md) |  | 
**object** | **str** |  | [optional] [default to 'list']

## Example

```python
from mmgateway.models.model_limits_list_response import ModelLimitsListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ModelLimitsListResponse from a JSON string
model_limits_list_response_instance = ModelLimitsListResponse.from_json(json)
# print the JSON string representation of the object
print(ModelLimitsListResponse.to_json())

# convert the object into a dict
model_limits_list_response_dict = model_limits_list_response_instance.to_dict()
# create an instance of ModelLimitsListResponse from a dict
model_limits_list_response_from_dict = ModelLimitsListResponse.from_dict(model_limits_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


