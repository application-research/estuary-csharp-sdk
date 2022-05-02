# Org.OpenAPITools.Api.PinningApi

All URIs are relative to *http://api.estuary.tech*

Method | HTTP request | Description
------------- | ------------- | -------------
[**PinningPinsGet**](PinningApi.md#pinningpinsget) | **GET** /pinning/pins | List all pinned objects
[**PinningPinsPost**](PinningApi.md#pinningpinspost) | **POST** /pinning/pins | Add and pin object
[**PinningPinsRequestidDelete**](PinningApi.md#pinningpinsrequestiddelete) | **DELETE** /pinning/pins/{requestid} | Delete a pinned object
[**PinningPinsRequestidGet**](PinningApi.md#pinningpinsrequestidget) | **GET** /pinning/pins/{requestid} | Get a pinned objects
[**PinningPinsRequestidPost**](PinningApi.md#pinningpinsrequestidpost) | **POST** /pinning/pins/{requestid} | Replace a pinned object



## PinningPinsGet

> void PinningPinsGet ()

List all pinned objects

This endpoint lists all pinned objects

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class PinningPinsGetExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new PinningApi(Configuration.Default);

            try
            {
                // List all pinned objects
                apiInstance.PinningPinsGet();
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling PinningApi.PinningPinsGet: " + e.Message );
                Debug.Print("Status Code: "+ e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **400** | Bad Request |  -  |
| **404** | Not Found |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#)
[[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PinningPinsPost

> string PinningPinsPost (string cid, string name)

Add and pin object

This endpoint adds a pin to the IPFS daemon.

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class PinningPinsPostExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new PinningApi(Configuration.Default);
            var cid = "cid_example";  // string | cid
            var name = "name_example";  // string | name

            try
            {
                // Add and pin object
                string result = apiInstance.PinningPinsPost(cid, name);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling PinningApi.PinningPinsPost: " + e.Message );
                Debug.Print("Status Code: "+ e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cid** | **string**| cid | 
 **name** | **string**| name | 

### Return type

**string**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

[[Back to top]](#)
[[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PinningPinsRequestidDelete

> string PinningPinsRequestidDelete (string requestid)

Delete a pinned object

This endpoint deletes a pinned object.

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class PinningPinsRequestidDeleteExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new PinningApi(Configuration.Default);
            var requestid = "requestid_example";  // string | requestid

            try
            {
                // Delete a pinned object
                string result = apiInstance.PinningPinsRequestidDelete(requestid);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling PinningApi.PinningPinsRequestidDelete: " + e.Message );
                Debug.Print("Status Code: "+ e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestid** | **string**| requestid | 

### Return type

**string**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

[[Back to top]](#)
[[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PinningPinsRequestidGet

> string PinningPinsRequestidGet (string requestid)

Get a pinned objects

This endpoint returns a pinned object.

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class PinningPinsRequestidGetExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new PinningApi(Configuration.Default);
            var requestid = "requestid_example";  // string | cid

            try
            {
                // Get a pinned objects
                string result = apiInstance.PinningPinsRequestidGet(requestid);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling PinningApi.PinningPinsRequestidGet: " + e.Message );
                Debug.Print("Status Code: "+ e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestid** | **string**| cid | 

### Return type

**string**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

[[Back to top]](#)
[[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PinningPinsRequestidPost

> string PinningPinsRequestidPost (string requestid)

Replace a pinned object

This endpoint replaces a pinned object.

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class PinningPinsRequestidPostExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new PinningApi(Configuration.Default);
            var requestid = "requestid_example";  // string | id

            try
            {
                // Replace a pinned object
                string result = apiInstance.PinningPinsRequestidPost(requestid);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling PinningApi.PinningPinsRequestidPost: " + e.Message );
                Debug.Print("Status Code: "+ e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestid** | **string**| id | 

### Return type

**string**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

[[Back to top]](#)
[[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

