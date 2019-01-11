---
title: Delete device
description: Elimina un dispositivo registrado.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: c2b34cffbff6b3c627ed13d6e4b2917f6f36f4f9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27854575"
---
# <a name="delete-device"></a><span data-ttu-id="6ebb7-103">Delete device</span><span class="sxs-lookup"><span data-stu-id="6ebb7-103">Delete device</span></span>

> <span data-ttu-id="6ebb7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6ebb7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6ebb7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6ebb7-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6ebb7-106">Elimina un dispositivo registrado.</span><span class="sxs-lookup"><span data-stu-id="6ebb7-106">Delete a registered device.</span></span>

## <a name="permissions"></a><span data-ttu-id="6ebb7-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="6ebb7-107">Permissions</span></span>
<span data-ttu-id="6ebb7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6ebb7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="6ebb7-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6ebb7-110">Permission type</span></span>      | <span data-ttu-id="6ebb7-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6ebb7-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6ebb7-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6ebb7-112">Delegated (work or school account)</span></span> | <span data-ttu-id="6ebb7-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="6ebb7-113">Directory.AccessAsUser.All</span></span> |
|<span data-ttu-id="6ebb7-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6ebb7-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6ebb7-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6ebb7-115">Not supported.</span></span>    |
|<span data-ttu-id="6ebb7-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6ebb7-116">Application</span></span> | <span data-ttu-id="6ebb7-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6ebb7-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="6ebb7-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6ebb7-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /devices/{id}

```

> <span data-ttu-id="6ebb7-119">Nota: El "id" de la solicitud es la propiedad "id" del dispositivo, no la propiedad "deviceId".</span><span class="sxs-lookup"><span data-stu-id="6ebb7-119">Note: The "id" in the request is the "id" property of the device, not the "deviceId" property.</span></span>

## <a name="request-headers"></a><span data-ttu-id="6ebb7-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6ebb7-120">Request headers</span></span>
| <span data-ttu-id="6ebb7-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="6ebb7-121">Name</span></span>       | <span data-ttu-id="6ebb7-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="6ebb7-122">Type</span></span> | <span data-ttu-id="6ebb7-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ebb7-123">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="6ebb7-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="6ebb7-124">Authorization</span></span>  | <span data-ttu-id="6ebb7-125">string</span><span class="sxs-lookup"><span data-stu-id="6ebb7-125">string</span></span>  | <span data-ttu-id="6ebb7-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6ebb7-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6ebb7-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6ebb7-128">Request body</span></span>
<span data-ttu-id="6ebb7-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6ebb7-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6ebb7-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ebb7-130">Response</span></span>

<span data-ttu-id="6ebb7-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6ebb7-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6ebb7-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6ebb7-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6ebb7-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6ebb7-134">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_device"
}-->
```http
DELETE https://graph.microsoft.com/beta/devices/{id}
```
##### <a name="response"></a><span data-ttu-id="6ebb7-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ebb7-135">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete device",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
