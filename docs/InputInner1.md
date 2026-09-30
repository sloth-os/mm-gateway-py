# InputInner1


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** |  | 
**type** | **str** |  | 
**role** | **str** |  | [optional] [default to 'reference_audio']
**uri** | **str** | Absolute media URI. Inline media uses a base64 data URI. | 

## Example

```python
from mmgateway.models.input_inner1 import InputInner1

# TODO update the JSON string below
json = "{}"
# create an instance of InputInner1 from a JSON string
input_inner1_instance = InputInner1.from_json(json)
# print the JSON string representation of the object
print(InputInner1.to_json())

# convert the object into a dict
input_inner1_dict = input_inner1_instance.to_dict()
# create an instance of InputInner1 from a dict
input_inner1_from_dict = InputInner1.from_dict(input_inner1_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


