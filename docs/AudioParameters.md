# AudioParameters


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**bitrate_kbps** | **int** |  | [optional] 
**delivery** | **str** |  | [optional] 
**file_format** | **str** |  | [optional] 
**instructions** | **str** |  | [optional] 
**language** | **str** |  | [optional] 
**sample_rate_hz** | **int** |  | [optional] 
**seed** | **int** |  | [optional] 
**speed** | **float** |  | [optional] 
**voice** | **str** | A gateway voice id from GET /v1/voices. | [optional] [default to 'default']

## Example

```python
from mmgateway.models.audio_parameters import AudioParameters

# TODO update the JSON string below
json = "{}"
# create an instance of AudioParameters from a JSON string
audio_parameters_instance = AudioParameters.from_json(json)
# print the JSON string representation of the object
print(AudioParameters.to_json())

# convert the object into a dict
audio_parameters_dict = audio_parameters_instance.to_dict()
# create an instance of AudioParameters from a dict
audio_parameters_from_dict = AudioParameters.from_dict(audio_parameters_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


