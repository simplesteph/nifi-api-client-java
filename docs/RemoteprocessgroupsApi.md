# RemoteprocessgroupsApi

All URIs are relative to *http://localhost/nifi-api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getRemoteProcessGroup**](RemoteprocessgroupsApi.md#getRemoteProcessGroup) | **GET** /remote-process-groups/{id} | Gets a remote process group
[**removeRemoteProcessGroup**](RemoteprocessgroupsApi.md#removeRemoteProcessGroup) | **DELETE** /remote-process-groups/{id} | Deletes a remote process group
[**updateRemoteProcessGroup**](RemoteprocessgroupsApi.md#updateRemoteProcessGroup) | **PUT** /remote-process-groups/{id} | Updates a remote process group
[**updateRemoteProcessGroupInputPort**](RemoteprocessgroupsApi.md#updateRemoteProcessGroupInputPort) | **PUT** /remote-process-groups/{id}/input-ports/{port-id} | Updates a remote port
[**updateRemoteProcessGroupOutputPort**](RemoteprocessgroupsApi.md#updateRemoteProcessGroupOutputPort) | **PUT** /remote-process-groups/{id}/output-ports/{port-id} | Updates a remote port


<a name="getRemoteProcessGroup"></a>
# **getRemoteProcessGroup**
> RemoteProcessGroupEntity getRemoteProcessGroup(id)

Gets a remote process group



### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.RemoteprocessgroupsApi;


RemoteprocessgroupsApi apiInstance = new RemoteprocessgroupsApi();
String id = "id_example"; // String | The remote process group id.
try {
    RemoteProcessGroupEntity result = apiInstance.getRemoteProcessGroup(id);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling RemoteprocessgroupsApi#getRemoteProcessGroup");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| The remote process group id. |

### Return type

[**RemoteProcessGroupEntity**](RemoteProcessGroupEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: *_/_*
 - **Accept**: application/json

<a name="removeRemoteProcessGroup"></a>
# **removeRemoteProcessGroup**
> RemoteProcessGroupEntity removeRemoteProcessGroup(id, version, clientId)

Deletes a remote process group



### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.RemoteprocessgroupsApi;


RemoteprocessgroupsApi apiInstance = new RemoteprocessgroupsApi();
String id = "id_example"; // String | The remote process group id.
String version = "version_example"; // String | The revision is used to verify the client is working with the latest version of the flow.
String clientId = "clientId_example"; // String | If the client id is not specified, new one will be generated. This value (whether specified or generated) is included in the response.
try {
    RemoteProcessGroupEntity result = apiInstance.removeRemoteProcessGroup(id, version, clientId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling RemoteprocessgroupsApi#removeRemoteProcessGroup");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| The remote process group id. |
 **version** | **String**| The revision is used to verify the client is working with the latest version of the flow. | [optional]
 **clientId** | **String**| If the client id is not specified, new one will be generated. This value (whether specified or generated) is included in the response. | [optional]

### Return type

[**RemoteProcessGroupEntity**](RemoteProcessGroupEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: *_/_*
 - **Accept**: application/json

<a name="updateRemoteProcessGroup"></a>
# **updateRemoteProcessGroup**
> RemoteProcessGroupEntity updateRemoteProcessGroup(id, body)

Updates a remote process group



### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.RemoteprocessgroupsApi;


RemoteprocessgroupsApi apiInstance = new RemoteprocessgroupsApi();
String id = "id_example"; // String | The remote process group id.
RemoteProcessGroupEntity body = new RemoteProcessGroupEntity(); // RemoteProcessGroupEntity | The remote process group.
try {
    RemoteProcessGroupEntity result = apiInstance.updateRemoteProcessGroup(id, body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling RemoteprocessgroupsApi#updateRemoteProcessGroup");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| The remote process group id. |
 **body** | [**RemoteProcessGroupEntity**](RemoteProcessGroupEntity.md)| The remote process group. |

### Return type

[**RemoteProcessGroupEntity**](RemoteProcessGroupEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="updateRemoteProcessGroupInputPort"></a>
# **updateRemoteProcessGroupInputPort**
> RemoteProcessGroupPortEntity updateRemoteProcessGroupInputPort(id, portId, body)

Updates a remote port

Note: This endpoint is subject to change as NiFi and it&#39;s REST API evolve.

### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.RemoteprocessgroupsApi;


RemoteprocessgroupsApi apiInstance = new RemoteprocessgroupsApi();
String id = "id_example"; // String | The remote process group id.
String portId = "portId_example"; // String | The remote process group port id.
RemoteProcessGroupPortEntity body = new RemoteProcessGroupPortEntity(); // RemoteProcessGroupPortEntity | The remote process group port.
try {
    RemoteProcessGroupPortEntity result = apiInstance.updateRemoteProcessGroupInputPort(id, portId, body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling RemoteprocessgroupsApi#updateRemoteProcessGroupInputPort");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| The remote process group id. |
 **portId** | **String**| The remote process group port id. |
 **body** | [**RemoteProcessGroupPortEntity**](RemoteProcessGroupPortEntity.md)| The remote process group port. |

### Return type

[**RemoteProcessGroupPortEntity**](RemoteProcessGroupPortEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="updateRemoteProcessGroupOutputPort"></a>
# **updateRemoteProcessGroupOutputPort**
> RemoteProcessGroupPortEntity updateRemoteProcessGroupOutputPort(id, portId, body)

Updates a remote port

Note: This endpoint is subject to change as NiFi and it&#39;s REST API evolve.

### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.RemoteprocessgroupsApi;


RemoteprocessgroupsApi apiInstance = new RemoteprocessgroupsApi();
String id = "id_example"; // String | The remote process group id.
String portId = "portId_example"; // String | The remote process group port id.
RemoteProcessGroupPortEntity body = new RemoteProcessGroupPortEntity(); // RemoteProcessGroupPortEntity | The remote process group port.
try {
    RemoteProcessGroupPortEntity result = apiInstance.updateRemoteProcessGroupOutputPort(id, portId, body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling RemoteprocessgroupsApi#updateRemoteProcessGroupOutputPort");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| The remote process group id. |
 **portId** | **String**| The remote process group port id. |
 **body** | [**RemoteProcessGroupPortEntity**](RemoteProcessGroupPortEntity.md)| The remote process group port. |

### Return type

[**RemoteProcessGroupPortEntity**](RemoteProcessGroupPortEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

