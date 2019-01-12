---
title: Create device
description: Crear un nuevo dispositivo.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 0d24829a057326d35b2b35e0ba72d736e3afb15c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27971602"
---
# <a name="create-device"></a><span data-ttu-id="9240a-103">Create device</span><span class="sxs-lookup"><span data-stu-id="9240a-103">Create device</span></span>

> <span data-ttu-id="9240a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9240a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9240a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9240a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9240a-106">Crear un nuevo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9240a-106">Create a new device.</span></span>
## <a name="permissions"></a><span data-ttu-id="9240a-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="9240a-107">Permissions</span></span>
<span data-ttu-id="9240a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9240a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="9240a-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9240a-110">Permission type</span></span>      | <span data-ttu-id="9240a-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9240a-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9240a-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9240a-112">Delegated (work or school account)</span></span> | <span data-ttu-id="9240a-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="9240a-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="9240a-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9240a-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9240a-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9240a-115">Not supported.</span></span>    |
|<span data-ttu-id="9240a-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9240a-116">Application</span></span> | <span data-ttu-id="9240a-117">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9240a-117">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="9240a-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9240a-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /devices

```
## <a name="request-headers"></a><span data-ttu-id="9240a-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9240a-119">Request headers</span></span>
| <span data-ttu-id="9240a-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="9240a-120">Name</span></span>       | <span data-ttu-id="9240a-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="9240a-121">Type</span></span> | <span data-ttu-id="9240a-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="9240a-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="9240a-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="9240a-123">Authorization</span></span>  | <span data-ttu-id="9240a-124">string</span><span class="sxs-lookup"><span data-stu-id="9240a-124">string</span></span>  | <span data-ttu-id="9240a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9240a-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9240a-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9240a-127">Request body</span></span>
<span data-ttu-id="9240a-128">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [device](../resources/device.md).</span><span class="sxs-lookup"><span data-stu-id="9240a-128">In the request body, supply a JSON representation of [device](../resources/device.md) object.</span></span>

<span data-ttu-id="9240a-129">Puesto que el recurso de **dispositivo** es compatible con [las extensiones](/graph/extensibility-overview), puede usar el `POST` operación y agregar propiedades personalizadas con sus propios datos a la instancia de dispositivo al crearla.</span><span class="sxs-lookup"><span data-stu-id="9240a-129">Since the **device** resource supports [extensions](/graph/extensibility-overview), you can use the `POST` operation and add custom properties with your own data to the device instance while creating it.</span></span>

## <a name="response"></a><span data-ttu-id="9240a-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9240a-130">Response</span></span>

<span data-ttu-id="9240a-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [device](../resources/device.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9240a-131">If successful, this method returns `201 Created` response code and [device](../resources/device.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9240a-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9240a-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9240a-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9240a-133">Request</span></span>
<span data-ttu-id="9240a-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9240a-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_device_from_devices"
}-->
```http
POST https://graph.microsoft.com/beta/devices
Content-type: application/json
Content-length: 364

{
  "accountEnabled": true,
  "alternativeSecurityIds": [
    {
      "type": 99,
      "identityProvider": "identityProvider-value",
      "key": "key-value"
    }
  ],
  "approximateLastSignInDateTime": "2016-10-19T10:37:00Z",
  "deviceId": "deviceId-value",
  "deviceMetadata": "deviceMetadata-value",
  "deviceVersion": 99
}
```
<span data-ttu-id="9240a-135">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [device](../resources/device.md).</span><span class="sxs-lookup"><span data-stu-id="9240a-135">In the request body, supply a JSON representation of [device](../resources/device.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="9240a-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9240a-136">Response</span></span>
<span data-ttu-id="9240a-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9240a-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.device"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 364

{
  "accountEnabled": true,
  "alternativeSecurityIds": [
    {
      "type": 99,
      "identityProvider": "identityProvider-value",
      "key": "key-value"
    }
  ],
  "approximateLastSignInDateTime": "2016-10-19T10:37:00Z",
  "deviceId": "deviceId-value",
  "deviceMetadata": "deviceMetadata-value",
  "deviceVersion": 99
}
```

## <a name="see-also"></a><span data-ttu-id="9240a-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="9240a-140">See also</span></span>

- [<span data-ttu-id="9240a-141">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="9240a-141">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="9240a-142">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="9240a-142">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
- [<span data-ttu-id="9240a-143">Agregar datos personalizados a grupos mediante extensiones de esquema (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="9240a-143">Add custom data to groups using schema extensions (preview)</span></span>](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create device",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
