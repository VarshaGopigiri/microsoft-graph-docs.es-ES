---
title: Create device
description: Crea y registra un nuevo dispositivo en la organización.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 98ad7cd2735458a59f30a6ce00edb64015f7cf2d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27946108"
---
# <a name="create-device"></a><span data-ttu-id="f6e99-103">Create device</span><span class="sxs-lookup"><span data-stu-id="f6e99-103">Create device</span></span>

<span data-ttu-id="f6e99-104">Crea y registra un nuevo dispositivo en la organización.</span><span class="sxs-lookup"><span data-stu-id="f6e99-104">Create and register a new device in the organization.</span></span>

## <a name="permissions"></a><span data-ttu-id="f6e99-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="f6e99-105">Permissions</span></span>
<span data-ttu-id="f6e99-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f6e99-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="f6e99-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f6e99-108">Permission type</span></span>      | <span data-ttu-id="f6e99-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f6e99-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f6e99-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f6e99-110">Delegated (work or school account)</span></span> | <span data-ttu-id="f6e99-111">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="f6e99-111">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="f6e99-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f6e99-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f6e99-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f6e99-113">Not supported.</span></span>    |
|<span data-ttu-id="f6e99-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f6e99-114">Application</span></span> | <span data-ttu-id="f6e99-115">Device.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f6e99-115">Device.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="f6e99-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f6e99-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /devices

```
## <a name="request-headers"></a><span data-ttu-id="f6e99-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f6e99-117">Request headers</span></span>
| <span data-ttu-id="f6e99-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="f6e99-118">Name</span></span>       | <span data-ttu-id="f6e99-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="f6e99-119">Type</span></span> | <span data-ttu-id="f6e99-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6e99-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="f6e99-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="f6e99-121">Authorization</span></span>  | <span data-ttu-id="f6e99-122">string</span><span class="sxs-lookup"><span data-stu-id="f6e99-122">string</span></span>  | <span data-ttu-id="f6e99-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f6e99-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="f6e99-125">Tipo de contenido</span><span class="sxs-lookup"><span data-stu-id="f6e99-125">Content-type</span></span> | <span data-ttu-id="f6e99-126">string</span><span class="sxs-lookup"><span data-stu-id="f6e99-126">string</span></span> | <span data-ttu-id="f6e99-127">application/json</span><span class="sxs-lookup"><span data-stu-id="f6e99-127">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="f6e99-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f6e99-128">Request body</span></span>
<span data-ttu-id="f6e99-129">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [device](../resources/device.md).</span><span class="sxs-lookup"><span data-stu-id="f6e99-129">In the request body, supply a JSON representation of [device](../resources/device.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="f6e99-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f6e99-130">Response</span></span>

<span data-ttu-id="f6e99-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [device](../resources/device.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f6e99-131">If successful, this method returns `201 Created` response code and [device](../resources/device.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f6e99-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f6e99-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f6e99-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f6e99-133">Request</span></span>
<span data-ttu-id="f6e99-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f6e99-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_device_from_devices"
}-->
```http
POST https://graph.microsoft.com/v1.0/devices
Content-type: application/json

{
  "accountEnabled":false,
  "alternativeSecurityIds":
  [
    {
      "type":2,
      "key":"base64Y3YxN2E1MWFlYw=="
    }
  ],
  "deviceId":"4c299165-6e8f-4b45-a5ba-c5d250a707ff",
  "displayName":"Test device",
  "operatingSystem":"linux",
  "operatingSystemVersion":"1"
}
```
<span data-ttu-id="f6e99-135">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [device](../resources/device.md).</span><span class="sxs-lookup"><span data-stu-id="f6e99-135">In the request body, supply a JSON representation of [device](../resources/device.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="f6e99-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f6e99-136">Response</span></span>
<span data-ttu-id="f6e99-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f6e99-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.device"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "accountEnabled":false,
  "alternativeSecurityIds":
  [
    {
      "type":2,
      "key":"base64Y3YxN2E1MWFlYw=="
    }
  ],
  "deviceId":"4c299165-6e8f-4b45-a5ba-c5d250a707ff",
  "displayName":"Test device",
  "id": "id-value",
  "operatingSystem":"linux",
  "operatingSystemVersion":"1"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create device",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
