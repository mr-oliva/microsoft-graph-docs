---
title: "Get agreementFile"
description: "Retrieve the details of the default file for an agreement, including the language and version information. "
author: "raprakasMSFT"
ms.localizationpriority: medium
ms.prod: "governance"
doc_type: apiPageType
---

# Get agreementFile
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Retrieve the details of the default file for an agreement, including the language and version information. The file information is specified through the [agreementFile](../resources/agreementfile.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|Agreement.Read.All, Agreement.ReadWrite.All |
|Delegated (personal Microsoft account)|Not supported.|
|Application|Not supported.|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /agreements/{agreementsId}/file
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

If successful, this method returns a `200 OK` response code and a collection of [agreementFile](../resources/agreementfile.md) objects in the response body.

## Examples

### Request

# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_agreementfile"
}
-->
``` http
GET https://graph.microsoft.com/beta/identityGovernance/termsOfUse/agreements/94410bbf-3d3e-4683-8149-f034e55c39dd/file
```
# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-agreementfile-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-agreementfile-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/get-agreementfile-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/get-agreementfile-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Go](#tab/go)
[!INCLUDE [sample-code](../includes/snippets/go/get-agreementfile-go-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PowerShell](#tab/powershell)
[!INCLUDE [sample-code](../includes/snippets/powershell/get-agreementfile-powershell-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---



### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.agreementFile"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#identityGovernance/termsOfUse/agreements('94410bbf-3d3e-4683-8149-f034e55c39dd')/file/$entity",
    "@odata.type": "#microsoft.graph.agreementFileLocalization",
    "id": "08033369-8972-42a3-8533-90bbd2757a01",
    "fileName": "TOU.pdf",
    "displayName": "Contoso ToU for guest users",
    "language": "en",
    "isDefault": true,
    "isMajorVersion": false,
    "createdDateTime": "2022-03-04T13:14:13.9361722Z",
    "fileData": null
}
```

