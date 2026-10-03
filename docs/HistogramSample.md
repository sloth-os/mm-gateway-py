# HistogramSample


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**count** | **int** |  | 
**labels** | **Dict[str, str]** |  | 
**max** | **float** |  | 
**mean** | **float** |  | 
**min** | **float** |  | 
**name** | **str** |  | 
**sum** | **float** |  | 

## Example

```python
from mmgateway.models.histogram_sample import HistogramSample

# TODO update the JSON string below
json = "{}"
# create an instance of HistogramSample from a JSON string
histogram_sample_instance = HistogramSample.from_json(json)
# print the JSON string representation of the object
print(HistogramSample.to_json())

# convert the object into a dict
histogram_sample_dict = histogram_sample_instance.to_dict()
# create an instance of HistogramSample from a dict
histogram_sample_from_dict = HistogramSample.from_dict(histogram_sample_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


