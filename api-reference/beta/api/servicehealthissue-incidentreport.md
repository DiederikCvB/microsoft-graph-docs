---
title: "serviceHealthIssue: incidentReport"
description: "Gets the post incident report (PIR) document of a specified service issue for tenant. This operation returns Edm.Stream. The PIR won't be returned to tenant if the specified issue is not visible to tenant."
author: "payiAzure"
localization_priority: Normal
ms.prod: "M365ServiceCommsPlatform"
doc_type: apiPageType
---

# serviceHealthIssue: incidentReport
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Gets the post incident report (PIR) document of a specified service issue for tenant. This operation returns Edm.Stream. The PIR won't be returned to tenant if the specified issue is not visible to tenant.


## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|ServiceHealth.Read.All|
|Delegated (personal Microsoft account)|ServiceHealth.Read.All|
|Application|ServiceHealth.Read.All|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /admin/serviceAnnouncement/issues('{serviceHealthIssueId}')/incidentReport
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this function returns a `200 OK` response code and a Stream in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "servicehealthissue_incidentreport"
}
-->
``` http
GET https://graph.microsoft.com/beta/admin/serviceAnnouncement/issues('MO248163')/incidentReport
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Edm.Stream"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": "Stream"
}
```
