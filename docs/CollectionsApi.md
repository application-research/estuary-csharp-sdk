# Org.OpenAPITools.Api.CollectionsApi

All URIs are relative to *http://api.estuary.tech*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CollectionsAddContentPost**](CollectionsApi.md#collectionsaddcontentpost) | **POST** /collections/add-content | Add contents to a collection
[**CollectionsContentColuuidGet**](CollectionsApi.md#collectionscontentcoluuidget) | **GET** /collections/content/{coluuid} | Get contents in a collection
[**CollectionsCreatePost**](CollectionsApi.md#collectionscreatepost) | **POST** /collections/create | Create a new collection
[**CollectionsFsAddPost**](CollectionsApi.md#collectionsfsaddpost) | **POST** /collections/fs/add | Add a file to a collection
[**CollectionsFsListGet**](CollectionsApi.md#collectionsfslistget) | **GET** /collections/fs/list | Create a new collection
[**CollectionsListGet**](CollectionsApi.md#collectionslistget) | **GET** /collections/list | List all collections



## CollectionsAddContentPost

> Dictionary&lt;string, string&gt; CollectionsAddContentPost (MainAddContentToCollectionParams body)

Add contents to a collection

When a collection is created, users with valid API keys can add contents to the collection. This endpoint can be used to add contents to a collection.

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class CollectionsAddContentPostExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new CollectionsApi(Configuration.Default);
            var body = new MainAddContentToCollectionParams(); // MainAddContentToCollectionParams | Contents to add to collection

            try
            {
                // Add contents to a collection
                Dictionary<string, string> result = apiInstance.CollectionsAddContentPost(body);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling CollectionsApi.CollectionsAddContentPost: " + e.Message );
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
 **body** | [**MainAddContentToCollectionParams**](MainAddContentToCollectionParams.md)| Contents to add to collection | 

### Return type

**Dictionary<string, string>**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

[[Back to top]](#)
[[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CollectionsContentColuuidGet

> string CollectionsContentColuuidGet (string coluuid)

Get contents in a collection

This endpoint is used to get contents in a collection. When a collection is created, this collection object is retrievable along with its content via this endpoint.

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class CollectionsContentColuuidGetExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new CollectionsApi(Configuration.Default);
            var coluuid = "coluuid_example";  // string | coluuid

            try
            {
                // Get contents in a collection
                string result = apiInstance.CollectionsContentColuuidGet(coluuid);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling CollectionsApi.CollectionsContentColuuidGet: " + e.Message );
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
 **coluuid** | **string**| coluuid | 

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


## CollectionsCreatePost

> MainCollection CollectionsCreatePost (MainCreateCollectionBody body)

Create a new collection

This endpoint is used to create a new collection. A collection is a representaion of a group of objects added on the estuary. This endpoint can be used to create a new collection.

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class CollectionsCreatePostExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new CollectionsApi(Configuration.Default);
            var body = new MainCreateCollectionBody(); // MainCreateCollectionBody | Collection name and description

            try
            {
                // Create a new collection
                MainCollection result = apiInstance.CollectionsCreatePost(body);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling CollectionsApi.CollectionsCreatePost: " + e.Message );
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
 **body** | [**MainCreateCollectionBody**](MainCreateCollectionBody.md)| Collection name and description | 

### Return type

[**MainCollection**](MainCollection.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad Request |  -  |
| **404** | Not Found |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#)
[[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CollectionsFsAddPost

> string CollectionsFsAddPost (string col, string collection, string content, string path)

Add a file to a collection

This endpoint adds a file to a collection

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class CollectionsFsAddPostExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new CollectionsApi(Configuration.Default);
            var col = "col_example";  // string | Collection ID
            var collection = "collection_example";  // string | Collection ID Long
            var content = "content_example";  // string | Content
            var path = "path_example";  // string | Path to file

            try
            {
                // Add a file to a collection
                string result = apiInstance.CollectionsFsAddPost(col, collection, content, path);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling CollectionsApi.CollectionsFsAddPost: " + e.Message );
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
 **col** | **string**| Collection ID | 
 **collection** | **string**| Collection ID Long | 
 **content** | **string**| Content | 
 **path** | **string**| Path to file | 

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


## CollectionsFsListGet

> string CollectionsFsListGet (string col, string dir)

Create a new collection

This endpoint creates a new collection

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class CollectionsFsListGetExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new CollectionsApi(Configuration.Default);
            var col = "col_example";  // string | Collection
            var dir = "dir_example";  // string | Directory

            try
            {
                // Create a new collection
                string result = apiInstance.CollectionsFsListGet(col, dir);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling CollectionsApi.CollectionsFsListGet: " + e.Message );
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
 **col** | **string**| Collection | 
 **dir** | **string**| Directory | 

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


## CollectionsListGet

> List&lt;MainCollection&gt; CollectionsListGet ()

List all collections

This endpoint is used to list all collections. Whenever a user logs on estuary, it will list all collections that the user has access to. This endpoint provides a way to list all collections to the user.

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class CollectionsListGetExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new CollectionsApi(Configuration.Default);

            try
            {
                // List all collections
                List<MainCollection> result = apiInstance.CollectionsListGet();
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling CollectionsApi.CollectionsListGet: " + e.Message );
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

[**List&lt;MainCollection&gt;**](MainCollection.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **400** | Bad Request |  -  |
| **404** | Not Found |  -  |
| **500** | Internal Server Error |  -  |

[[Back to top]](#)
[[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

