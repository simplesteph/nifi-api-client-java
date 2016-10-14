# CountersApi

All URIs are relative to *http://localhost/nifi-api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getCounters**](CountersApi.md#getCounters) | **GET** /counters | Gets the current counters for this NiFi
[**updateCounter**](CountersApi.md#updateCounter) | **PUT** /counters/{id} | Updates the specified counter. This will reset the counter value to 0


<a name="getCounters"></a>
# **getCounters**
> CountersEntity getCounters(nodewise, clusterNodeId)

Gets the current counters for this NiFi

Note: This endpoint is subject to change as NiFi and it&#39;s REST API evolve.

### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.CountersApi;


CountersApi apiInstance = new CountersApi();
Boolean nodewise = true; // Boolean | Whether or not to include the breakdown per node. Optional, defaults to false
String clusterNodeId = "clusterNodeId_example"; // String | The id of the node where to get the status.
try {
    CountersEntity result = apiInstance.getCounters(nodewise, clusterNodeId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling CountersApi#getCounters");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **nodewise** | **Boolean**| Whether or not to include the breakdown per node. Optional, defaults to false | [optional]
 **clusterNodeId** | **String**| The id of the node where to get the status. | [optional]

### Return type

[**CountersEntity**](CountersEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: *_/_*
 - **Accept**: application/json

<a name="updateCounter"></a>
# **updateCounter**
> CounterEntity updateCounter(id)

Updates the specified counter. This will reset the counter value to 0

Note: This endpoint is subject to change as NiFi and it&#39;s REST API evolve.

### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.CountersApi;


CountersApi apiInstance = new CountersApi();
String id = "id_example"; // String | 
try {
    CounterEntity result = apiInstance.updateCounter(id);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling CountersApi#updateCounter");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**|  |

### Return type

[**CounterEntity**](CounterEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: *_/_*
 - **Accept**: application/json

