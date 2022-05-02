# Org.OpenAPITools.Api.DealsApi

All URIs are relative to *http://api.estuary.tech*

Method | HTTP request | Description
------------- | ------------- | -------------
[**DealsEstimatePost**](DealsApi.md#dealsestimatepost) | **POST** /deals/estimate | Estimate the cost of a deal
[**DealsFailuresGet**](DealsApi.md#dealsfailuresget) | **GET** /deals/failures | Get storage failures
[**DealsInfoDealidGet**](DealsApi.md#dealsinfodealidget) | **GET** /deals/info/{dealid} | Get Deal Info
[**DealsMakeMinerPost**](DealsApi.md#dealsmakeminerpost) | **POST** /deals/make/{miner} | Make Deal
[**DealsProposalPropcidGet**](DealsApi.md#dealsproposalpropcidget) | **GET** /deals/proposal/{propcid} | Get Proposal
[**DealsQueryMinerGet**](DealsApi.md#dealsqueryminerget) | **GET** /deals/query/{miner} | Query Ask
[**DealsStatusByProposalPropcidGet**](DealsApi.md#dealsstatusbyproposalpropcidget) | **GET** /deals/status-by-proposal/{propcid} | Get Deal Status by PropCid
[**DealsStatusDealGet**](DealsApi.md#dealsstatusdealget) | **GET** /deals/status/{deal} | Get Deal Status
[**DealsStatusMinerPropcidGet**](DealsApi.md#dealsstatusminerpropcidget) | **GET** /deals/status/{miner}/{propcid} | Deal Status
[**DealsTransferInProgressGet**](DealsApi.md#dealstransferinprogressget) | **GET** /deals/transfer/in-progress | Transfer In Progress
[**DealsTransferStatusPost**](DealsApi.md#dealstransferstatuspost) | **POST** /deals/transfer/status | Transfer Status



## DealsEstimatePost

> string DealsEstimatePost (MainEstimateDealBody body)

Estimate the cost of a deal

This endpoint estimates the cost of a deal

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class DealsEstimatePostExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new DealsApi(Configuration.Default);
            var body = new MainEstimateDealBody(); // MainEstimateDealBody | The size of the deal in bytes, the replication factor, and the duration of the deal in blocks

            try
            {
                // Estimate the cost of a deal
                string result = apiInstance.DealsEstimatePost(body);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling DealsApi.DealsEstimatePost: " + e.Message );
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
 **body** | [**MainEstimateDealBody**](MainEstimateDealBody.md)| The size of the deal in bytes, the replication factor, and the duration of the deal in blocks | 

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


## DealsFailuresGet

> string DealsFailuresGet ()

Get storage failures

This endpoint returns a list of storage failures

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class DealsFailuresGetExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new DealsApi(Configuration.Default);

            try
            {
                // Get storage failures
                string result = apiInstance.DealsFailuresGet();
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling DealsApi.DealsFailuresGet: " + e.Message );
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


## DealsInfoDealidGet

> string DealsInfoDealidGet (int dealid)

Get Deal Info

This endpoint returns the deal info for a deal

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class DealsInfoDealidGetExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new DealsApi(Configuration.Default);
            var dealid = 56;  // int | Deal ID

            try
            {
                // Get Deal Info
                string result = apiInstance.DealsInfoDealidGet(dealid);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling DealsApi.DealsInfoDealidGet: " + e.Message );
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
 **dealid** | **int**| Deal ID | 

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


## DealsMakeMinerPost

> string DealsMakeMinerPost (string miner, string dealRequest)

Make Deal

This endpoint makes a deal for a given content and miner

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class DealsMakeMinerPostExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new DealsApi(Configuration.Default);
            var miner = "miner_example";  // string | Miner
            var dealRequest = "dealRequest_example";  // string | Deal Request

            try
            {
                // Make Deal
                string result = apiInstance.DealsMakeMinerPost(miner, dealRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling DealsApi.DealsMakeMinerPost: " + e.Message );
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
 **miner** | **string**| Miner | 
 **dealRequest** | **string**| Deal Request | 

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


## DealsProposalPropcidGet

> string DealsProposalPropcidGet (string propcid)

Get Proposal

This endpoint returns the proposal for a deal

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class DealsProposalPropcidGetExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new DealsApi(Configuration.Default);
            var propcid = "propcid_example";  // string | Proposal CID

            try
            {
                // Get Proposal
                string result = apiInstance.DealsProposalPropcidGet(propcid);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling DealsApi.DealsProposalPropcidGet: " + e.Message );
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
 **propcid** | **string**| Proposal CID | 

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


## DealsQueryMinerGet

> string DealsQueryMinerGet (string miner)

Query Ask

This endpoint returns the ask for a given CID

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class DealsQueryMinerGetExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new DealsApi(Configuration.Default);
            var miner = "miner_example";  // string | CID

            try
            {
                // Query Ask
                string result = apiInstance.DealsQueryMinerGet(miner);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling DealsApi.DealsQueryMinerGet: " + e.Message );
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
 **miner** | **string**| CID | 

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


## DealsStatusByProposalPropcidGet

> string DealsStatusByProposalPropcidGet (string propcid)

Get Deal Status by PropCid

Get Deal Status by PropCid

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class DealsStatusByProposalPropcidGetExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new DealsApi(Configuration.Default);
            var propcid = "propcid_example";  // string | PropCid

            try
            {
                // Get Deal Status by PropCid
                string result = apiInstance.DealsStatusByProposalPropcidGet(propcid);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling DealsApi.DealsStatusByProposalPropcidGet: " + e.Message );
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
 **propcid** | **string**| PropCid | 

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


## DealsStatusDealGet

> string DealsStatusDealGet (int deal)

Get Deal Status

This endpoint returns the status of a deal

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class DealsStatusDealGetExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new DealsApi(Configuration.Default);
            var deal = 56;  // int | Deal ID

            try
            {
                // Get Deal Status
                string result = apiInstance.DealsStatusDealGet(deal);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling DealsApi.DealsStatusDealGet: " + e.Message );
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
 **deal** | **int**| Deal ID | 

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


## DealsStatusMinerPropcidGet

> string DealsStatusMinerPropcidGet (string miner, string propcid)

Deal Status

This endpoint returns the status of a deal

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class DealsStatusMinerPropcidGetExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new DealsApi(Configuration.Default);
            var miner = "miner_example";  // string | Miner
            var propcid = "propcid_example";  // string | Proposal CID

            try
            {
                // Deal Status
                string result = apiInstance.DealsStatusMinerPropcidGet(miner, propcid);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling DealsApi.DealsStatusMinerPropcidGet: " + e.Message );
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
 **miner** | **string**| Miner | 
 **propcid** | **string**| Proposal CID | 

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


## DealsTransferInProgressGet

> string DealsTransferInProgressGet ()

Transfer In Progress

This endpoint returns the in-progress transfers

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class DealsTransferInProgressGetExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new DealsApi(Configuration.Default);

            try
            {
                // Transfer In Progress
                string result = apiInstance.DealsTransferInProgressGet();
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling DealsApi.DealsTransferInProgressGet: " + e.Message );
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


## DealsTransferStatusPost

> string DealsTransferStatusPost ()

Transfer Status

This endpoint returns the status of a transfer

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class DealsTransferStatusPostExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new DealsApi(Configuration.Default);

            try
            {
                // Transfer Status
                string result = apiInstance.DealsTransferStatusPost();
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling DealsApi.DealsTransferStatusPost: " + e.Message );
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

