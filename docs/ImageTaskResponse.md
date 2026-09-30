# ImageTaskResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**completed_at** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | 
**error** | [**TaskError**](TaskError.md) |  | [optional] 
**id** | **str** |  | 
**links** | [**ResourceLinks**](ResourceLinks.md) |  | 
**metadata** | **Dict[str, object]** |  | [optional] 
**model** | **str** |  | 
**object** | **str** |  | [optional] [default to 'image']
**outputs** | [**List[ImageOutput]**](ImageOutput.md) |  | [optional] 
**status** | **str** |  | 
**usage** | [**Usage**](Usage.md) |  | [optional] 

## Example

```python
from mmgateway.models.image_task_response import ImageTaskResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ImageTaskResponse from a JSON string
image_task_response_instance = ImageTaskResponse.from_json(json)
# print the JSON string representation of the object
print(ImageTaskResponse.to_json())

# convert the object into a dict
image_task_response_dict = image_task_response_instance.to_dict()
# create an instance of ImageTaskResponse from a dict
image_task_response_from_dict = ImageTaskResponse.from_dict(image_task_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


