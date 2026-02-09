# ApiHistoryBody


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**count** | **int** | Number of history items to retrieve | 
**offset** | **int** | Offset for pagination | 
**var_date** | **int** | Timestamp to filter events after this date | [optional] 

## Example

```python
from openapi_client.models.api_history_body import ApiHistoryBody

# TODO update the JSON string below
json = "{}"
# create an instance of ApiHistoryBody from a JSON string
api_history_body_instance = ApiHistoryBody.from_json(json)
# print the JSON string representation of the object
print(ApiHistoryBody.to_json())

# convert the object into a dict
api_history_body_dict = api_history_body_instance.to_dict()
# create an instance of ApiHistoryBody from a dict
api_history_body_from_dict = ApiHistoryBody.from_dict(api_history_body_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


