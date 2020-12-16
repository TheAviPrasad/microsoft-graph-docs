---
title: "Get temporaryAccessPassAuthenticationMethodConfiguration"
description: "Read the properties and relationships of a temporaryAccessPassAuthenticationMethodConfiguration object."
author: "inbarckms"
localization_priority: Normal
ms.prod: "microsoft-identity-platform"
doc_type: apiPageType
---

# Get temporaryAccessPassAuthenticationMethodConfiguration
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Read the properties and relationships of a [temporaryAccessPassAuthenticationMethodConfiguration](../resources/temporaryaccesspassauthenticationmethodconfiguration.md) object, which represents the Temporary Access Pass [authentication method policy](../resources/authenticationmethodspolicies-overview.md) for the Azure Active Directory (Azure AD) tenant.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from most to least privileged)|
|:---|:---|
|Delegated (work or school account)|Policy.ReadWrite.AuthenticationMethod|
|Delegated (personal Microsoft account)|Not supported.|
|Application|Policy.ReadWrite.AuthenticationMethod|


For delegated scenarios the administrator needs one of the following [roles](/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles):

* Global admin


## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /policies/authenticationMethodsPolicy/authenticationMethodConfigurations/TemporaryAccessPass
```
## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

### Response
The following is an example of the response.

**Note:** The response object shown here might be shortened for readability.
<!-- {​​​​​
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.fido2AuthenticationMethodConfiguration"
}​​​​​
-->
``` http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#authenticationMethodConfigurations/$entity",
    "@odata.type": "#microsoft.graph.temporaryAccessPassAuthenticationMethodConfiguration",
    "id": "TemporaryAccessPass",
    "state": "enabled",
    "defaultLifetimeInMinutes": Integer,
    "defaultLength": Integer,
    "minimumLifetimeInMinutes": Integer,
    "maximumLifetimeInMinutes": Integer,
    "isUsableOnce": Boolean,
    "includeTargets":[
         {​​​​​
            "targetType":"group",
            "id":"all_users",
            "isRegistrationRequired":false,
            "useForSignIn":true
         }​​​​​
    ]
}
```