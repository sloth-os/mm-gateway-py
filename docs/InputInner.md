# InputInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** |  | 
**type** | **str** |  | 
**uri** | **str** | Absolute media URI. Inline media uses a base64 data URI. | 

## Example

```python
from mmgateway.models.input_inner import InputInner

# TODO update the JSON string below
json = "{}"
# create an instance of InputInner from a JSON string
input_inner_instance = InputInner.from_json(json)
# print the JSON string representation of the object
print(InputInner.to_json())

# convert the object into a dict
input_inner_dict = input_inner_instance.to_dict()
# create an instance of InputInner from a dict
input_inner_from_dict = InputInner.from_dict(input_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


