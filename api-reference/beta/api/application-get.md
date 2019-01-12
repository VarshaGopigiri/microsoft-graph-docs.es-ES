---
title: Obtener la aplicación
description: Recuperar las propiedades y relaciones del objeto application.
author: lleonard-msft
localization_priority: Priority
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 444a95d437591bade674b350c67ec349b06f8d8c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27941810"
---
# <a name="get-application"></a><span data-ttu-id="69f6c-103">Obtener la aplicación</span><span class="sxs-lookup"><span data-stu-id="69f6c-103">Get application</span></span>

> <span data-ttu-id="69f6c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="69f6c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="69f6c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="69f6c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="69f6c-106">Recuperar las propiedades y relaciones del objeto application.</span><span class="sxs-lookup"><span data-stu-id="69f6c-106">Retrieve the properties and relationships of application object.</span></span>

## <a name="permissions"></a><span data-ttu-id="69f6c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="69f6c-107">Permissions</span></span>
<span data-ttu-id="69f6c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="69f6c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="69f6c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="69f6c-110">Permission type</span></span>      | <span data-ttu-id="69f6c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="69f6c-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="69f6c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="69f6c-112">Delegated (work or school account)</span></span> | <span data-ttu-id="69f6c-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="69f6c-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="69f6c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="69f6c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="69f6c-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="69f6c-115">Not supported.</span></span>    |
|<span data-ttu-id="69f6c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="69f6c-116">Application</span></span> | <span data-ttu-id="69f6c-117">Application.ReadWrite.OwnedBy, Application.ReadWrite.All, Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="69f6c-117">Application.ReadWrite.OwnedBy, Application.ReadWrite.All, Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="69f6c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="69f6c-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /applications/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="69f6c-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="69f6c-119">Optional query parameters</span></span>
<span data-ttu-id="69f6c-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="69f6c-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="69f6c-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="69f6c-121">Request headers</span></span>
| <span data-ttu-id="69f6c-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="69f6c-122">Name</span></span>       | <span data-ttu-id="69f6c-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="69f6c-123">Type</span></span> | <span data-ttu-id="69f6c-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="69f6c-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="69f6c-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="69f6c-125">Authorization</span></span>  | <span data-ttu-id="69f6c-126">string</span><span class="sxs-lookup"><span data-stu-id="69f6c-126">string</span></span>  | <span data-ttu-id="69f6c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="69f6c-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="69f6c-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="69f6c-129">Request body</span></span>
<span data-ttu-id="69f6c-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="69f6c-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="69f6c-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="69f6c-131">Response</span></span>

<span data-ttu-id="69f6c-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y la [aplicación](../resources/application.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="69f6c-132">If successful, this method returns a `200 OK` response code and [application](../resources/application.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="69f6c-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="69f6c-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="69f6c-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="69f6c-134">Request</span></span>
<span data-ttu-id="69f6c-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="69f6c-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_application"
}-->
```http
GET https://graph.microsoft.com/beta/applications/{id}
```
##### <a name="response"></a><span data-ttu-id="69f6c-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="69f6c-136">Response</span></span>
<span data-ttu-id="69f6c-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="69f6c-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.application"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 1044

{
  "api": {
    "acceptedAccessTokenVersion": 1,
    "publishedPermissionScopes": [
      {
        "adminConsentDescription": "adminConsentDescription-value",
        "adminConsentDisplayName": "adminConsentDisplayName-value",
        "id": "id-value",
        "isEnabled": true,
        "type": "type-value",
        "userConsentDescription": "userConsentDescription-value",
        "userConsentDisplayName": "userConsentDisplayName-value",
        "value": "value-value"
      }
    ]
  },
  "allowPublicClient": true,
  "applicationAliases": [
    "applicationAliases-value"
  ],
  "createdDateTime": "datetime-value",
  "installedClients": {
    "redirectUrls": [
      "redirectUrls-value"
    ]
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get application",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
