---
title: Delete device
description: Elimina un dispositivo registrado.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 49bffc1147735aeefcbdb541804fbff386f2c77f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27917576"
---
# <a name="delete-device"></a><span data-ttu-id="f75f2-103">Delete device</span><span class="sxs-lookup"><span data-stu-id="f75f2-103">Delete device</span></span>

<span data-ttu-id="f75f2-104">Elimina un dispositivo registrado.</span><span class="sxs-lookup"><span data-stu-id="f75f2-104">Delete a registered device.</span></span>

## <a name="permissions"></a><span data-ttu-id="f75f2-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="f75f2-105">Permissions</span></span>
<span data-ttu-id="f75f2-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f75f2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="f75f2-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f75f2-108">Permission type</span></span>      | <span data-ttu-id="f75f2-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f75f2-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f75f2-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f75f2-110">Delegated (work or school account)</span></span> | <span data-ttu-id="f75f2-111">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="f75f2-111">Directory.AccessAsUser.All</span></span> |
|<span data-ttu-id="f75f2-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f75f2-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f75f2-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f75f2-113">Not supported.</span></span>    |
|<span data-ttu-id="f75f2-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f75f2-114">Application</span></span> | <span data-ttu-id="f75f2-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f75f2-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f75f2-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f75f2-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /devices/{id}
```
> <span data-ttu-id="f75f2-117">Nota: El "id" de la solicitud es la propiedad "id" del dispositivo, no la propiedad "deviceId".</span><span class="sxs-lookup"><span data-stu-id="f75f2-117">Note: The "id" in the request is the "id" property of the device, not the "deviceId" property.</span></span>

## <a name="request-headers"></a><span data-ttu-id="f75f2-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f75f2-118">Request headers</span></span>
| <span data-ttu-id="f75f2-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="f75f2-119">Name</span></span>       | <span data-ttu-id="f75f2-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="f75f2-120">Type</span></span> | <span data-ttu-id="f75f2-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="f75f2-121">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="f75f2-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="f75f2-122">Authorization</span></span>  | <span data-ttu-id="f75f2-123">string</span><span class="sxs-lookup"><span data-stu-id="f75f2-123">string</span></span>  | <span data-ttu-id="f75f2-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f75f2-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f75f2-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f75f2-126">Request body</span></span>
<span data-ttu-id="f75f2-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f75f2-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f75f2-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f75f2-128">Response</span></span>

<span data-ttu-id="f75f2-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f75f2-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f75f2-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f75f2-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f75f2-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f75f2-132">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_device"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/devices/{id}
```
##### <a name="response"></a><span data-ttu-id="f75f2-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f75f2-133">Response</span></span>

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
