# SitetositeApi

All URIs are relative to *http://localhost/nifi-api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getPeers**](SitetositeApi.md#getPeers) | **GET** /site-to-site/peers | Returns the available Peers and its status of this NiFi
[**getSiteToSiteDetails**](SitetositeApi.md#getSiteToSiteDetails) | **GET** /site-to-site | Returns the details about this NiFi necessary to communicate via site to site


<a name="getPeers"></a>
# **getPeers**
> PeersEntity getPeers()

Returns the available Peers and its status of this NiFi



### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.SitetositeApi;


SitetositeApi apiInstance = new SitetositeApi();
try {
    PeersEntity result = apiInstance.getPeers();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling SitetositeApi#getPeers");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**PeersEntity**](PeersEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: *_/_*
 - **Accept**: application/json, application/xml

<a name="getSiteToSiteDetails"></a>
# **getSiteToSiteDetails**
> ControllerEntity getSiteToSiteDetails()

Returns the details about this NiFi necessary to communicate via site to site



### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.SitetositeApi;


SitetositeApi apiInstance = new SitetositeApi();
try {
    ControllerEntity result = apiInstance.getSiteToSiteDetails();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling SitetositeApi#getSiteToSiteDetails");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ControllerEntity**](ControllerEntity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: *_/_*
 - **Accept**: application/json

