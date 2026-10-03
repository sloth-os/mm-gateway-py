# ManagedKey


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**allow_backends** | **List[str]** |  | [optional] 
**allow_tags** | **List[str]** |  | [optional] 
**budget** | [**ManagedBudget**](ManagedBudget.md) |  | [optional] 
**default_audio_backend** | **str** |  | [optional] 
**default_audio_tag** | **str** |  | [optional] 
**default_image_backend** | **str** |  | [optional] 
**default_image_tag** | **str** |  | [optional] 
**default_music_backend** | **str** |  | [optional] 
**default_music_tag** | **str** |  | [optional] 
**default_video_backend** | **str** |  | [optional] 
**default_video_tag** | **str** |  | [optional] 
**deny_tags** | **List[str]** |  | [optional] 
**enabled** | **bool** |  | [optional] [default to True]
**extra** | **Dict[str, object]** |  | [optional] 
**id** | **str** |  | 
**key** | **str** |  | 

## Example

```python
from mmgateway.models.managed_key import ManagedKey

# TODO update the JSON string below
json = "{}"
# create an instance of ManagedKey from a JSON string
managed_key_instance = ManagedKey.from_json(json)
# print the JSON string representation of the object
print(ManagedKey.to_json())

# convert the object into a dict
managed_key_dict = managed_key_instance.to_dict()
# create an instance of ManagedKey from a dict
managed_key_from_dict = ManagedKey.from_dict(managed_key_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


