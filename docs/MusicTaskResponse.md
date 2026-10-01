# MusicTaskResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**completed_at** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | 
**error** | [**TaskError**](TaskError.md) |  | [optional] 
**id** | **str** |  | 
**links** | [**ResourceLinks**](ResourceLinks.md) |  | 
**lyrics** | **str** |  | [optional] 
**metadata** | **Dict[str, object]** |  | [optional] 
**model** | **str** |  | 
**object** | **str** |  | [optional] [default to 'music']
**outputs** | [**List[MusicOutput]**](MusicOutput.md) |  | [optional] 
**routing** | [**RoutingInfo**](RoutingInfo.md) |  | [optional] 
**status** | **str** |  | 
**usage** | [**Usage**](Usage.md) |  | [optional] 

## Example

```python
from mmgateway.models.music_task_response import MusicTaskResponse

# TODO update the JSON string below
json = "{}"
# create an instance of MusicTaskResponse from a JSON string
music_task_response_instance = MusicTaskResponse.from_json(json)
# print the JSON string representation of the object
print(MusicTaskResponse.to_json())

# convert the object into a dict
music_task_response_dict = music_task_response_instance.to_dict()
# create an instance of MusicTaskResponse from a dict
music_task_response_from_dict = MusicTaskResponse.from_dict(music_task_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


