# ApiHistoryResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**list** | [**List[HistoryItem]**](HistoryItem.md) |  | 

## Example

```python
from openapi_client.models.api_history_response import ApiHistoryResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ApiHistoryResponse from a JSON string
api_history_response_instance = ApiHistoryResponse.from_json(json)
# print the JSON string representation of the object
print(ApiHistoryResponse.to_json())

# convert the object into a dict
api_history_response_dict = api_history_response_instance.to_dict()
# create an instance of ApiHistoryResponse from a dict
api_history_response_from_dict = ApiHistoryResponse.from_dict(api_history_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


