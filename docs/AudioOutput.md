# AudioOutput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channels** | **int** |  | [optional] 
**duration_seconds** | **float** |  | [optional] 
**mime_type** | **str** |  | [optional] 
**sample_rate_hz** | **int** |  | [optional] 
**uri** | **str** | Absolute media URI. Inline media uses a base64 data URI. | 

## Example

```python
from mmgateway.models.audio_output import AudioOutput

# TODO update the JSON string below
json = "{}"
# create an instance of AudioOutput from a JSON string
audio_output_instance = AudioOutput.from_json(json)
# print the JSON string representation of the object
print(AudioOutput.to_json())

# convert the object into a dict
audio_output_dict = audio_output_instance.to_dict()
# create an instance of AudioOutput from a dict
audio_output_from_dict = AudioOutput.from_dict(audio_output_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


