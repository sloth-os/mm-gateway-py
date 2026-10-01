# VideoTaskResponse


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
**object** | **str** |  | [optional] [default to 'video']
**outputs** | [**List[VideoOutput]**](VideoOutput.md) |  | [optional] 
**routing** | [**RoutingInfo**](RoutingInfo.md) |  | [optional] 
**status** | **str** |  | 
**usage** | [**Usage**](Usage.md) |  | [optional] 

## Example

```python
from mmgateway.models.video_task_response import VideoTaskResponse

# TODO update the JSON string below
json = "{}"
# create an instance of VideoTaskResponse from a JSON string
video_task_response_instance = VideoTaskResponse.from_json(json)
# print the JSON string representation of the object
print(VideoTaskResponse.to_json())

# convert the object into a dict
video_task_response_dict = video_task_response_instance.to_dict()
# create an instance of VideoTaskResponse from a dict
video_task_response_from_dict = VideoTaskResponse.from_dict(video_task_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


