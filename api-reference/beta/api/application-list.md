---
title: Aplicaciones de lista
description: Recuperar la lista de aplicaciones en esta organización.
author: lleonard-msft
localization_priority: Priority
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 455a0ecd4d0a5f5c94c1edb083e0aa80c816b043
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27971700"
---
# <a name="list-applications"></a><span data-ttu-id="01e84-103">Aplicaciones de lista</span><span class="sxs-lookup"><span data-stu-id="01e84-103">List applications</span></span>

> <span data-ttu-id="01e84-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="01e84-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="01e84-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="01e84-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="01e84-106">Recuperar la lista de aplicaciones en esta organización.</span><span class="sxs-lookup"><span data-stu-id="01e84-106">Retrieve the list of applications in this organization.</span></span>

## <a name="permissions"></a><span data-ttu-id="01e84-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="01e84-107">Permissions</span></span>
<span data-ttu-id="01e84-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="01e84-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="01e84-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="01e84-110">Permission type</span></span>      | <span data-ttu-id="01e84-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="01e84-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="01e84-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="01e84-112">Delegated (work or school account)</span></span> | <span data-ttu-id="01e84-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="01e84-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="01e84-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="01e84-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="01e84-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="01e84-115">Not supported.</span></span>    |
|<span data-ttu-id="01e84-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="01e84-116">Application</span></span> | <span data-ttu-id="01e84-117">Application.ReadWrite.All, Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="01e84-117">Application.ReadWrite.All, Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="01e84-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="01e84-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /applications
```
## <a name="optional-query-parameters"></a><span data-ttu-id="01e84-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="01e84-119">Optional query parameters</span></span>
<span data-ttu-id="01e84-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="01e84-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="01e84-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="01e84-121">Request headers</span></span>
| <span data-ttu-id="01e84-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="01e84-122">Name</span></span>       | <span data-ttu-id="01e84-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="01e84-123">Type</span></span> | <span data-ttu-id="01e84-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="01e84-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="01e84-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="01e84-125">Authorization</span></span>  | <span data-ttu-id="01e84-126">string</span><span class="sxs-lookup"><span data-stu-id="01e84-126">string</span></span>  | <span data-ttu-id="01e84-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="01e84-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="01e84-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="01e84-129">Request body</span></span>
<span data-ttu-id="01e84-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="01e84-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="01e84-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01e84-131">Response</span></span>

<span data-ttu-id="01e84-132">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de la [aplicación](../resources/application.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="01e84-132">If successful, this method returns a `200 OK` response code and a collection of [application](../resources/application.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="01e84-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="01e84-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="01e84-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="01e84-134">Request</span></span>
<span data-ttu-id="01e84-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="01e84-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "list_application"
}-->
```http
GET https://graph.microsoft.com/beta/applications
```
##### <a name="response"></a><span data-ttu-id="01e84-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01e84-136">Response</span></span>
<span data-ttu-id="01e84-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="01e84-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.application",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 1229

{
  "value": [
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
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List applications",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
