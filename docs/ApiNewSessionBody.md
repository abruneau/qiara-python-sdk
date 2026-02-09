# ApiNewSessionBody


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cust_id** | **int** | Customer ID | 
**challenge_rsp** | **str** | Challenge response computed using HMAC-SHA256 | 

## Example

```python
from openapi_client.models.api_new_session_body import ApiNewSessionBody

# TODO update the JSON string below
json = "{}"
# create an instance of ApiNewSessionBody from a JSON string
api_new_session_body_instance = ApiNewSessionBody.from_json(json)
# print the JSON string representation of the object
print(ApiNewSessionBody.to_json())

# convert the object into a dict
api_new_session_body_dict = api_new_session_body_instance.to_dict()
# create an instance of ApiNewSessionBody from a dict
api_new_session_body_from_dict = ApiNewSessionBody.from_dict(api_new_session_body_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


