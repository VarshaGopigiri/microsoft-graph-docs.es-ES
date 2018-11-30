---
title: Actualizar synchronizationTemplate
description: Actualización (reemplazo) de la plantilla de sincronización asociada con una aplicación determinada.
ms.openlocfilehash: 9862b0a31294448e1b43e8438b76a16d471cb2d8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090260"
---
# <a name="update-synchronizationtemplate"></a><span data-ttu-id="3f51c-103">Actualizar synchronizationTemplate</span><span class="sxs-lookup"><span data-stu-id="3f51c-103">Update synchronizationTemplate</span></span>

> <span data-ttu-id="3f51c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3f51c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3f51c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3f51c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3f51c-106">Actualización (reemplazo) de la plantilla de sincronización asociada con una aplicación determinada.</span><span class="sxs-lookup"><span data-stu-id="3f51c-106">Update (override) the synchronization template associated with a given application.</span></span>

## <a name="permissions"></a><span data-ttu-id="3f51c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="3f51c-107">Permissions</span></span>
<span data-ttu-id="3f51c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3f51c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3f51c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3f51c-110">Permission type</span></span>                        | <span data-ttu-id="3f51c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3f51c-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="3f51c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3f51c-112">Delegated (work or school account)</span></span>     |<span data-ttu-id="3f51c-113">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3f51c-113">Directory.ReadWrite.All</span></span>  |
|<span data-ttu-id="3f51c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3f51c-114">Delegated (personal Microsoft account)</span></span> |<span data-ttu-id="3f51c-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3f51c-115">Not supported.</span></span>|
|<span data-ttu-id="3f51c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3f51c-116">Application</span></span>                            |<span data-ttu-id="3f51c-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3f51c-117">Not supported.</span></span>| 

### <a name="http-request"></a><span data-ttu-id="3f51c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3f51c-118">HTTP Request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PUT application/{id}/synchronization/templates/{templateId}
```

## <a name="request-headers"></a><span data-ttu-id="3f51c-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3f51c-119">Request headers</span></span>

| <span data-ttu-id="3f51c-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="3f51c-120">Name</span></span>           | <span data-ttu-id="3f51c-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="3f51c-121">Type</span></span>    | <span data-ttu-id="3f51c-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f51c-122">Description</span></span>|
|:---------------|:--------|:-----------|
| <span data-ttu-id="3f51c-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="3f51c-123">Authorization</span></span>  | <span data-ttu-id="3f51c-124">string</span><span class="sxs-lookup"><span data-stu-id="3f51c-124">string</span></span>  | <span data-ttu-id="3f51c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3f51c-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="3f51c-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3f51c-127">Request body</span></span>

<span data-ttu-id="3f51c-128">En el cuerpo de la solicitud, proporcione el objeto [synchronizationTemplate](../resources/synchronization-synchronizationtemplate.md) que va a reemplazar la plantilla existente.</span><span class="sxs-lookup"><span data-stu-id="3f51c-128">In the request body, supply the [synchronizationTemplate](../resources/synchronization-synchronizationtemplate.md) object to replace the existing template.</span></span> <span data-ttu-id="3f51c-129">Asegúrese de que todas las propiedades se proporcionan.</span><span class="sxs-lookup"><span data-stu-id="3f51c-129">Make sure all properties are provided.</span></span> <span data-ttu-id="3f51c-130">Se borrarán las propiedades que faltan.</span><span class="sxs-lookup"><span data-stu-id="3f51c-130">Missing properties will be erased.</span></span>

### <a name="response"></a><span data-ttu-id="3f51c-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3f51c-131">Response</span></span>

<span data-ttu-id="3f51c-p105">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3f51c-p105">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

### <a name="examples"></a><span data-ttu-id="3f51c-134">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3f51c-134">Examples</span></span>

##### <a name="request"></a><span data-ttu-id="3f51c-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3f51c-135">Request</span></span>
<span data-ttu-id="3f51c-136">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="3f51c-136">The following is an example of a request.</span></span> 

><span data-ttu-id="3f51c-137">**Nota:** El objeto de solicitud que se muestra aquí es más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="3f51c-137">**Note:** The request object shown here is shortened for readability.</span></span> <span data-ttu-id="3f51c-138">Incluir todas las propiedades en una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3f51c-138">Include all the properties in an actual call.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_synchronizationtemplate"
}-->
```http
PUT https://graph.microsoft.com/beta/applications/{id}/synchronization/templates/{templateId}
Authorization: Bearer <token>
Content-type: application/json

{
    "id": "Slack",
    "applicationId": "{id}",
    "factoryTag": "CustomSCIM"
}
```

##### <a name="response"></a><span data-ttu-id="3f51c-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3f51c-139">Response</span></span>
<span data-ttu-id="3f51c-140">El siguiente es un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="3f51c-140">The following is an example of a response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.synchronizationTemplate"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update synchronizationtemplate",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->