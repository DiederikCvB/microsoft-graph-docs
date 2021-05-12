---
title: "Update verifiableCredentialsContract"
description: "Update the properties of a verifiableCredentialsContract object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Update verifiableCredentialsContract
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of a [verifiableCredentialsContract](../resources/verifiablecredentialscontract.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|**TODO: Provide applicable permissions.**|
|Delegated (personal Microsoft account)|**TODO: Provide applicable permissions.**|
|Application|**TODO: Provide applicable permissions.**|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /verifiableCredentialsIssuer/contracts/{verifiableCredentialsContractId}
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [verifiableCredentialsContract](../resources/verifiablecredentialscontract.md) object.

The following table shows the properties that are required when you update the [verifiableCredentialsContract](../resources/verifiablecredentialscontract.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description**|
|contractName|String|**TODO: Add Description**|
|rulesFileUrl|String|**TODO: Add Description**|
|displayFileUrl|String|**TODO: Add Description**|



## Response

If successful, this method returns a `200 OK` response code and an updated [verifiableCredentialsContract](../resources/verifiablecredentialscontract.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "update_verifiablecredentialscontract"
}
-->
``` http
PATCH https://graph.microsoft.com/beta/verifiableCredentialsIssuer/contracts/{verifiableCredentialsContractId}
Content-Type: application/json
Content-length: 160

{
  "@odata.type": "#microsoft.graph.verifiableCredentialsContract",
  "contractName": "String",
  "rulesFileUrl": "String",
  "displayFileUrl": "String"
}
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.verifiableCredentialsContract",
  "id": "734a868f-868f-734a-8f86-4a738f864a73",
  "contractName": "String",
  "rulesFileUrl": "String",
  "displayFileUrl": "String"
}
```
