# LyricsInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** |  | 
**type** | **str** |  | 

## Example

```python
from mmgateway.models.lyrics_input import LyricsInput

# TODO update the JSON string below
json = "{}"
# create an instance of LyricsInput from a JSON string
lyrics_input_instance = LyricsInput.from_json(json)
# print the JSON string representation of the object
print(LyricsInput.to_json())

# convert the object into a dict
lyrics_input_dict = lyrics_input_instance.to_dict()
# create an instance of LyricsInput from a dict
lyrics_input_from_dict = LyricsInput.from_dict(lyrics_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


