# Org.OpenAPITools.Api.ContentApi

All URIs are relative to *http://api.estuary.tech*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ContentAddCarPost**](ContentApi.md#contentaddcarpost) | **POST** /content/add-car | Add Car object
[**ContentAddIpfsPost**](ContentApi.md#contentaddipfspost) | **POST** /content/add-ipfs | Add IPFS object
[**ContentAddPost**](ContentApi.md#contentaddpost) | **POST** /content/add | Add new content
[**ContentAggregatedContentGet**](ContentApi.md#contentaggregatedcontentget) | **GET** /content/aggregated/{content} | Get aggregated content stats
[**ContentAllDealsGet**](ContentApi.md#contentalldealsget) | **GET** /content/all-deals | Get all deals for a user
[**ContentBwUsageContentGet**](ContentApi.md#contentbwusagecontentget) | **GET** /content/bw-usage/{content} | Get content bandwidth
[**ContentCreatePost**](ContentApi.md#contentcreatepost) | **POST** /content/create | Add a new content
[**ContentDealsGet**](ContentApi.md#contentdealsget) | **GET** /content/deals | Content with deals
[**ContentEnsureReplicationDatacidGet**](ContentApi.md#contentensurereplicationdatacidget) | **GET** /content/ensure-replication/{datacid} | Ensure Replication
[**ContentFailuresContentGet**](ContentApi.md#contentfailurescontentget) | **GET** /content/failures/{content} | List all failures for a content
[**ContentImportdealPost**](ContentApi.md#contentimportdealpost) | **POST** /content/importdeal | Import a deal
[**ContentListGet**](ContentApi.md#contentlistget) | **GET** /content/list | List all pinned content
[**ContentReadContGet**](ContentApi.md#contentreadcontget) | **GET** /content/read/{cont} | Read content
[**ContentStagingZonesGet**](ContentApi.md#contentstagingzonesget) | **GET** /content/staging-zones | Get staging zone for user
[**ContentStatsGet**](ContentApi.md#contentstatsget) | **GET** /content/stats | Get content statistics
[**ContentStatusIdGet**](ContentApi.md#contentstatusidget) | **GET** /content/status/{id} | Content Status



## ContentAddCarPost

> string ContentAddCarPost (string body, string filename = null, string commp = null, string size = null)

Add Car object

This endpoint is used to add a car object to the network. The object can be a file or a directory.

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class ContentAddCarPostExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new ContentApi(Configuration.Default);
            var body = "body_example";  // string | Car
            var filename = "filename_example";  // string | Filename (optional) 
            var commp = "commp_example";  // string | Commp (optional) 
            var size = "size_example";  // string | Size (optional) 

            try
            {
                // Add Car object
                string result = apiInstance.ContentAddCarPost(body, filename, commp, size);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling ContentApi.ContentAddCarPost: " + e.Message );
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
 **body** | **string**| Car | 
 **filename** | **string**| Filename | [optional] 
 **commp** | **string**| Commp | [optional] 
 **size** | **string**| Size | [optional] 

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


## ContentAddIpfsPost

> string ContentAddIpfsPost (UtilContentAddIpfsBody body)

Add IPFS object

This endpoint is used to add an IPFS object to the network. The object can be a file or a directory.

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class ContentAddIpfsPostExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new ContentApi(Configuration.Default);
            var body = new UtilContentAddIpfsBody(); // UtilContentAddIpfsBody | IPFS Body

            try
            {
                // Add IPFS object
                string result = apiInstance.ContentAddIpfsPost(body);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling ContentApi.ContentAddIpfsPost: " + e.Message );
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
 **body** | [**UtilContentAddIpfsBody**](UtilContentAddIpfsBody.md)| IPFS Body | 

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


## ContentAddPost

> string ContentAddPost (System.IO.Stream file, string collection = null, string collectionPath = null)

Add new content

This endpoint is used to upload new content.

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class ContentAddPostExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new ContentApi(Configuration.Default);
            var file = new System.IO.MemoryStream(System.IO.File.ReadAllBytes("/path/to/file.txt"));  // System.IO.Stream | File to upload
            var collection = "collection_example";  // string | Collection (optional) 
            var collectionPath = "collectionPath_example";  // string | Collection Path (optional) 

            try
            {
                // Add new content
                string result = apiInstance.ContentAddPost(file, collection, collectionPath);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling ContentApi.ContentAddPost: " + e.Message );
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
 **file** | **System.IO.Stream**| File to upload | 
 **collection** | **string**| Collection | [optional] 
 **collectionPath** | **string**| Collection Path | [optional] 

### Return type

**string**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

[[Back to top]](#)
[[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ContentAggregatedContentGet

> string ContentAggregatedContentGet (string content)

Get aggregated content stats

This endpoint returns aggregated content stats

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class ContentAggregatedContentGetExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new ContentApi(Configuration.Default);
            var content = "content_example";  // string | Content ID

            try
            {
                // Get aggregated content stats
                string result = apiInstance.ContentAggregatedContentGet(content);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling ContentApi.ContentAggregatedContentGet: " + e.Message );
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
 **content** | **string**| Content ID | 

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


## ContentAllDealsGet

> string ContentAllDealsGet (string begin, string duration, string all)

Get all deals for a user

This endpoint is used to get all deals for a user

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class ContentAllDealsGetExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new ContentApi(Configuration.Default);
            var begin = "begin_example";  // string | Begin
            var duration = "duration_example";  // string | Duration
            var all = "all_example";  // string | All

            try
            {
                // Get all deals for a user
                string result = apiInstance.ContentAllDealsGet(begin, duration, all);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling ContentApi.ContentAllDealsGet: " + e.Message );
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
 **begin** | **string**| Begin | 
 **duration** | **string**| Duration | 
 **all** | **string**| All | 

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


## ContentBwUsageContentGet

> string ContentBwUsageContentGet (string content)

Get content bandwidth

This endpoint returns content bandwidth

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class ContentBwUsageContentGetExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new ContentApi(Configuration.Default);
            var content = "content_example";  // string | Content ID

            try
            {
                // Get content bandwidth
                string result = apiInstance.ContentBwUsageContentGet(content);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling ContentApi.ContentBwUsageContentGet: " + e.Message );
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
 **content** | **string**| Content ID | 

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


## ContentCreatePost

> string ContentCreatePost (string body)

Add a new content

This endpoint adds a new content

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class ContentCreatePostExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new ContentApi(Configuration.Default);
            var body = "body_example";  // string | Content

            try
            {
                // Add a new content
                string result = apiInstance.ContentCreatePost(body);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling ContentApi.ContentCreatePost: " + e.Message );
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
 **body** | **string**| Content | 

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


## ContentDealsGet

> string ContentDealsGet (int? limit = null, int? offset = null)

Content with deals

This endpoint lists all content with deals

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class ContentDealsGetExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new ContentApi(Configuration.Default);
            var limit = 56;  // int? | Limit (optional) 
            var offset = 56;  // int? | Offset (optional) 

            try
            {
                // Content with deals
                string result = apiInstance.ContentDealsGet(limit, offset);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling ContentApi.ContentDealsGet: " + e.Message );
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
 **limit** | **int?**| Limit | [optional] 
 **offset** | **int?**| Offset | [optional] 

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


## ContentEnsureReplicationDatacidGet

> string ContentEnsureReplicationDatacidGet (string datacid)

Ensure Replication

This endpoint ensures that the content is replicated to the specified number of providers

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class ContentEnsureReplicationDatacidGetExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new ContentApi(Configuration.Default);
            var datacid = "datacid_example";  // string | Data CID

            try
            {
                // Ensure Replication
                string result = apiInstance.ContentEnsureReplicationDatacidGet(datacid);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling ContentApi.ContentEnsureReplicationDatacidGet: " + e.Message );
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
 **datacid** | **string**| Data CID | 

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


## ContentFailuresContentGet

> string ContentFailuresContentGet (string content)

List all failures for a content

This endpoint returns all failures for a content

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class ContentFailuresContentGetExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new ContentApi(Configuration.Default);
            var content = "content_example";  // string | Content ID

            try
            {
                // List all failures for a content
                string result = apiInstance.ContentFailuresContentGet(content);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling ContentApi.ContentFailuresContentGet: " + e.Message );
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
 **content** | **string**| Content ID | 

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


## ContentImportdealPost

> string ContentImportdealPost (MainImportDealBody body)

Import a deal

This endpoint imports a deal into the shuttle.

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class ContentImportdealPostExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new ContentApi(Configuration.Default);
            var body = new MainImportDealBody(); // MainImportDealBody | Import a deal

            try
            {
                // Import a deal
                string result = apiInstance.ContentImportdealPost(body);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling ContentApi.ContentImportdealPost: " + e.Message );
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
 **body** | [**MainImportDealBody**](MainImportDealBody.md)| Import a deal | 

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


## ContentListGet

> List&lt;string&gt; ContentListGet ()

List all pinned content

This endpoint lists all content

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class ContentListGetExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new ContentApi(Configuration.Default);

            try
            {
                // List all pinned content
                List<string> result = apiInstance.ContentListGet();
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling ContentApi.ContentListGet: " + e.Message );
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

**List<string>**

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


## ContentReadContGet

> string ContentReadContGet (string cont)

Read content

This endpoint reads content from the blockstore

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class ContentReadContGetExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new ContentApi(Configuration.Default);
            var cont = "cont_example";  // string | CID

            try
            {
                // Read content
                string result = apiInstance.ContentReadContGet(cont);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling ContentApi.ContentReadContGet: " + e.Message );
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
 **cont** | **string**| CID | 

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


## ContentStagingZonesGet

> string ContentStagingZonesGet ()

Get staging zone for user

This endpoint is used to get staging zone for user.

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class ContentStagingZonesGetExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new ContentApi(Configuration.Default);

            try
            {
                // Get staging zone for user
                string result = apiInstance.ContentStagingZonesGet();
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling ContentApi.ContentStagingZonesGet: " + e.Message );
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


## ContentStatsGet

> string ContentStatsGet (string limit)

Get content statistics

This endpoint is used to get content statistics. Every content stored in the network (estuary) is tracked by a unique ID which can be used to get information about the content. This endpoint will allow the consumer to get the collected stats of a conten

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class ContentStatsGetExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new ContentApi(Configuration.Default);
            var limit = "limit_example";  // string | limit

            try
            {
                // Get content statistics
                string result = apiInstance.ContentStatsGet(limit);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling ContentApi.ContentStatsGet: " + e.Message );
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
 **limit** | **string**| limit | 

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


## ContentStatusIdGet

> string ContentStatusIdGet (int id)

Content Status

This endpoint returns the status of a content

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class ContentStatusIdGetExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new ContentApi(Configuration.Default);
            var id = 56;  // int | Content ID

            try
            {
                // Content Status
                string result = apiInstance.ContentStatusIdGet(id);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling ContentApi.ContentStatusIdGet: " + e.Message );
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
 **id** | **int**| Content ID | 

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

