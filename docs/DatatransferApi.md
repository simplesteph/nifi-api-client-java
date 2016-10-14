# DatatransferApi

All URIs are relative to *http://localhost/nifi-api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**commitInputPortTransaction**](DatatransferApi.md#commitInputPortTransaction) | **DELETE** /data-transfer/input-ports/{portId}/transactions/{transactionId} | Commit or cancel the specified transaction
[**commitOutputPortTransaction**](DatatransferApi.md#commitOutputPortTransaction) | **DELETE** /data-transfer/output-ports/{portId}/transactions/{transactionId} | Commit or cancel the specified transaction
[**createPortTransaction**](DatatransferApi.md#createPortTransaction) | **POST** /data-transfer/{portType}/{portId}/transactions | Create a transaction to the specified output port or input port
[**extendInputPortTransactionTTL**](DatatransferApi.md#extendInputPortTransactionTTL) | **PUT** /data-transfer/input-ports/{portId}/transactions/{transactionId} | Extend transaction TTL
[**extendOutputPortTransactionTTL**](DatatransferApi.md#extendOutputPortTransactionTTL) | **PUT** /data-transfer/output-ports/{portId}/transactions/{transactionId} | Extend transaction TTL
[**receiveFlowFiles**](DatatransferApi.md#receiveFlowFiles) | **POST** /data-transfer/input-ports/{portId}/transactions/{transactionId}/flow-files | Transfer flow files to the input port
[**transferFlowFiles**](DatatransferApi.md#transferFlowFiles) | **GET** /data-transfer/output-ports/{portId}/transactions/{transactionId}/flow-files | Transfer flow files from the output port


<a name="commitInputPortTransaction"></a>
# **commitInputPortTransaction**
> TransactionResultEntity commitInputPortTransaction(responseCode, portId, transactionId)

Commit or cancel the specified transaction



### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.DatatransferApi;


DatatransferApi apiInstance = new DatatransferApi();
Integer responseCode = 56; // Integer | The response code. Available values are BAD_CHECKSUM(19), CONFIRM_TRANSACTION(12) or CANCEL_TRANSACTION(15).
String portId = "portId_example"; // String | The input port id.
String transactionId = "transactionId_example"; // String | The transaction id.
try {
    TransactionResultEntity result = apiInstance.commitInputPortTransaction(responseCode, portId, transactionId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DatatransferApi#commitInputPortTransaction");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **responseCode** | **Integer**| The response code. Available values are BAD_CHECKSUM(19), CONFIRM_TRANSACTION(12) or CANCEL_TRANSACTION(15). |
 **portId** | **String**| The input port id. |
 **transactionId** | **String**| The transaction id. |

### Return type

[**TransactionResultEntity**](TransactionResultEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/octet-stream
 - **Accept**: application/json

<a name="commitOutputPortTransaction"></a>
# **commitOutputPortTransaction**
> TransactionResultEntity commitOutputPortTransaction(responseCode, checksum, portId, transactionId)

Commit or cancel the specified transaction



### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.DatatransferApi;


DatatransferApi apiInstance = new DatatransferApi();
Integer responseCode = 56; // Integer | The response code. Available values are CONFIRM_TRANSACTION(12) or CANCEL_TRANSACTION(15).
String checksum = "checksum_example"; // String | A checksum calculated at client side using CRC32 to check flow file content integrity. It must match with the value calculated at server side.
String portId = "portId_example"; // String | The output port id.
String transactionId = "transactionId_example"; // String | The transaction id.
try {
    TransactionResultEntity result = apiInstance.commitOutputPortTransaction(responseCode, checksum, portId, transactionId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DatatransferApi#commitOutputPortTransaction");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **responseCode** | **Integer**| The response code. Available values are CONFIRM_TRANSACTION(12) or CANCEL_TRANSACTION(15). |
 **checksum** | **String**| A checksum calculated at client side using CRC32 to check flow file content integrity. It must match with the value calculated at server side. |
 **portId** | **String**| The output port id. |
 **transactionId** | **String**| The transaction id. |

### Return type

[**TransactionResultEntity**](TransactionResultEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/octet-stream
 - **Accept**: application/json

<a name="createPortTransaction"></a>
# **createPortTransaction**
> TransactionResultEntity createPortTransaction(portType, portId)

Create a transaction to the specified output port or input port



### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.DatatransferApi;


DatatransferApi apiInstance = new DatatransferApi();
String portType = "portType_example"; // String | The port type.
String portId = "portId_example"; // String | 
try {
    TransactionResultEntity result = apiInstance.createPortTransaction(portType, portId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DatatransferApi#createPortTransaction");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **portType** | **String**| The port type. | [enum: input-ports, output-ports]
 **portId** | **String**|  |

### Return type

[**TransactionResultEntity**](TransactionResultEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="extendInputPortTransactionTTL"></a>
# **extendInputPortTransactionTTL**
> TransactionResultEntity extendInputPortTransactionTTL(portId, transactionId)

Extend transaction TTL



### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.DatatransferApi;


DatatransferApi apiInstance = new DatatransferApi();
String portId = "portId_example"; // String | 
String transactionId = "transactionId_example"; // String | 
try {
    TransactionResultEntity result = apiInstance.extendInputPortTransactionTTL(portId, transactionId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DatatransferApi#extendInputPortTransactionTTL");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **portId** | **String**|  |
 **transactionId** | **String**|  |

### Return type

[**TransactionResultEntity**](TransactionResultEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: *_/_*
 - **Accept**: application/json

<a name="extendOutputPortTransactionTTL"></a>
# **extendOutputPortTransactionTTL**
> TransactionResultEntity extendOutputPortTransactionTTL(portId, transactionId)

Extend transaction TTL



### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.DatatransferApi;


DatatransferApi apiInstance = new DatatransferApi();
String portId = "portId_example"; // String | 
String transactionId = "transactionId_example"; // String | 
try {
    TransactionResultEntity result = apiInstance.extendOutputPortTransactionTTL(portId, transactionId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DatatransferApi#extendOutputPortTransactionTTL");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **portId** | **String**|  |
 **transactionId** | **String**|  |

### Return type

[**TransactionResultEntity**](TransactionResultEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: *_/_*
 - **Accept**: application/json

<a name="receiveFlowFiles"></a>
# **receiveFlowFiles**
> String receiveFlowFiles(portId, transactionId)

Transfer flow files to the input port



### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.DatatransferApi;


DatatransferApi apiInstance = new DatatransferApi();
String portId = "portId_example"; // String | The input port id.
String transactionId = "transactionId_example"; // String | 
try {
    String result = apiInstance.receiveFlowFiles(portId, transactionId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DatatransferApi#receiveFlowFiles");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **portId** | **String**| The input port id. |
 **transactionId** | **String**|  |

### Return type

**String**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/octet-stream
 - **Accept**: text/plain

<a name="transferFlowFiles"></a>
# **transferFlowFiles**
> StreamingOutput transferFlowFiles(portId, transactionId)

Transfer flow files from the output port



### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.DatatransferApi;


DatatransferApi apiInstance = new DatatransferApi();
String portId = "portId_example"; // String | The output port id.
String transactionId = "transactionId_example"; // String | 
try {
    StreamingOutput result = apiInstance.transferFlowFiles(portId, transactionId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DatatransferApi#transferFlowFiles");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **portId** | **String**| The output port id. |
 **transactionId** | **String**|  |

### Return type

[**StreamingOutput**](StreamingOutput.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: *_/_*
 - **Accept**: application/octet-stream

