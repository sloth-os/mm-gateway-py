# AudioTaskResponse


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
**object** | **str** |  | [optional] [default to 'audio']
**outputs** | [**List[AudioOutput]**](AudioOutput.md) |  | [optional] 
**routing** | [**RoutingInfo**](RoutingInfo.md) |  | [optional] 
**status** | **str** |  | 
**usage** | [**Usage**](Usage.md) |  | [optional] 

## Example

```python
from mmgateway.models.audio_task_response import AudioTaskResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AudioTaskResponse from a JSON string
audio_task_response_instance = AudioTaskResponse.from_json(json)
# print the JSON string representation of the object
print(AudioTaskResponse.to_json())

# convert the object into a dict
audio_task_response_dict = audio_task_response_instance.to_dict()
# create an instance of AudioTaskResponse from a dict
audio_task_response_from_dict = AudioTaskResponse.from_dict(audio_task_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


