:no_entry: [DEPRECATED] Active at https://github.com/application-research/estuary-clients

# Org.OpenAPITools - the C# library for the Estuary API

This is the API for the Estuary application.

This C# SDK is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: 1.0.0
- SDK version: 1.0.0
- Build package: org.openapitools.codegen.languages.CSharpClientCodegen
    For more information, please visit [https://docs.estuary.tech/feedback](https://docs.estuary.tech/feedback)

## Frameworks supported


- .NET 4.0 or later
- Windows Phone 7.1 (Mango)

## Dependencies


- [RestSharp](https://www.nuget.org/packages/RestSharp) - 105.1.0 or later
- [Json.NET](https://www.nuget.org/packages/Newtonsoft.Json/) - 7.0.0 or later
- [JsonSubTypes](https://www.nuget.org/packages/JsonSubTypes/) - 1.2.0 or later

The DLLs included in the package may not be the latest version. We recommend using [NuGet](https://docs.nuget.org/consume/installing-nuget) to obtain the latest version of the packages:

```
Install-Package RestSharp
Install-Package Newtonsoft.Json
Install-Package JsonSubTypes
```

NOTE: RestSharp versions greater than 105.1.0 have a bug which causes file uploads to fail. See [RestSharp#742](https://github.com/restsharp/RestSharp/issues/742)

## Installation

Run the following command to generate the DLL

- [Mac/Linux] `/bin/sh build.sh`
- [Windows] `build.bat`

Then include the DLL (under the `bin` folder) in the C# project, and use the namespaces:

```csharp
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

```


## Packaging

A `.nuspec` is included with the project. You can follow the Nuget quickstart to [create](https://docs.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package#create-the-package) and [publish](https://docs.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package#publish-the-package) packages.

This `.nuspec` uses placeholders from the `.csproj`, so build the `.csproj` directly:

```
nuget pack -Build -OutputDirectory out Org.OpenAPITools.csproj
```

Then, publish to a [local feed](https://docs.microsoft.com/en-us/nuget/hosting-packages/local-feeds) or [other host](https://docs.microsoft.com/en-us/nuget/hosting-packages/overview) and consume the new package via Nuget as usual.


## Getting Started

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Org.OpenAPITools.Api;
using Org.OpenAPITools.Client;
using Org.OpenAPITools.Model;

namespace Example
{
    public class Example
    {
        public static void Main()
        {

            Configuration.Default.BasePath = "http://api.estuary.tech";
            // Configure API key authorization: bearerAuth
            Configuration.Default.ApiKey.Add("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.ApiKeyPrefix.Add("Authorization", "Bearer");

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

## Documentation for API Endpoints

All URIs are relative to *http://api.estuary.tech*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*CollectionsApi* | [**CollectionsAddContentPost**](docs/CollectionsApi.md#collectionsaddcontentpost) | **POST** /collections/add-content | Add contents to a collection
*CollectionsApi* | [**CollectionsContentColuuidGet**](docs/CollectionsApi.md#collectionscontentcoluuidget) | **GET** /collections/content/{coluuid} | Get contents in a collection
*CollectionsApi* | [**CollectionsCreatePost**](docs/CollectionsApi.md#collectionscreatepost) | **POST** /collections/create | Create a new collection
*CollectionsApi* | [**CollectionsFsAddPost**](docs/CollectionsApi.md#collectionsfsaddpost) | **POST** /collections/fs/add | Add a file to a collection
*CollectionsApi* | [**CollectionsFsListGet**](docs/CollectionsApi.md#collectionsfslistget) | **GET** /collections/fs/list | Create a new collection
*CollectionsApi* | [**CollectionsListGet**](docs/CollectionsApi.md#collectionslistget) | **GET** /collections/list | List all collections
*ContentApi* | [**ContentAddCarPost**](docs/ContentApi.md#contentaddcarpost) | **POST** /content/add-car | Add Car object
*ContentApi* | [**ContentAddIpfsPost**](docs/ContentApi.md#contentaddipfspost) | **POST** /content/add-ipfs | Add IPFS object
*ContentApi* | [**ContentAddPost**](docs/ContentApi.md#contentaddpost) | **POST** /content/add | Add new content
*ContentApi* | [**ContentAggregatedContentGet**](docs/ContentApi.md#contentaggregatedcontentget) | **GET** /content/aggregated/{content} | Get aggregated content stats
*ContentApi* | [**ContentAllDealsGet**](docs/ContentApi.md#contentalldealsget) | **GET** /content/all-deals | Get all deals for a user
*ContentApi* | [**ContentBwUsageContentGet**](docs/ContentApi.md#contentbwusagecontentget) | **GET** /content/bw-usage/{content} | Get content bandwidth
*ContentApi* | [**ContentCreatePost**](docs/ContentApi.md#contentcreatepost) | **POST** /content/create | Add a new content
*ContentApi* | [**ContentDealsGet**](docs/ContentApi.md#contentdealsget) | **GET** /content/deals | Content with deals
*ContentApi* | [**ContentEnsureReplicationDatacidGet**](docs/ContentApi.md#contentensurereplicationdatacidget) | **GET** /content/ensure-replication/{datacid} | Ensure Replication
*ContentApi* | [**ContentFailuresContentGet**](docs/ContentApi.md#contentfailurescontentget) | **GET** /content/failures/{content} | List all failures for a content
*ContentApi* | [**ContentImportdealPost**](docs/ContentApi.md#contentimportdealpost) | **POST** /content/importdeal | Import a deal
*ContentApi* | [**ContentListGet**](docs/ContentApi.md#contentlistget) | **GET** /content/list | List all pinned content
*ContentApi* | [**ContentReadContGet**](docs/ContentApi.md#contentreadcontget) | **GET** /content/read/{cont} | Read content
*ContentApi* | [**ContentStagingZonesGet**](docs/ContentApi.md#contentstagingzonesget) | **GET** /content/staging-zones | Get staging zone for user
*ContentApi* | [**ContentStatsGet**](docs/ContentApi.md#contentstatsget) | **GET** /content/stats | Get content statistics
*ContentApi* | [**ContentStatusIdGet**](docs/ContentApi.md#contentstatusidget) | **GET** /content/status/{id} | Content Status
*DealsApi* | [**DealsEstimatePost**](docs/DealsApi.md#dealsestimatepost) | **POST** /deals/estimate | Estimate the cost of a deal
*DealsApi* | [**DealsFailuresGet**](docs/DealsApi.md#dealsfailuresget) | **GET** /deals/failures | Get storage failures
*DealsApi* | [**DealsInfoDealidGet**](docs/DealsApi.md#dealsinfodealidget) | **GET** /deals/info/{dealid} | Get Deal Info
*DealsApi* | [**DealsMakeMinerPost**](docs/DealsApi.md#dealsmakeminerpost) | **POST** /deals/make/{miner} | Make Deal
*DealsApi* | [**DealsProposalPropcidGet**](docs/DealsApi.md#dealsproposalpropcidget) | **GET** /deals/proposal/{propcid} | Get Proposal
*DealsApi* | [**DealsQueryMinerGet**](docs/DealsApi.md#dealsqueryminerget) | **GET** /deals/query/{miner} | Query Ask
*DealsApi* | [**DealsStatusByProposalPropcidGet**](docs/DealsApi.md#dealsstatusbyproposalpropcidget) | **GET** /deals/status-by-proposal/{propcid} | Get Deal Status by PropCid
*DealsApi* | [**DealsStatusDealGet**](docs/DealsApi.md#dealsstatusdealget) | **GET** /deals/status/{deal} | Get Deal Status
*DealsApi* | [**DealsStatusMinerPropcidGet**](docs/DealsApi.md#dealsstatusminerpropcidget) | **GET** /deals/status/{miner}/{propcid} | Deal Status
*DealsApi* | [**DealsTransferInProgressGet**](docs/DealsApi.md#dealstransferinprogressget) | **GET** /deals/transfer/in-progress | Transfer In Progress
*DealsApi* | [**DealsTransferStatusPost**](docs/DealsApi.md#dealstransferstatuspost) | **POST** /deals/transfer/status | Transfer Status
*MetricsApi* | [**PublicMetricsDealsOnChainGet**](docs/MetricsApi.md#publicmetricsdealsonchainget) | **GET** /public/metrics/deals-on-chain | Get deal metrics
*MinerApi* | [**PublicMinersDealsMinerGet**](docs/MinerApi.md#publicminersdealsminerget) | **GET** /public/miners/deals/{miner} | Get all miners deals
*MinerApi* | [**PublicMinersStatsMinerGet**](docs/MinerApi.md#publicminersstatsminerget) | **GET** /public/miners/stats/{miner} | Get miner stats
*NetApi* | [**PublicMinersFailuresMinerGet**](docs/NetApi.md#publicminersfailuresminerget) | **GET** /public/miners/failures/{miner} | Get all miners
*NetApi* | [**PublicMinersGet**](docs/NetApi.md#publicminersget) | **GET** /public/miners | Get all miners
*NetApi* | [**PublicNetAddrsGet**](docs/NetApi.md#publicnetaddrsget) | **GET** /public/net/addrs | Net Addrs
*NetApi* | [**PublicNetPeersGet**](docs/NetApi.md#publicnetpeersget) | **GET** /public/net/peers | Net Peers
*PinningApi* | [**PinningPinsGet**](docs/PinningApi.md#pinningpinsget) | **GET** /pinning/pins | List all pinned objects
*PinningApi* | [**PinningPinsPost**](docs/PinningApi.md#pinningpinspost) | **POST** /pinning/pins | Add and pin object
*PinningApi* | [**PinningPinsRequestidDelete**](docs/PinningApi.md#pinningpinsrequestiddelete) | **DELETE** /pinning/pins/{requestid} | Delete a pinned object
*PinningApi* | [**PinningPinsRequestidGet**](docs/PinningApi.md#pinningpinsrequestidget) | **GET** /pinning/pins/{requestid} | Get a pinned objects
*PinningApi* | [**PinningPinsRequestidPost**](docs/PinningApi.md#pinningpinsrequestidpost) | **POST** /pinning/pins/{requestid} | Replace a pinned object
*PublicApi* | [**ContentByCidCidGet**](docs/PublicApi.md#contentbycidcidget) | **GET** /content/by-cid/{cid} | Get Content by Cid
*PublicApi* | [**PublicByCidCidGet**](docs/PublicApi.md#publicbycidcidget) | **GET** /public/by-cid/{cid} | Get Content by Cid
*PublicApi* | [**PublicInfoGet**](docs/PublicApi.md#publicinfoget) | **GET** /public/info | Get public node info
*PublicApi* | [**PublicMetricsDealsOnChainGet**](docs/PublicApi.md#publicmetricsdealsonchainget) | **GET** /public/metrics/deals-on-chain | Get deal metrics
*PublicApi* | [**PublicMinersDealsMinerGet**](docs/PublicApi.md#publicminersdealsminerget) | **GET** /public/miners/deals/{miner} | Get all miners deals
*PublicApi* | [**PublicMinersFailuresMinerGet**](docs/PublicApi.md#publicminersfailuresminerget) | **GET** /public/miners/failures/{miner} | Get all miners
*PublicApi* | [**PublicMinersGet**](docs/PublicApi.md#publicminersget) | **GET** /public/miners | Get all miners
*PublicApi* | [**PublicMinersStatsMinerGet**](docs/PublicApi.md#publicminersstatsminerget) | **GET** /public/miners/stats/{miner} | Get miner stats
*PublicApi* | [**PublicMinersStorageQueryMinerGet**](docs/PublicApi.md#publicminersstoragequeryminerget) | **GET** /public/miners/storage/query/{miner} | Get miner stats
*PublicApi* | [**PublicNetAddrsGet**](docs/PublicApi.md#publicnetaddrsget) | **GET** /public/net/addrs | Net Addrs
*PublicApi* | [**PublicNetPeersGet**](docs/PublicApi.md#publicnetpeersget) | **GET** /public/net/peers | Net Peers
*PublicApi* | [**PublicStatsGet**](docs/PublicApi.md#publicstatsget) | **GET** /public/stats | Public stats
*UserApi* | [**UserApiKeysGet**](docs/UserApi.md#userapikeysget) | **GET** /user/api-keys | Get API keys for a user
*UserApi* | [**UserApiKeysKeyDelete**](docs/UserApi.md#userapikeyskeydelete) | **DELETE** /user/api-keys/{key} | Revoke a User API Key.
*UserApi* | [**UserApiKeysPost**](docs/UserApi.md#userapikeyspost) | **POST** /user/api-keys | Create API keys for a user
*UserApi* | [**UserExportGet**](docs/UserApi.md#userexportget) | **GET** /user/export | Export user data
*UserApi* | [**UserStatsGet**](docs/UserApi.md#userstatsget) | **GET** /user/stats | Create API keys for a user


## Documentation for Models

 - [Model.MainAddContentToCollectionParams](docs/MainAddContentToCollectionParams.md)
 - [Model.MainCollection](docs/MainCollection.md)
 - [Model.MainCreateCollectionBody](docs/MainCreateCollectionBody.md)
 - [Model.MainEstimateDealBody](docs/MainEstimateDealBody.md)
 - [Model.MainGetApiKeysResp](docs/MainGetApiKeysResp.md)
 - [Model.MainImportDealBody](docs/MainImportDealBody.md)
 - [Model.MainUserStatsResponse](docs/MainUserStatsResponse.md)
 - [Model.UtilContentAddIpfsBody](docs/UtilContentAddIpfsBody.md)
 - [Model.UtilHttpError](docs/UtilHttpError.md)


## Documentation for Authorization


### bearerAuth

- **Type**: API key

- **API key parameter name**: Authorization
- **Location**: HTTP header

