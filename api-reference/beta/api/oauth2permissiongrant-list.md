---
title: Lista oauth2PermissionGrants
description: Recuperar una lista de objetos de oauth2PermissionGrant.
localization_priority: Normal
ms.openlocfilehash: f75ae0922b8c02ab3b290b471db2e649a000fbcc
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27813786"
---
# <a name="list-oauth2permissiongrants"></a><span data-ttu-id="532f3-103">Lista oauth2PermissionGrants</span><span class="sxs-lookup"><span data-stu-id="532f3-103">List oauth2PermissionGrants</span></span>

> <span data-ttu-id="532f3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="532f3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="532f3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="532f3-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="532f3-106">Recuperar una lista de objetos de oauth2PermissionGrant.</span><span class="sxs-lookup"><span data-stu-id="532f3-106">Retrieve a list of oauth2PermissionGrant objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="532f3-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="532f3-107">Permissions</span></span>

<span data-ttu-id="532f3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="532f3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="532f3-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="532f3-110">Permission type</span></span>      | <span data-ttu-id="532f3-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="532f3-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="532f3-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="532f3-112">Delegated (work or school account)</span></span> | <span data-ttu-id="532f3-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="532f3-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="532f3-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="532f3-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="532f3-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="532f3-115">Not supported.</span></span>    |
|<span data-ttu-id="532f3-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="532f3-116">Application</span></span> | <span data-ttu-id="532f3-117">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="532f3-117">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="532f3-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="532f3-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /oauth2PermissionGrants
```
## <a name="optional-query-parameters"></a><span data-ttu-id="532f3-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="532f3-119">Optional query parameters</span></span>
<span data-ttu-id="532f3-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="532f3-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="532f3-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="532f3-121">Request headers</span></span>
| <span data-ttu-id="532f3-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="532f3-122">Name</span></span> | <span data-ttu-id="532f3-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="532f3-123">Description</span></span> |
|:----------|:----------|
| <span data-ttu-id="532f3-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="532f3-124">Authorization</span></span>  | <span data-ttu-id="532f3-125">string</span><span class="sxs-lookup"><span data-stu-id="532f3-125">string</span></span>  | <span data-ttu-id="532f3-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="532f3-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="532f3-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="532f3-128">Request body</span></span>
<span data-ttu-id="532f3-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="532f3-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="532f3-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="532f3-130">Response</span></span>

<span data-ttu-id="532f3-131">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [oAuth2PermissionGrant](../resources/oauth2permissiongrant.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="532f3-131">If successful, this method returns a `200 OK` response code and collection of [oAuth2PermissionGrant](../resources/oauth2permissiongrant.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="532f3-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="532f3-132">Example</span></span>

##### <a name="request"></a><span data-ttu-id="532f3-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="532f3-133">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_oauth2permissiongrants"
}-->
```http
GET https://graph.microsoft.com/beta/oauth2PermissionGrants
```
##### <a name="response"></a><span data-ttu-id="532f3-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="532f3-134">Response</span></span>

<span data-ttu-id="532f3-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="532f3-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.oAuth2Permissiongrant",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 259

{
  "value": [
    {
      "clientId": "clientId-value",
      "consentType": "consentType-value",
      "expiryTime": "datetime-value",
      "id": "id-value",
      "principalId": "principalId-value",
      "resourceId": "resourceId-value",
      "scope": "scope-value",
      "startTime": "datetime-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List oauth2PermissionGrants",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
