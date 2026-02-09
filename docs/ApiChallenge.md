# ApiChallenge


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**challenge** | **str** | Random challenge string for authentication | 

## Example

```python
from openapi_client.models.api_challenge import ApiChallenge

# TODO update the JSON string below
json = "{}"
# create an instance of ApiChallenge from a JSON string
api_challenge_instance = ApiChallenge.from_json(json)
# print the JSON string representation of the object
print(ApiChallenge.to_json())

# convert the object into a dict
api_challenge_dict = api_challenge_instance.to_dict()
# create an instance of ApiChallenge from a dict
api_challenge_from_dict = ApiChallenge.from_dict(api_challenge_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


