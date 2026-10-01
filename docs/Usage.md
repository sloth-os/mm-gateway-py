# Usage

Provider-neutral usage fields shared by all three modalities.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cost** | **float** |  | [optional] 
**cost_source** | **str** |  | [optional] 
**currency** | **str** |  | [optional] 
**duration_seconds** | **float** |  | [optional] 
**input_tokens** | **int** |  | [optional] 
**output_count** | **int** |  | [optional] 
**output_tokens** | **int** |  | [optional] 
**total_tokens** | **int** |  | [optional] 

## Example

```python
from mmgateway.models.usage import Usage

# TODO update the JSON string below
json = "{}"
# create an instance of Usage from a JSON string
usage_instance = Usage.from_json(json)
# print the JSON string representation of the object
print(Usage.to_json())

# convert the object into a dict
usage_dict = usage_instance.to_dict()
# create an instance of Usage from a dict
usage_from_dict = Usage.from_dict(usage_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


