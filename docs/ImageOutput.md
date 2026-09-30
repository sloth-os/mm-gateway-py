# ImageOutput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**mime_type** | **str** |  | [optional] 
**revised_prompt** | **str** |  | [optional] 
**uri** | **str** | Absolute media URI. Inline media uses a base64 data URI. | 

## Example

```python
from mmgateway.models.image_output import ImageOutput

# TODO update the JSON string below
json = "{}"
# create an instance of ImageOutput from a JSON string
image_output_instance = ImageOutput.from_json(json)
# print the JSON string representation of the object
print(ImageOutput.to_json())

# convert the object into a dict
image_output_dict = image_output_instance.to_dict()
# create an instance of ImageOutput from a dict
image_output_from_dict = ImageOutput.from_dict(image_output_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


