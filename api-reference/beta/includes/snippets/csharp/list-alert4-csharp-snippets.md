---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

// Code snippets are only available for the latest version. Current version is 5.x

// To initialize your graphClient, see https://learn.microsoft.com/en-us/graph/sdks/create-client?from=snippets&tabs=csharp
var result = await graphClient.Reports.HealthMonitoring.Alerts.GetAsync((requestConfiguration) =>
{
	requestConfiguration.QueryParameters.Expand = new string []{ "enrichment/impacts/microsoft.graph.healthmonitoring.directoryobjectimpactsummary/resourceSampling" };
	requestConfiguration.QueryParameters.Select = new string []{ "alertType"," createdDateTime"," enrichment'" };
});


```