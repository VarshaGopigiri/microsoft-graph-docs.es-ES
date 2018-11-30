---
title: Llamada a Delete
description: Elimine o colgar una llamada activa.
ms.openlocfilehash: ed0fb6928806511f92771237acb8ba08c8a162de
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085934"
---
# <a name="delete-call"></a><span data-ttu-id="4825f-103">Llamada a Delete</span><span class="sxs-lookup"><span data-stu-id="4825f-103">Delete call</span></span>

> <span data-ttu-id="4825f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4825f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4825f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4825f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4825f-106">Elimine o colgar una llamada activa.</span><span class="sxs-lookup"><span data-stu-id="4825f-106">Delete or hang up an active call.</span></span>

## <a name="permissions"></a><span data-ttu-id="4825f-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="4825f-107">Permissions</span></span>

<span data-ttu-id="4825f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4825f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="4825f-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4825f-110">Permission type</span></span> | <span data-ttu-id="4825f-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4825f-111">Permissions (from least to most privileged)</span></span>                  |
| :-------------- | :----------------------------------------------------------- |
| <span data-ttu-id="4825f-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4825f-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="4825f-113">No se admite.</span><span class="sxs-lookup"><span data-stu-id="4825f-113">Not Supported.</span></span>                         |
| <span data-ttu-id="4825f-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4825f-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4825f-115">No se admite.</span><span class="sxs-lookup"><span data-stu-id="4825f-115">Not Supported.</span></span>                         |
| <span data-ttu-id="4825f-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4825f-116">Application</span></span>                            | <span data-ttu-id="4825f-117">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="4825f-117">None.</span></span>                                  |

## <a name="http-request"></a><span data-ttu-id="4825f-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4825f-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /app/calls/{id}
DELETE /applications/{id}/calls/{id}
```

## <a name="request-headers"></a><span data-ttu-id="4825f-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4825f-119">Request headers</span></span>
| <span data-ttu-id="4825f-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="4825f-120">Name</span></span>          | <span data-ttu-id="4825f-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="4825f-121">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="4825f-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="4825f-122">Authorization</span></span> | <span data-ttu-id="4825f-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4825f-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4825f-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4825f-125">Request body</span></span>
<span data-ttu-id="4825f-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4825f-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4825f-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4825f-127">Response</span></span>
<span data-ttu-id="4825f-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4825f-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4825f-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4825f-130">Example</span></span>

##### <a name="request"></a><span data-ttu-id="4825f-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4825f-131">Request</span></span>
<span data-ttu-id="4825f-132">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4825f-132">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_call"
}-->
```http
DELETE https://graph.microsoft.com/beta/app/calls/{id}
```

##### <a name="response"></a><span data-ttu-id="4825f-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4825f-133">Response</span></span>

> <span data-ttu-id="4825f-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4825f-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

##### <a name="notification---terminating"></a><span data-ttu-id="4825f-136">-Notificación de finalización</span><span class="sxs-lookup"><span data-stu-id="4825f-136">Notification - terminating</span></span>

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

##### <a name="notification---terminated"></a><span data-ttu-id="4825f-137">Notificación - terminada</span><span class="sxs-lookup"><span data-stu-id="4825f-137">Notification - terminated</span></span>

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