# ApiVideoStreamBody


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**force** | **bool** | Force stream opening even if already active | 

## Example

```python
from openapi_client.models.api_video_stream_body import ApiVideoStreamBody

# TODO update the JSON string below
json = "{}"
# create an instance of ApiVideoStreamBody from a JSON string
api_video_stream_body_instance = ApiVideoStreamBody.from_json(json)
# print the JSON string representation of the object
print(ApiVideoStreamBody.to_json())

# convert the object into a dict
api_video_stream_body_dict = api_video_stream_body_instance.to_dict()
# create an instance of ApiVideoStreamBody from a dict
api_video_stream_body_from_dict = ApiVideoStreamBody.from_dict(api_video_stream_body_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


