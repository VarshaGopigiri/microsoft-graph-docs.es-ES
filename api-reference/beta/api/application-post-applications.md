---
title: Crear la aplicación
description: Utilice esta API para crear una nueva aplicación.
author: lleonard-msft
localization_priority: Priority
ms.openlocfilehash: 9a4ca06bfd19dbe6319bb276cd5c33fc13f6d81d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27855009"
---
# <a name="create-application"></a><span data-ttu-id="7b59f-103">Crear la aplicación</span><span class="sxs-lookup"><span data-stu-id="7b59f-103">Create Application</span></span>

> <span data-ttu-id="7b59f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7b59f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7b59f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7b59f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7b59f-106">Utilice esta API para crear una nueva aplicación.</span><span class="sxs-lookup"><span data-stu-id="7b59f-106">Use this API to create a new application.</span></span>

## <a name="permissions"></a><span data-ttu-id="7b59f-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="7b59f-107">Permissions</span></span>
<span data-ttu-id="7b59f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7b59f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="7b59f-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7b59f-110">Permission type</span></span>      | <span data-ttu-id="7b59f-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7b59f-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7b59f-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7b59f-112">Delegated (work or school account)</span></span> | <span data-ttu-id="7b59f-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="7b59f-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="7b59f-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7b59f-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7b59f-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7b59f-115">Not supported.</span></span>    |
|<span data-ttu-id="7b59f-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7b59f-116">Application</span></span> | <span data-ttu-id="7b59f-117">Application.ReadWrite.OwnedBy, Application.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7b59f-117">Application.ReadWrite.OwnedBy, Application.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="7b59f-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7b59f-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /applications
```

## <a name="request-headers"></a><span data-ttu-id="7b59f-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7b59f-119">Request headers</span></span>
| <span data-ttu-id="7b59f-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="7b59f-120">Name</span></span>       | <span data-ttu-id="7b59f-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="7b59f-121">Type</span></span> | <span data-ttu-id="7b59f-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b59f-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="7b59f-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="7b59f-123">Authorization</span></span>  | <span data-ttu-id="7b59f-124">string</span><span class="sxs-lookup"><span data-stu-id="7b59f-124">string</span></span>  | <span data-ttu-id="7b59f-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7b59f-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="7b59f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7b59f-127">Request body</span></span>
<span data-ttu-id="7b59f-128">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [application](../resources/application.md) .</span><span class="sxs-lookup"><span data-stu-id="7b59f-128">In the request body, supply a JSON representation of [application](../resources/application.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="7b59f-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7b59f-129">Response</span></span>

<span data-ttu-id="7b59f-130">Si tiene éxito, este método devuelve `201 Created` objeto de código y la [aplicación](../resources/application.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7b59f-130">If successful, this method returns `201 Created` response code and [application](../resources/application.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7b59f-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7b59f-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7b59f-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7b59f-132">Request</span></span>
<span data-ttu-id="7b59f-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7b59f-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_application_from_applications"
}-->
```http
POST https://graph.microsoft.com/beta/applications
Content-type: application/json
Content-length: 67

{
  "allowPublicClient": true,
  "displayName": "Display name"
}
```
<span data-ttu-id="7b59f-134">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [application](../resources/application.md) .</span><span class="sxs-lookup"><span data-stu-id="7b59f-134">In the request body, supply a JSON representation of [application](../resources/application.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="7b59f-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7b59f-135">Response</span></span>
<span data-ttu-id="7b59f-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7b59f-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.application"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 1145

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#applications/$entity",
    "id": "b5b2920e-a47c-43b7-91ef-25ae96fddddd",
    "deletedDateTime": null,
    "api": {
        "acceptedAccessTokenVersion": 2,
        "publishedPermissionScopes": []
    },
    "allowPublicClient": true,
    "applicationAliases": [],
    "appRoles": [],
    "createdDateTime": "2017-05-25T16:33:04.3646617Z",
    "installedClients": {
        "redirectUrls": []
    },
    "displayName": "Display name",
    "info": {
        "termsOfServiceUrl": null,
        "supportUrl": null,
        "privacyStatementUrl": null,
        "marketingUrl": null,
        "logoUrl": null
    },
    "keyCredentials": [],
    "orgRestrictions": [],
    "passwordCredentials": [],
    "preAuthorizedApplications": [],
    "requiredResourceAccess": [],
    "tags": [],
    "web": {
        "redirectUrls": [],
        "logoutUrl": null,
        "oauth2AllowImplicitFlow": null
    }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create application",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
