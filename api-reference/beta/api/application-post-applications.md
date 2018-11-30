---
title: Crear la aplicación
description: Utilice esta API para crear una nueva aplicación.
ms.openlocfilehash: d192f543d123c29cf2686c203ffc8c7c69b1bcc9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084657"
---
# <a name="create-application"></a><span data-ttu-id="6a07e-103">Crear la aplicación</span><span class="sxs-lookup"><span data-stu-id="6a07e-103">Create Application</span></span>

> <span data-ttu-id="6a07e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6a07e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6a07e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6a07e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6a07e-106">Utilice esta API para crear una nueva aplicación.</span><span class="sxs-lookup"><span data-stu-id="6a07e-106">Use this API to create a new application.</span></span>

## <a name="permissions"></a><span data-ttu-id="6a07e-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="6a07e-107">Permissions</span></span>
<span data-ttu-id="6a07e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6a07e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="6a07e-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6a07e-110">Permission type</span></span>      | <span data-ttu-id="6a07e-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6a07e-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6a07e-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6a07e-112">Delegated (work or school account)</span></span> | <span data-ttu-id="6a07e-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="6a07e-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="6a07e-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6a07e-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6a07e-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6a07e-115">Not supported.</span></span>    |
|<span data-ttu-id="6a07e-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6a07e-116">Application</span></span> | <span data-ttu-id="6a07e-117">Application.ReadWrite.OwnedBy, Application.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6a07e-117">Application.ReadWrite.OwnedBy, Application.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="6a07e-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6a07e-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /applications
```

## <a name="request-headers"></a><span data-ttu-id="6a07e-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6a07e-119">Request headers</span></span>
| <span data-ttu-id="6a07e-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="6a07e-120">Name</span></span>       | <span data-ttu-id="6a07e-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="6a07e-121">Type</span></span> | <span data-ttu-id="6a07e-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a07e-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="6a07e-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="6a07e-123">Authorization</span></span>  | <span data-ttu-id="6a07e-124">string</span><span class="sxs-lookup"><span data-stu-id="6a07e-124">string</span></span>  | <span data-ttu-id="6a07e-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6a07e-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6a07e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6a07e-127">Request body</span></span>
<span data-ttu-id="6a07e-128">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [application](../resources/application.md) .</span><span class="sxs-lookup"><span data-stu-id="6a07e-128">In the request body, supply a JSON representation of [application](../resources/application.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="6a07e-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6a07e-129">Response</span></span>

<span data-ttu-id="6a07e-130">Si tiene éxito, este método devuelve `201 Created` objeto de código y la [aplicación](../resources/application.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6a07e-130">If successful, this method returns `201 Created` response code and [application](../resources/application.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6a07e-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6a07e-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6a07e-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6a07e-132">Request</span></span>
<span data-ttu-id="6a07e-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6a07e-133">Here is an example of the request.</span></span>
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
<span data-ttu-id="6a07e-134">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [application](../resources/application.md) .</span><span class="sxs-lookup"><span data-stu-id="6a07e-134">In the request body, supply a JSON representation of [application](../resources/application.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="6a07e-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6a07e-135">Response</span></span>
<span data-ttu-id="6a07e-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6a07e-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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