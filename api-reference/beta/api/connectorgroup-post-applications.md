---
title: Crear la aplicación
description: Utilice esta API para crear una nueva aplicación.
ms.openlocfilehash: 08300057f78671ce74dd98bd98f7d3182bde083d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086260"
---
# <a name="create-application"></a><span data-ttu-id="e9377-103">Crear la aplicación</span><span class="sxs-lookup"><span data-stu-id="e9377-103">Create application</span></span>

> <span data-ttu-id="e9377-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e9377-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e9377-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e9377-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e9377-106">Utilice esta API para crear una nueva aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9377-106">Use this API to create a new application.</span></span>
## <a name="permissions"></a><span data-ttu-id="e9377-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="e9377-107">Permissions</span></span>
<span data-ttu-id="e9377-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e9377-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e9377-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e9377-110">Permission type</span></span>      | <span data-ttu-id="e9377-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e9377-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e9377-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e9377-112">Delegated (work or school account)</span></span> | <span data-ttu-id="e9377-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="e9377-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="e9377-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e9377-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e9377-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e9377-115">Not supported.</span></span>    |
|<span data-ttu-id="e9377-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e9377-116">Application</span></span> | <span data-ttu-id="e9377-117">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e9377-117">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="e9377-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e9377-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /connectorGroups/{id}/applications

```
## <a name="request-headers"></a><span data-ttu-id="e9377-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e9377-119">Request headers</span></span>
| <span data-ttu-id="e9377-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="e9377-120">Name</span></span>       | <span data-ttu-id="e9377-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9377-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="e9377-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="e9377-122">Authorization</span></span>  | <span data-ttu-id="e9377-123">Bearer.</span><span class="sxs-lookup"><span data-stu-id="e9377-123">Bearer.</span></span> <span data-ttu-id="e9377-124">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="e9377-124">Required</span></span>|

## <a name="request-body"></a><span data-ttu-id="e9377-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e9377-125">Request body</span></span>
<span data-ttu-id="e9377-126">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [application](../resources/application.md) .</span><span class="sxs-lookup"><span data-stu-id="e9377-126">In the request body, supply a JSON representation of [application](../resources/application.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="e9377-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9377-127">Response</span></span>

<span data-ttu-id="e9377-128">Si tiene éxito, este método devuelve `201 Created` objeto de código y la [aplicación](../resources/application.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9377-128">If successful, this method returns `201 Created` response code and [application](../resources/application.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e9377-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e9377-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e9377-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e9377-130">Request</span></span>
<span data-ttu-id="e9377-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e9377-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_application_from_connectorgroup"
}-->
```http
POST https://graph.microsoft.com/{ver}/connectorGroups/{id}/applications
Content-type: application/json
Content-length: 329

{
  "@odata.id": "https://graph.microsoft.com/{ver}/applications/{id}"
}
```
<span data-ttu-id="e9377-132">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [application](../resources/application.md) .</span><span class="sxs-lookup"><span data-stu-id="e9377-132">In the request body, supply a JSON representation of [application](../resources/application.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="e9377-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9377-133">Response</span></span>
<span data-ttu-id="e9377-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e9377-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.application"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 355

{
  "appId": "appId-value",
  "onPremisesPublishing": {
    "externalUrl": "externalUrl-value",
    "internalUrl": "internalUrl-value",
    "externalAuthenticationType": "externalAuthenticationType-value",
    "customDomainCertificate": "customDomainCertificate-value",
    "isTranslateHostHeaderEnabled": true,
    "isOnPremPublishingEnabled": true
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
