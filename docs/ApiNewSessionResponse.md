# ApiNewSessionResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**session** | **str** | Session ID for authenticated requests | 

## Example

```python
from openapi_client.models.api_new_session_response import ApiNewSessionResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ApiNewSessionResponse from a JSON string
api_new_session_response_instance = ApiNewSessionResponse.from_json(json)
# print the JSON string representation of the object
print(ApiNewSessionResponse.to_json())

# convert the object into a dict
api_new_session_response_dict = api_new_session_response_instance.to_dict()
# create an instance of ApiNewSessionResponse from a dict
api_new_session_response_from_dict = ApiNewSessionResponse.from_dict(api_new_session_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


