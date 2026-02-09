# openapi_client.DefaultApi

All URIs are relative to *https://api.qiara.co/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**control_video_recorder**](DefaultApi.md#control_video_recorder) | **POST** /home/recorder_action | Control video recorder
[**create_session**](DefaultApi.md#create_session) | **POST** /login/new | Create new session
[**delete_history**](DefaultApi.md#delete_history) | **POST** /home/delete_history | Delete history items
[**delete_nodes**](DefaultApi.md#delete_nodes) | **POST** /home/delete | Delete nodes
[**delete_video_recordings**](DefaultApi.md#delete_video_recordings) | **POST** /home/remove_records/720p | Delete video recordings
[**get_challenge**](DefaultApi.md#get_challenge) | **GET** /login/challenge | Get authentication challenge
[**get_history**](DefaultApi.md#get_history) | **POST** /home/history | Get event history
[**get_nodes**](DefaultApi.md#get_nodes) | **POST** /home/nodes | Get home nodes
[**get_revision_update**](DefaultApi.md#get_revision_update) | **GET** /home/revision | Get revision update
[**get_stream_snapshot**](DefaultApi.md#get_stream_snapshot) | **GET** /home/stream/live.jpeg | Get live stream snapshot
[**get_video_recordings**](DefaultApi.md#get_video_recordings) | **GET** /home/recording/720p | Get video recordings
[**manage_home_pairing**](DefaultApi.md#manage_home_pairing) | **POST** /home/pairing | Manage device pairing
[**open_video_stream**](DefaultApi.md#open_video_stream) | **POST** /home/open_stream | Open video stream
[**read_endpoints**](DefaultApi.md#read_endpoints) | **POST** /home/endpoints_read | Read endpoint values
[**update_firmware**](DefaultApi.md#update_firmware) | **POST** /home/fw_update | Update firmware
[**update_revision**](DefaultApi.md#update_revision) | **POST** /home/revision | Update revision
[**write_endpoints**](DefaultApi.md#write_endpoints) | **POST** /home/endpoints_write | Write endpoint values


# **control_video_recorder**
> object control_video_recorder(x_hlcore_session_id, body)

Control video recorder

Perform an action on the video recorder (start/stop recording)

### Example

* Api Key Authentication (SessionAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.qiara.co/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://api.qiara.co/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: SessionAuth
configuration.api_key['SessionAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['SessionAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DefaultApi(api_client)
    x_hlcore_session_id = 'sess_1a2b3c4d5e6f' # str | Session ID obtained from the /login/new endpoint after successful authentication
    body = None # object | 

    try:
        # Control video recorder
        api_response = api_instance.control_video_recorder(x_hlcore_session_id, body)
        print("The response of DefaultApi->control_video_recorder:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->control_video_recorder: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_hlcore_session_id** | **str**| Session ID obtained from the /login/new endpoint after successful authentication | 
 **body** | **object**|  | 

### Return type

**object**

### Authorization

[SessionAuth](../README.md#SessionAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Recorder action executed successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_session**
> ApiNewSessionResponse create_session(api_new_session_body)

Create new session

Create a new authenticated session using challenge response

### Example


```python
import openapi_client
from openapi_client.models.api_new_session_body import ApiNewSessionBody
from openapi_client.models.api_new_session_response import ApiNewSessionResponse
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.qiara.co/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://api.qiara.co/api/v1"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DefaultApi(api_client)
    api_new_session_body = openapi_client.ApiNewSessionBody() # ApiNewSessionBody | 

    try:
        # Create new session
        api_response = api_instance.create_session(api_new_session_body)
        print("The response of DefaultApi->create_session:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->create_session: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_new_session_body** | [**ApiNewSessionBody**](ApiNewSessionBody.md)|  | 

### Return type

[**ApiNewSessionResponse**](ApiNewSessionResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Session created successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_history**
> delete_history(x_hlcore_session_id, body)

Delete history items

Delete specified history items

### Example

* Api Key Authentication (SessionAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.qiara.co/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://api.qiara.co/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: SessionAuth
configuration.api_key['SessionAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['SessionAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DefaultApi(api_client)
    x_hlcore_session_id = 'sess_1a2b3c4d5e6f' # str | Session ID obtained from the /login/new endpoint after successful authentication
    body = None # object | 

    try:
        # Delete history items
        api_instance.delete_history(x_hlcore_session_id, body)
    except Exception as e:
        print("Exception when calling DefaultApi->delete_history: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_hlcore_session_id** | **str**| Session ID obtained from the /login/new endpoint after successful authentication | 
 **body** | **object**|  | 

### Return type

void (empty response body)

### Authorization

[SessionAuth](../README.md#SessionAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | History items deleted successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_nodes**
> delete_nodes(x_hlcore_session_id, body)

Delete nodes

Delete specified nodes from the system

### Example

* Api Key Authentication (SessionAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.qiara.co/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://api.qiara.co/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: SessionAuth
configuration.api_key['SessionAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['SessionAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DefaultApi(api_client)
    x_hlcore_session_id = 'sess_1a2b3c4d5e6f' # str | Session ID obtained from the /login/new endpoint after successful authentication
    body = None # object | 

    try:
        # Delete nodes
        api_instance.delete_nodes(x_hlcore_session_id, body)
    except Exception as e:
        print("Exception when calling DefaultApi->delete_nodes: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_hlcore_session_id** | **str**| Session ID obtained from the /login/new endpoint after successful authentication | 
 **body** | **object**|  | 

### Return type

void (empty response body)

### Authorization

[SessionAuth](../README.md#SessionAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Nodes deleted successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_video_recordings**
> object delete_video_recordings(x_hlcore_session_id, body)

Delete video recordings

Delete specified 720p video recordings

### Example

* Api Key Authentication (SessionAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.qiara.co/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://api.qiara.co/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: SessionAuth
configuration.api_key['SessionAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['SessionAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DefaultApi(api_client)
    x_hlcore_session_id = 'sess_1a2b3c4d5e6f' # str | Session ID obtained from the /login/new endpoint after successful authentication
    body = None # object | 

    try:
        # Delete video recordings
        api_response = api_instance.delete_video_recordings(x_hlcore_session_id, body)
        print("The response of DefaultApi->delete_video_recordings:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->delete_video_recordings: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_hlcore_session_id** | **str**| Session ID obtained from the /login/new endpoint after successful authentication | 
 **body** | **object**|  | 

### Return type

**object**

### Authorization

[SessionAuth](../README.md#SessionAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Video recordings deleted successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_challenge**
> ApiChallenge get_challenge()

Get authentication challenge

Retrieve a challenge string for authentication

### Example


```python
import openapi_client
from openapi_client.models.api_challenge import ApiChallenge
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.qiara.co/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://api.qiara.co/api/v1"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DefaultApi(api_client)

    try:
        # Get authentication challenge
        api_response = api_instance.get_challenge()
        print("The response of DefaultApi->get_challenge:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->get_challenge: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**ApiChallenge**](ApiChallenge.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Challenge retrieved successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_history**
> ApiHistoryResponse get_history(x_hlcore_session_id, api_history_body)

Get event history

Retrieve event history with pagination

### Example

* Api Key Authentication (SessionAuth):

```python
import openapi_client
from openapi_client.models.api_history_body import ApiHistoryBody
from openapi_client.models.api_history_response import ApiHistoryResponse
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.qiara.co/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://api.qiara.co/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: SessionAuth
configuration.api_key['SessionAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['SessionAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DefaultApi(api_client)
    x_hlcore_session_id = 'sess_1a2b3c4d5e6f' # str | Session ID obtained from the /login/new endpoint after successful authentication
    api_history_body = openapi_client.ApiHistoryBody() # ApiHistoryBody | 

    try:
        # Get event history
        api_response = api_instance.get_history(x_hlcore_session_id, api_history_body)
        print("The response of DefaultApi->get_history:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->get_history: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_hlcore_session_id** | **str**| Session ID obtained from the /login/new endpoint after successful authentication | 
 **api_history_body** | [**ApiHistoryBody**](ApiHistoryBody.md)|  | 

### Return type

[**ApiHistoryResponse**](ApiHistoryResponse.md)

### Authorization

[SessionAuth](../README.md#SessionAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | History retrieved successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_nodes**
> ApiNodesResponse get_nodes(x_hlcore_session_id)

Get home nodes

Retrieve list of all nodes (devices) in the home system

### Example

* Api Key Authentication (SessionAuth):

```python
import openapi_client
from openapi_client.models.api_nodes_response import ApiNodesResponse
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.qiara.co/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://api.qiara.co/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: SessionAuth
configuration.api_key['SessionAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['SessionAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DefaultApi(api_client)
    x_hlcore_session_id = 'sess_1a2b3c4d5e6f' # str | Session ID obtained from the /login/new endpoint after successful authentication

    try:
        # Get home nodes
        api_response = api_instance.get_nodes(x_hlcore_session_id)
        print("The response of DefaultApi->get_nodes:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->get_nodes: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_hlcore_session_id** | **str**| Session ID obtained from the /login/new endpoint after successful authentication | 

### Return type

[**ApiNodesResponse**](ApiNodesResponse.md)

### Authorization

[SessionAuth](../README.md#SessionAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of nodes retrieved successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_revision_update**
> object get_revision_update()

Get revision update

Check for system revision updates

### Example

* Api Key Authentication (SessionAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.qiara.co/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://api.qiara.co/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: SessionAuth
configuration.api_key['SessionAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['SessionAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DefaultApi(api_client)

    try:
        # Get revision update
        api_response = api_instance.get_revision_update()
        print("The response of DefaultApi->get_revision_update:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->get_revision_update: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

**object**

### Authorization

[SessionAuth](../README.md#SessionAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Revision update information |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_stream_snapshot**
> bytearray get_stream_snapshot(x_hlcore_session_id)

Get live stream snapshot

Retrieve a JPEG snapshot from the live video stream

### Example

* Api Key Authentication (SessionAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.qiara.co/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://api.qiara.co/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: SessionAuth
configuration.api_key['SessionAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['SessionAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DefaultApi(api_client)
    x_hlcore_session_id = 'sess_1a2b3c4d5e6f' # str | Session ID obtained from the /login/new endpoint after successful authentication

    try:
        # Get live stream snapshot
        api_response = api_instance.get_stream_snapshot(x_hlcore_session_id)
        print("The response of DefaultApi->get_stream_snapshot:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->get_stream_snapshot: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_hlcore_session_id** | **str**| Session ID obtained from the /login/new endpoint after successful authentication | 

### Return type

**bytearray**

### Authorization

[SessionAuth](../README.md#SessionAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/jpeg

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Snapshot retrieved successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_video_recordings**
> object get_video_recordings(x_hlcore_session_id)

Get video recordings

Retrieve list of 720p video recordings

### Example

* Api Key Authentication (SessionAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.qiara.co/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://api.qiara.co/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: SessionAuth
configuration.api_key['SessionAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['SessionAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DefaultApi(api_client)
    x_hlcore_session_id = 'sess_1a2b3c4d5e6f' # str | Session ID obtained from the /login/new endpoint after successful authentication

    try:
        # Get video recordings
        api_response = api_instance.get_video_recordings(x_hlcore_session_id)
        print("The response of DefaultApi->get_video_recordings:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->get_video_recordings: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_hlcore_session_id** | **str**| Session ID obtained from the /login/new endpoint after successful authentication | 

### Return type

**object**

### Authorization

[SessionAuth](../README.md#SessionAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of video recordings |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **manage_home_pairing**
> ApiPairingResponse manage_home_pairing(x_hlcore_session_id, manage_home_pairing_request)

Manage device pairing

Start, update, or stop device pairing process

### Example

* Api Key Authentication (SessionAuth):

```python
import openapi_client
from openapi_client.models.api_pairing_response import ApiPairingResponse
from openapi_client.models.manage_home_pairing_request import ManageHomePairingRequest
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.qiara.co/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://api.qiara.co/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: SessionAuth
configuration.api_key['SessionAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['SessionAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DefaultApi(api_client)
    x_hlcore_session_id = 'sess_1a2b3c4d5e6f' # str | Session ID obtained from the /login/new endpoint after successful authentication
    manage_home_pairing_request = openapi_client.ManageHomePairingRequest() # ManageHomePairingRequest | 

    try:
        # Manage device pairing
        api_response = api_instance.manage_home_pairing(x_hlcore_session_id, manage_home_pairing_request)
        print("The response of DefaultApi->manage_home_pairing:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->manage_home_pairing: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_hlcore_session_id** | **str**| Session ID obtained from the /login/new endpoint after successful authentication | 
 **manage_home_pairing_request** | [**ManageHomePairingRequest**](ManageHomePairingRequest.md)|  | 

### Return type

[**ApiPairingResponse**](ApiPairingResponse.md)

### Authorization

[SessionAuth](../README.md#SessionAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Pairing operation successful |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **open_video_stream**
> object open_video_stream(x_hlcore_session_id, api_video_stream_body)

Open video stream

Open a live video stream

### Example

* Api Key Authentication (SessionAuth):

```python
import openapi_client
from openapi_client.models.api_video_stream_body import ApiVideoStreamBody
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.qiara.co/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://api.qiara.co/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: SessionAuth
configuration.api_key['SessionAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['SessionAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DefaultApi(api_client)
    x_hlcore_session_id = 'sess_1a2b3c4d5e6f' # str | Session ID obtained from the /login/new endpoint after successful authentication
    api_video_stream_body = openapi_client.ApiVideoStreamBody() # ApiVideoStreamBody | 

    try:
        # Open video stream
        api_response = api_instance.open_video_stream(x_hlcore_session_id, api_video_stream_body)
        print("The response of DefaultApi->open_video_stream:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->open_video_stream: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_hlcore_session_id** | **str**| Session ID obtained from the /login/new endpoint after successful authentication | 
 **api_video_stream_body** | [**ApiVideoStreamBody**](ApiVideoStreamBody.md)|  | 

### Return type

**object**

### Authorization

[SessionAuth](../README.md#SessionAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Video stream opened successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_endpoints**
> ReadEndpoints200Response read_endpoints(x_hlcore_session_id, read_endpoints_request)

Read endpoint values

Read configuration values from specified endpoints

### Example

* Api Key Authentication (SessionAuth):

```python
import openapi_client
from openapi_client.models.read_endpoints200_response import ReadEndpoints200Response
from openapi_client.models.read_endpoints_request import ReadEndpointsRequest
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.qiara.co/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://api.qiara.co/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: SessionAuth
configuration.api_key['SessionAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['SessionAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DefaultApi(api_client)
    x_hlcore_session_id = 'sess_1a2b3c4d5e6f' # str | Session ID obtained from the /login/new endpoint after successful authentication
    read_endpoints_request = openapi_client.ReadEndpointsRequest() # ReadEndpointsRequest | 

    try:
        # Read endpoint values
        api_response = api_instance.read_endpoints(x_hlcore_session_id, read_endpoints_request)
        print("The response of DefaultApi->read_endpoints:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->read_endpoints: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_hlcore_session_id** | **str**| Session ID obtained from the /login/new endpoint after successful authentication | 
 **read_endpoints_request** | [**ReadEndpointsRequest**](ReadEndpointsRequest.md)|  | 

### Return type

[**ReadEndpoints200Response**](ReadEndpoints200Response.md)

### Authorization

[SessionAuth](../README.md#SessionAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Endpoint values retrieved successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_firmware**
> update_firmware(x_hlcore_session_id)

Update firmware

Initiate firmware update for devices

### Example

* Api Key Authentication (SessionAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.qiara.co/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://api.qiara.co/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: SessionAuth
configuration.api_key['SessionAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['SessionAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DefaultApi(api_client)
    x_hlcore_session_id = 'sess_1a2b3c4d5e6f' # str | Session ID obtained from the /login/new endpoint after successful authentication

    try:
        # Update firmware
        api_instance.update_firmware(x_hlcore_session_id)
    except Exception as e:
        print("Exception when calling DefaultApi->update_firmware: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_hlcore_session_id** | **str**| Session ID obtained from the /login/new endpoint after successful authentication | 

### Return type

void (empty response body)

### Authorization

[SessionAuth](../README.md#SessionAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Firmware update initiated successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_revision**
> object update_revision(x_hlcore_session_id, body)

Update revision

Submit revision update request

### Example

* Api Key Authentication (SessionAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.qiara.co/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://api.qiara.co/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: SessionAuth
configuration.api_key['SessionAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['SessionAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DefaultApi(api_client)
    x_hlcore_session_id = 'sess_1a2b3c4d5e6f' # str | Session ID obtained from the /login/new endpoint after successful authentication
    body = None # object | 

    try:
        # Update revision
        api_response = api_instance.update_revision(x_hlcore_session_id, body)
        print("The response of DefaultApi->update_revision:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->update_revision: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_hlcore_session_id** | **str**| Session ID obtained from the /login/new endpoint after successful authentication | 
 **body** | **object**|  | 

### Return type

**object**

### Authorization

[SessionAuth](../README.md#SessionAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Revision updated successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **write_endpoints**
> object write_endpoints(x_hlcore_session_id, write_endpoints_request)

Write endpoint values

Write configuration values to specified endpoints

### Example

* Api Key Authentication (SessionAuth):

```python
import openapi_client
from openapi_client.models.write_endpoints_request import WriteEndpointsRequest
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.qiara.co/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://api.qiara.co/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: SessionAuth
configuration.api_key['SessionAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['SessionAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DefaultApi(api_client)
    x_hlcore_session_id = 'sess_1a2b3c4d5e6f' # str | Session ID obtained from the /login/new endpoint after successful authentication
    write_endpoints_request = openapi_client.WriteEndpointsRequest() # WriteEndpointsRequest | 

    try:
        # Write endpoint values
        api_response = api_instance.write_endpoints(x_hlcore_session_id, write_endpoints_request)
        print("The response of DefaultApi->write_endpoints:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->write_endpoints: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_hlcore_session_id** | **str**| Session ID obtained from the /login/new endpoint after successful authentication | 
 **write_endpoints_request** | [**WriteEndpointsRequest**](WriteEndpointsRequest.md)|  | 

### Return type

**object**

### Authorization

[SessionAuth](../README.md#SessionAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Endpoint values written successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

