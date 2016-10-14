# TemplatesApi

All URIs are relative to *http://localhost/nifi-api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**exportTemplate**](TemplatesApi.md#exportTemplate) | **GET** /templates/{id}/download | Exports a template
[**removeTemplate**](TemplatesApi.md#removeTemplate) | **DELETE** /templates/{id} | Deletes a template


<a name="exportTemplate"></a>
# **exportTemplate**
> TemplateDTO exportTemplate(id)

Exports a template



### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.TemplatesApi;


TemplatesApi apiInstance = new TemplatesApi();
String id = "id_example"; // String | The template id.
try {
    TemplateDTO result = apiInstance.exportTemplate(id);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling TemplatesApi#exportTemplate");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| The template id. |

### Return type

[**TemplateDTO**](TemplateDTO.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: *_/_*
 - **Accept**: application/xml

<a name="removeTemplate"></a>
# **removeTemplate**
> TemplateEntity removeTemplate(id)

Deletes a template



### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.TemplatesApi;


TemplatesApi apiInstance = new TemplatesApi();
String id = "id_example"; // String | The template id.
try {
    TemplateEntity result = apiInstance.removeTemplate(id);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling TemplatesApi#removeTemplate");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| The template id. |

### Return type

[**TemplateEntity**](TemplateEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: *_/_*
 - **Accept**: application/json

