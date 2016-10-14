# ProvenanceeventsApi

All URIs are relative to *http://localhost/nifi-api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getInputContent**](ProvenanceeventsApi.md#getInputContent) | **GET** /provenance-events/{id}/content/input | Gets the input content for a provenance event
[**getOutputContent**](ProvenanceeventsApi.md#getOutputContent) | **GET** /provenance-events/{id}/content/output | Gets the output content for a provenance event
[**getProvenanceEvent**](ProvenanceeventsApi.md#getProvenanceEvent) | **GET** /provenance-events/{id} | Gets a provenance event
[**submitReplay**](ProvenanceeventsApi.md#submitReplay) | **POST** /provenance-events/replays | Replays content from a provenance event


<a name="getInputContent"></a>
# **getInputContent**
> getInputContent(id, clusterNodeId)

Gets the input content for a provenance event



### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.ProvenanceeventsApi;


ProvenanceeventsApi apiInstance = new ProvenanceeventsApi();
String id = "id_example"; // String | The provenance event id.
String clusterNodeId = "clusterNodeId_example"; // String | The id of the node where the content exists if clustered.
try {
    apiInstance.getInputContent(id, clusterNodeId);
} catch (ApiException e) {
    System.err.println("Exception when calling ProvenanceeventsApi#getInputContent");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| The provenance event id. |
 **clusterNodeId** | **String**| The id of the node where the content exists if clustered. | [optional]

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: *_/_*
 - **Accept**: *_/_*

<a name="getOutputContent"></a>
# **getOutputContent**
> getOutputContent(id, clusterNodeId)

Gets the output content for a provenance event



### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.ProvenanceeventsApi;


ProvenanceeventsApi apiInstance = new ProvenanceeventsApi();
String id = "id_example"; // String | The provenance event id.
String clusterNodeId = "clusterNodeId_example"; // String | The id of the node where the content exists if clustered.
try {
    apiInstance.getOutputContent(id, clusterNodeId);
} catch (ApiException e) {
    System.err.println("Exception when calling ProvenanceeventsApi#getOutputContent");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| The provenance event id. |
 **clusterNodeId** | **String**| The id of the node where the content exists if clustered. | [optional]

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: *_/_*
 - **Accept**: *_/_*

<a name="getProvenanceEvent"></a>
# **getProvenanceEvent**
> ProvenanceEventEntity getProvenanceEvent(id, clusterNodeId)

Gets a provenance event



### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.ProvenanceeventsApi;


ProvenanceeventsApi apiInstance = new ProvenanceeventsApi();
String id = "id_example"; // String | The provenance event id.
String clusterNodeId = "clusterNodeId_example"; // String | The id of the node where this event exists if clustered.
try {
    ProvenanceEventEntity result = apiInstance.getProvenanceEvent(id, clusterNodeId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ProvenanceeventsApi#getProvenanceEvent");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| The provenance event id. |
 **clusterNodeId** | **String**| The id of the node where this event exists if clustered. | [optional]

### Return type

[**ProvenanceEventEntity**](ProvenanceEventEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: *_/_*
 - **Accept**: application/json

<a name="submitReplay"></a>
# **submitReplay**
> ProvenanceEventEntity submitReplay(body)

Replays content from a provenance event



### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.ProvenanceeventsApi;


ProvenanceeventsApi apiInstance = new ProvenanceeventsApi();
SubmitReplayRequestEntity body = new SubmitReplayRequestEntity(); // SubmitReplayRequestEntity | The replay request.
try {
    ProvenanceEventEntity result = apiInstance.submitReplay(body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ProvenanceeventsApi#submitReplay");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**SubmitReplayRequestEntity**](SubmitReplayRequestEntity.md)| The replay request. |

### Return type

[**ProvenanceEventEntity**](ProvenanceEventEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

