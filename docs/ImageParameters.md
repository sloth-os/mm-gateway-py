# ImageParameters


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**background** | **str** |  | [optional] 
**compression** | **int** |  | [optional] 
**delivery** | **str** |  | [optional] 
**dimensions** | [**Dimensions**](Dimensions.md) |  | [optional] 
**file_format** | **str** |  | [optional] 
**guidance_scale** | **float** |  | [optional] 
**inference_steps** | **int** |  | [optional] 
**negative_prompt** | **str** |  | [optional] 
**output_count** | **int** |  | [optional] 
**quality** | **str** |  | [optional] 
**seed** | **int** |  | [optional] 
**strength** | **float** |  | [optional] 
**style** | **str** |  | [optional] 
**watermark** | **bool** |  | [optional] 

## Example

```python
from mmgateway.models.image_parameters import ImageParameters

# TODO update the JSON string below
json = "{}"
# create an instance of ImageParameters from a JSON string
image_parameters_instance = ImageParameters.from_json(json)
# print the JSON string representation of the object
print(ImageParameters.to_json())

# convert the object into a dict
image_parameters_dict = image_parameters_instance.to_dict()
# create an instance of ImageParameters from a dict
image_parameters_from_dict = ImageParameters.from_dict(image_parameters_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


