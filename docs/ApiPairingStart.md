# ApiPairingStart


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**node_type** | **str** | Type of node to pair. Maps to device types in the Qiara home security system. - HOMELABCAM: Camera (MainCamera or SlaveCamera) - HOMELABSRN: Siren - HOMELABDWS: Door/Window Sensor - HOMELABPIR: PIR Motion Sensor   - HOMELABKPD: Keypad  | 
**op** | **str** | Operation type for pairing process. - start_adapter: Start adapter and begin pairing - stop: Stop pairing process - poll: Poll for pairing status - next: Move to next step in pairing  | [default to 'start_adapter']
**adapter_type** | **str** | Adapter type for the pairing process. Default is Adapter.DomusAdapter which is used for the Qiara/Domus home security system devices.  | [default to 'Adapter.DomusAdapter']

## Example

```python
from openapi_client.models.api_pairing_start import ApiPairingStart

# TODO update the JSON string below
json = "{}"
# create an instance of ApiPairingStart from a JSON string
api_pairing_start_instance = ApiPairingStart.from_json(json)
# print the JSON string representation of the object
print(ApiPairingStart.to_json())

# convert the object into a dict
api_pairing_start_dict = api_pairing_start_instance.to_dict()
# create an instance of ApiPairingStart from a dict
api_pairing_start_from_dict = ApiPairingStart.from_dict(api_pairing_start_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


