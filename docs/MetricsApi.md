# Org.OpenAPITools.Api.MetricsApi

All URIs are relative to *http://api.estuary.tech*

Method | HTTP request | Description
------------- | ------------- | -------------
[**PublicMetricsDealsOnChainGet**](MetricsApi.md#publicmetricsdealsonchainget) | **GET** /public/metrics/deals-on-chain | Get deal metrics



## PublicMetricsDealsOnChainGet

> string PublicMetricsDealsOnChainGet ()

Get deal metrics

This endpoint is used to get deal metrics

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class PublicMetricsDealsOnChainGetExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new MetricsApi(Configuration.Default);

            try
            {
                // Get deal metrics
                string result = apiInstance.PublicMetricsDealsOnChainGet();
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling MetricsApi.PublicMetricsDealsOnChainGet: " + e.Message );
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

