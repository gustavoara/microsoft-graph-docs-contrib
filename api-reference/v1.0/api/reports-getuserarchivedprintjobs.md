---
title: "reports: getUserArchivedPrintJobs"
description: Get a list of archived print jobs for a particular user.
author: nilakhan
ms.localizationpriority: medium
ms.subservice: universal-print
doc_type: apiPageType
ms.date: 04/04/2024
---

# reportRoot: getUserArchivedPrintJobs
Namespace: microsoft.graph

Get a list of archived print jobs for a particular user.

[!INCLUDE [national-cloud-support](../../includes/global-us.md)]

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "reports_getuserarchivedprintjobs" } -->
[!INCLUDE [permissions-table](../includes/permissions/reports-getuserarchivedprintjobs-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /reports/getUserArchivedPrintJobs(userId='{userId}',startDateTime='{startDateTime}',endDateTime='{endDateTime}')
```

## Function Parameters

In the request URL, provide the following function parameters with values:

| Parameter     | Type                 | Required? | Description                                                          |
|---------------|----------------------|-----------|----------------------------------------------------------------------|
| `userId`      | `Edm.String`         | Yes       | The ID of the user to return data for.                               |
| `startDateTime` | `Edm.DateTimeOffset` | No        | The start date (inclusive) for the time period to include data from.|
| `endDateTime`   | `Edm.DateTimeOffset` | No        | The end date (inclusive) for the time period to include data from.|

>**Note:** If a value is not required, pass the parameter with null value.
## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required. Learn more about [authentication and authorization](/graph/auth/auth-concepts).|

## Request body
Don't supply a request body for this method.

## Response

If successful, this function returns a `200 OK` response code and a [archivedPrintJob](../resources/archivedprintjob.md) collection in the response body.

## Examples

### Request
# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "reportroot_getuserarchivedprintjobs"
}
-->
``` http
GET https://graph.microsoft.com/v1.0/reports/getUserArchivedPrintJobs(userId='{id}',startDateTime=<timestamp>,endDateTime=<timestamp>)
```

# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/reportroot-getuserarchivedprintjobs-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [CLI](#tab/cli)
[!INCLUDE [sample-code](../includes/snippets/cli/reportroot-getuserarchivedprintjobs-cli-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Go](#tab/go)
[!INCLUDE [sample-code](../includes/snippets/go/reportroot-getuserarchivedprintjobs-go-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/reportroot-getuserarchivedprintjobs-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PHP](#tab/php)
[!INCLUDE [sample-code](../includes/snippets/php/reportroot-getuserarchivedprintjobs-php-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PowerShell](#tab/powershell)
[!INCLUDE [sample-code](../includes/snippets/powershell/reportroot-getuserarchivedprintjobs-powershell-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Python](#tab/python)
[!INCLUDE [sample-code](../includes/snippets/python/reportroot-getuserarchivedprintjobs-python-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.archivedPrintJob)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "id": "016b5565-3bbf-4067-b9ff-4d68167eb1a6",
      "printerId": "016b5565-3bbf-4067-b9ff-4d68167eb1a6",
      "printerName": "printerName1",
      "processingState": "completed",
      "createdDateTime": "2023-06-29T00:00:00.0000000Z",
      "acquiredDateTime": "2023-06-29T00:00:01.0000000Z",
      "completionDateTime": "2023-06-29T00:00:02.0000000Z",
      "acquiredByPrinter": true,
      "copiesPrinted": 1,
      "createdBy": {
        "displayName": "username",
        "userPrincipalName": "username@contoso.com",
      }
    }
  ]
}
```

