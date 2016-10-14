# ControllerservicesApi

All URIs are relative to *http://localhost/nifi-api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**clearState**](ControllerservicesApi.md#clearState) | **POST** /controller-services/{id}/state/clear-requests | Clears the state for a controller service
[**getControllerService**](ControllerservicesApi.md#getControllerService) | **GET** /controller-services/{id} | Gets a controller service
[**getControllerServiceReferences**](ControllerservicesApi.md#getControllerServiceReferences) | **GET** /controller-services/{id}/references | Gets a controller service
[**getPropertyDescriptor**](ControllerservicesApi.md#getPropertyDescriptor) | **GET** /controller-services/{id}/descriptors | Gets a controller service property descriptor
[**getState**](ControllerservicesApi.md#getState) | **GET** /controller-services/{id}/state | Gets the state for a controller service
[**removeControllerService**](ControllerservicesApi.md#removeControllerService) | **DELETE** /controller-services/{id} | Deletes a controller service
[**updateControllerService**](ControllerservicesApi.md#updateControllerService) | **PUT** /controller-services/{id} | Updates a controller service
[**updateControllerServiceReferences**](ControllerservicesApi.md#updateControllerServiceReferences) | **PUT** /controller-services/{id}/references | Updates a controller services references


<a name="clearState"></a>
# **clearState**
> ComponentStateDTO clearState(id)

Clears the state for a controller service



### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.ControllerservicesApi;


ControllerservicesApi apiInstance = new ControllerservicesApi();
String id = "id_example"; // String | The controller service id.
try {
    ComponentStateDTO result = apiInstance.clearState(id);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ControllerservicesApi#clearState");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| The controller service id. |

### Return type

[**ComponentStateDTO**](ComponentStateDTO.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: *_/_*
 - **Accept**: application/json

<a name="getControllerService"></a>
# **getControllerService**
> ControllerServiceEntity getControllerService(id)

Gets a controller service



### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.ControllerservicesApi;


ControllerservicesApi apiInstance = new ControllerservicesApi();
String id = "id_example"; // String | The controller service id.
try {
    ControllerServiceEntity result = apiInstance.getControllerService(id);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ControllerservicesApi#getControllerService");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| The controller service id. |

### Return type

[**ControllerServiceEntity**](ControllerServiceEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: *_/_*
 - **Accept**: application/json

<a name="getControllerServiceReferences"></a>
# **getControllerServiceReferences**
> ControllerServiceEntity getControllerServiceReferences(id)

Gets a controller service



### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.ControllerservicesApi;


ControllerservicesApi apiInstance = new ControllerservicesApi();
String id = "id_example"; // String | The controller service id.
try {
    ControllerServiceEntity result = apiInstance.getControllerServiceReferences(id);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ControllerservicesApi#getControllerServiceReferences");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| The controller service id. |

### Return type

[**ControllerServiceEntity**](ControllerServiceEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: *_/_*
 - **Accept**: application/json

<a name="getPropertyDescriptor"></a>
# **getPropertyDescriptor**
> PropertyDescriptorEntity getPropertyDescriptor(id, propertyName)

Gets a controller service property descriptor



### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.ControllerservicesApi;


ControllerservicesApi apiInstance = new ControllerservicesApi();
String id = "id_example"; // String | The controller service id.
String propertyName = "propertyName_example"; // String | The property name to return the descriptor for.
try {
    PropertyDescriptorEntity result = apiInstance.getPropertyDescriptor(id, propertyName);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ControllerservicesApi#getPropertyDescriptor");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| The controller service id. |
 **propertyName** | **String**| The property name to return the descriptor for. |

### Return type

[**PropertyDescriptorEntity**](PropertyDescriptorEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: *_/_*
 - **Accept**: application/json

<a name="getState"></a>
# **getState**
> ComponentStateDTO getState(id)

Gets the state for a controller service



### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.ControllerservicesApi;


ControllerservicesApi apiInstance = new ControllerservicesApi();
String id = "id_example"; // String | The controller service id.
try {
    ComponentStateDTO result = apiInstance.getState(id);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ControllerservicesApi#getState");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| The controller service id. |

### Return type

[**ComponentStateDTO**](ComponentStateDTO.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: *_/_*
 - **Accept**: application/json

<a name="removeControllerService"></a>
# **removeControllerService**
> ControllerServiceEntity removeControllerService(id, version, clientId)

Deletes a controller service



### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.ControllerservicesApi;


ControllerservicesApi apiInstance = new ControllerservicesApi();
String id = "id_example"; // String | The controller service id.
String version = "version_example"; // String | The revision is used to verify the client is working with the latest version of the flow.
String clientId = "clientId_example"; // String | If the client id is not specified, new one will be generated. This value (whether specified or generated) is included in the response.
try {
    ControllerServiceEntity result = apiInstance.removeControllerService(id, version, clientId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ControllerservicesApi#removeControllerService");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| The controller service id. |
 **version** | **String**| The revision is used to verify the client is working with the latest version of the flow. | [optional]
 **clientId** | **String**| If the client id is not specified, new one will be generated. This value (whether specified or generated) is included in the response. | [optional]

### Return type

[**ControllerServiceEntity**](ControllerServiceEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: *_/_*
 - **Accept**: application/json

<a name="updateControllerService"></a>
# **updateControllerService**
> ControllerServiceEntity updateControllerService(id, body)

Updates a controller service



### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.ControllerservicesApi;


ControllerservicesApi apiInstance = new ControllerservicesApi();
String id = "id_example"; // String | The controller service id.
ControllerServiceEntity body = new ControllerServiceEntity(); // ControllerServiceEntity | The controller service configuration details.
try {
    ControllerServiceEntity result = apiInstance.updateControllerService(id, body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ControllerservicesApi#updateControllerService");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| The controller service id. |
 **body** | [**ControllerServiceEntity**](ControllerServiceEntity.md)| The controller service configuration details. |

### Return type

[**ControllerServiceEntity**](ControllerServiceEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="updateControllerServiceReferences"></a>
# **updateControllerServiceReferences**
> ControllerServiceReferencingComponentsEntity updateControllerServiceReferences(id, body)

Updates a controller services references



### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.ControllerservicesApi;


ControllerservicesApi apiInstance = new ControllerservicesApi();
String id = "id_example"; // String | The controller service id.
UpdateControllerServiceReferenceRequestEntity body = new UpdateControllerServiceReferenceRequestEntity(); // UpdateControllerServiceReferenceRequestEntity | The controller service request update request.
try {
    ControllerServiceReferencingComponentsEntity result = apiInstance.updateControllerServiceReferences(id, body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ControllerservicesApi#updateControllerServiceReferences");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| The controller service id. |
 **body** | [**UpdateControllerServiceReferenceRequestEntity**](UpdateControllerServiceReferenceRequestEntity.md)| The controller service request update request. |

### Return type

[**ControllerServiceReferencingComponentsEntity**](ControllerServiceReferencingComponentsEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

