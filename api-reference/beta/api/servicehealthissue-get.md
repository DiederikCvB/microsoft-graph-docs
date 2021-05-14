---
title: "Get serviceHealthIssue"
description: "Get a specified service health issue for tenant. Returns the properties and relationships of a [serviceHealthIssue](../resources/servicehealthissue.md) object for the specified issue."
author: "payiAzure"
localization_priority: Normal
ms.prod: "M365ServiceCommsPlatform"
doc_type: apiPageType
---

# Get serviceHealthIssue
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a specified service health issue for tenant. Returns the properties and relationships of a [serviceHealthIssue](../resources/servicehealthissue.md) object for the specified issue.

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
GET /admin/serviceAnnouncement/issues('{issueId}'))
```

## Optional query parameters
This method supports some of the OData query parameters to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a [serviceHealthIssue](../resources/servicehealthissue.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "get_servicehealthissue"
}
-->
``` http
GET https://graph.microsoft.com/beta/admin/serviceAnnouncement/issues('MO226784')
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "m365ServiceHealth.readServices.commercialWebService.models.serviceHealthIssue"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": {
    "@odata.type": "#m365ServiceHealth.readServices.commercialWebService.models.serviceHealthIssue",
    "startDateTime": "2020-11-14T08:15:00Z",
    "endDateTime": "2020-11-14T09:45:00Z",
   "lastModifiedDateTime": "2020-11-14T11:06:53.353Z",
    "title": "Intermittently unable to access some Microsoft 365 services",
    "id": "MO226784",
    "impactDescription": "Users may have been intermittently unable to access some Microsoft 365 services.",
    "classification": "Advisory",
    "origin": "Microsoft",
    "status": "ServiceRestored",
    "service": "Microsoft 365 suite",
    "feature": "Access",
    "featureGroup": "Portal",
    "isResolved": true,
    "highImpact": false,
    "details": [],
    "posts": [
      {
        "contentType": "Text",
        "content": "Title: Intermittently unable to invite partners to meetings using some Microsoft 365 services\n\nUser Impact: Users may have been intermittently unable to invite partners to meetings using some Microsoft 365 services....",
        "createdDateTime": "2020-11-14T10:12:25.377Z"
      }
    ]
  }
}
```
