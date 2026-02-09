# ApiPairingResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**session** | **int** | Pairing session ID | 
**layout_name** | **str** | UI layout name for the paired device | 
**actual_node_type** | **str** | Actual node type detected during pairing | [optional] 
**node_id** | **int** | ID of the newly paired node | [optional] 

## Example

```python
from openapi_client.models.api_pairing_response import ApiPairingResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ApiPairingResponse from a JSON string
api_pairing_response_instance = ApiPairingResponse.from_json(json)
# print the JSON string representation of the object
print(ApiPairingResponse.to_json())

# convert the object into a dict
api_pairing_response_dict = api_pairing_response_instance.to_dict()
# create an instance of ApiPairingResponse from a dict
api_pairing_response_from_dict = ApiPairingResponse.from_dict(api_pairing_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


