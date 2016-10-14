# ResourcesApi

All URIs are relative to *http://localhost/nifi-api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getResources**](ResourcesApi.md#getResources) | **GET** /resources | Gets the available resources that support access/authorization policies


<a name="getResources"></a>
# **getResources**
> ResourcesEntity getResources()

Gets the available resources that support access/authorization policies



### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.ResourcesApi;


ResourcesApi apiInstance = new ResourcesApi();
try {
    ResourcesEntity result = apiInstance.getResources();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ResourcesApi#getResources");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ResourcesEntity**](ResourcesEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: *_/_*
 - **Accept**: application/json

