# HistoryItem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Unique history event ID | 
**node_id** | **int** | ID of the node that triggered the event | 
**timestamp** | **int** | Unix timestamp of the event | [optional] 
**value** | **str** | Event type/value (e.g., \&quot;door_open\&quot;, \&quot;motion_detected\&quot;) | 
**is_trigger** | **bool** | Whether this event triggered another action | [optional] 
**trigger_source** | **int** | Node ID that triggered this event (if applicable) | [optional] 
**opening_type** | **str** | Type of opening (for door/window sensors) | [optional] 
**room** | **str** | Custom room name | [optional] 
**area** | **str** | Area key/identifier | [optional] 
**user_name** | **str** | Username associated with the event | [optional] 
**kpd_code_label** | **str** | Keypad code label (for keypad events) | [optional] 

## Example

```python
from openapi_client.models.history_item import HistoryItem

# TODO update the JSON string below
json = "{}"
# create an instance of HistoryItem from a JSON string
history_item_instance = HistoryItem.from_json(json)
# print the JSON string representation of the object
print(HistoryItem.to_json())

# convert the object into a dict
history_item_dict = history_item_instance.to_dict()
# create an instance of HistoryItem from a dict
history_item_from_dict = HistoryItem.from_dict(history_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


