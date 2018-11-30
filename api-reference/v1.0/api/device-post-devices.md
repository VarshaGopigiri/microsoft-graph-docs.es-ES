---
title: Create device
description: Crea y registra un nuevo dispositivo en la organización.
ms.openlocfilehash: 7dd4ab48c66383990eb3fca4630717ba8063c67a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030269"
---
# <a name="create-device"></a><span data-ttu-id="d9c53-103">Create device</span><span class="sxs-lookup"><span data-stu-id="d9c53-103">Create device</span></span>

<span data-ttu-id="d9c53-104">Crea y registra un nuevo dispositivo en la organización.</span><span class="sxs-lookup"><span data-stu-id="d9c53-104">Create and register a new device in the organization.</span></span>

## <a name="permissions"></a><span data-ttu-id="d9c53-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="d9c53-105">Permissions</span></span>
<span data-ttu-id="d9c53-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d9c53-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="d9c53-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d9c53-108">Permission type</span></span>      | <span data-ttu-id="d9c53-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d9c53-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d9c53-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d9c53-110">Delegated (work or school account)</span></span> | <span data-ttu-id="d9c53-111">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="d9c53-111">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="d9c53-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d9c53-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d9c53-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d9c53-113">Not supported.</span></span>    |
|<span data-ttu-id="d9c53-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d9c53-114">Application</span></span> | <span data-ttu-id="d9c53-115">Device.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d9c53-115">Device.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d9c53-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d9c53-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /devices

```
## <a name="request-headers"></a><span data-ttu-id="d9c53-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d9c53-117">Request headers</span></span>
| <span data-ttu-id="d9c53-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="d9c53-118">Name</span></span>       | <span data-ttu-id="d9c53-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="d9c53-119">Type</span></span> | <span data-ttu-id="d9c53-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9c53-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="d9c53-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="d9c53-121">Authorization</span></span>  | <span data-ttu-id="d9c53-122">string</span><span class="sxs-lookup"><span data-stu-id="d9c53-122">string</span></span>  | <span data-ttu-id="d9c53-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d9c53-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d9c53-125">Tipo de contenido</span><span class="sxs-lookup"><span data-stu-id="d9c53-125">Content-type</span></span> | <span data-ttu-id="d9c53-126">string</span><span class="sxs-lookup"><span data-stu-id="d9c53-126">string</span></span> | <span data-ttu-id="d9c53-127">application/json</span><span class="sxs-lookup"><span data-stu-id="d9c53-127">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="d9c53-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d9c53-128">Request body</span></span>
<span data-ttu-id="d9c53-129">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [device](../resources/device.md).</span><span class="sxs-lookup"><span data-stu-id="d9c53-129">In the request body, supply a JSON representation of [device](../resources/device.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="d9c53-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d9c53-130">Response</span></span>

<span data-ttu-id="d9c53-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [device](../resources/device.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d9c53-131">If successful, this method returns `201 Created` response code and [device](../resources/device.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d9c53-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d9c53-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d9c53-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d9c53-133">Request</span></span>
<span data-ttu-id="d9c53-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d9c53-134">Here is an example of the request.</span></span>
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
<span data-ttu-id="d9c53-135">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [device](../resources/device.md).</span><span class="sxs-lookup"><span data-stu-id="d9c53-135">In the request body, supply a JSON representation of [device](../resources/device.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="d9c53-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d9c53-136">Response</span></span>
<span data-ttu-id="d9c53-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d9c53-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
