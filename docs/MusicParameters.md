# MusicParameters


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**bitrate_kbps** | **int** |  | [optional] 
**bpm** | **int** |  | [optional] 
**duration_seconds** | **float** |  | [optional] 
**enhance_lyrics** | **bool** |  | [optional] 
**file_format** | **str** |  | [optional] 
**guidance_scale** | **float** |  | [optional] 
**inference_steps** | **int** |  | [optional] 
**instrumental** | **bool** |  | [optional] 
**key** | **str** |  | [optional] 
**negative_prompt** | **str** |  | [optional] 
**novelty** | **float** |  | [optional] 
**output_count** | **int** |  | [optional] 
**provenance** | **bool** |  | [optional] 
**reference_audio_strength** | **float** |  | [optional] 
**respect_section_durations** | **bool** |  | [optional] 
**sample_rate_hz** | **int** |  | [optional] 
**scale** | **str** |  | [optional] 
**seed** | **int** |  | [optional] 
**style** | **str** |  | [optional] 
**style_strength** | **float** |  | [optional] 
**time_signature** | **str** |  | [optional] 
**title** | **str** |  | [optional] 
**vocal_gender** | **str** |  | [optional] 
**vocal_language** | **str** |  | [optional] 
**voice** | **str** |  | [optional] 

## Example

```python
from mmgateway.models.music_parameters import MusicParameters

# TODO update the JSON string below
json = "{}"
# create an instance of MusicParameters from a JSON string
music_parameters_instance = MusicParameters.from_json(json)
# print the JSON string representation of the object
print(MusicParameters.to_json())

# convert the object into a dict
music_parameters_dict = music_parameters_instance.to_dict()
# create an instance of MusicParameters from a dict
music_parameters_from_dict = MusicParameters.from_dict(music_parameters_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


