# InputInner2


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** |  | 
**type** | **str** |  | 
**role** | **str** |  | [optional] [default to 'reference_video']
**uri** | **str** | Absolute media URI. Inline media uses a base64 data URI. | 

## Example

```python
from mmgateway.models.input_inner2 import InputInner2

# TODO update the JSON string below
json = "{}"
# create an instance of InputInner2 from a JSON string
input_inner2_instance = InputInner2.from_json(json)
# print the JSON string representation of the object
print(InputInner2.to_json())

# convert the object into a dict
input_inner2_dict = input_inner2_instance.to_dict()
# create an instance of InputInner2 from a dict
input_inner2_from_dict = InputInner2.from_dict(input_inner2_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


