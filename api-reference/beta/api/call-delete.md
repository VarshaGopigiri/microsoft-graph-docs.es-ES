---
title: Llamada a Delete
description: Elimine o colgar una llamada activa.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 0163f7eee4933406999e283378f31d7f5aeb92b8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27946770"
---
# <a name="delete-call"></a><span data-ttu-id="43251-103">Llamada a Delete</span><span class="sxs-lookup"><span data-stu-id="43251-103">Delete call</span></span>

> <span data-ttu-id="43251-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="43251-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="43251-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="43251-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="43251-106">Elimine o colgar una llamada activa.</span><span class="sxs-lookup"><span data-stu-id="43251-106">Delete or hang up an active call.</span></span>

## <a name="permissions"></a><span data-ttu-id="43251-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="43251-107">Permissions</span></span>

<span data-ttu-id="43251-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="43251-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="43251-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="43251-110">Permission type</span></span> | <span data-ttu-id="43251-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="43251-111">Permissions (from least to most privileged)</span></span>                  |
| :-------------- | :----------------------------------------------------------- |
| <span data-ttu-id="43251-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="43251-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="43251-113">No se admite.</span><span class="sxs-lookup"><span data-stu-id="43251-113">Not Supported.</span></span>                         |
| <span data-ttu-id="43251-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="43251-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="43251-115">No se admite.</span><span class="sxs-lookup"><span data-stu-id="43251-115">Not Supported.</span></span>                         |
| <span data-ttu-id="43251-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="43251-116">Application</span></span>                            | <span data-ttu-id="43251-117">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="43251-117">None.</span></span>                                  |

## <a name="http-request"></a><span data-ttu-id="43251-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="43251-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /app/calls/{id}
DELETE /applications/{id}/calls/{id}
```

## <a name="request-headers"></a><span data-ttu-id="43251-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="43251-119">Request headers</span></span>
| <span data-ttu-id="43251-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="43251-120">Name</span></span>          | <span data-ttu-id="43251-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="43251-121">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="43251-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="43251-122">Authorization</span></span> | <span data-ttu-id="43251-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="43251-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="43251-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="43251-125">Request body</span></span>
<span data-ttu-id="43251-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="43251-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="43251-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="43251-127">Response</span></span>
<span data-ttu-id="43251-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="43251-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="43251-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="43251-130">Example</span></span>

##### <a name="request"></a><span data-ttu-id="43251-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="43251-131">Request</span></span>
<span data-ttu-id="43251-132">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="43251-132">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "delete-call"
}-->
```http
DELETE https://graph.microsoft.com/beta/app/calls/{id}
```

##### <a name="response"></a><span data-ttu-id="43251-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="43251-133">Response</span></span>

> <span data-ttu-id="43251-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="43251-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

##### <a name="notification---terminating"></a><span data-ttu-id="43251-136">-Notificación de finalización</span><span class="sxs-lookup"><span data-stu-id="43251-136">Notification - terminating</span></span>

```http
POST https://bot.contoso.com/api/calls
Authorization: Bearer <TOKEN>
Content-Type: application/json
```

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.commsNotifications"
}-->
```json
{
  "value": [
    {
      "changeType": "updated",
      "resource": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896",
      "resourceData": {
        "@odata.type": "#microsoft.graph.call",
        "@odata.id": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896",
        "@odata.etag": "W/\"5445\"",
        "state": "terminating"
      }
    }
  ]
}
```

##### <a name="notification---terminated"></a><span data-ttu-id="43251-137">Notificación - terminada</span><span class="sxs-lookup"><span data-stu-id="43251-137">Notification - terminated</span></span>

```http
POST https://bot.contoso.com/api/calls
Authorization: Bearer <TOKEN>
Content-Type: application/json
```

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.commsNotifications"
}-->
```json
{
  "value": [
    {
      "changeType": "deleted",
      "resource": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896",
      "resourceData": {
        "@odata.type": "#microsoft.graph.call",
        "@odata.id": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896",
        "@odata.etag": "W/\"5445\"",
        "state": "terminated",
        "terminationReason": "AppInitiated"
      }
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete call",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
