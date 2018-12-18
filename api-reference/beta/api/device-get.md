---
title: Obtener device
description: Obtiene las propiedades y relaciones de un objeto device.
author: tfitzmac
ms.openlocfilehash: 632094db64cce86a965751d97b0ae9c92d439d5c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27348268"
---
# <a name="get-device"></a><span data-ttu-id="849a5-103">Obtener device</span><span class="sxs-lookup"><span data-stu-id="849a5-103">Get device</span></span>

> <span data-ttu-id="849a5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="849a5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="849a5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="849a5-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="849a5-106">Obtiene las propiedades y relaciones de un objeto device.</span><span class="sxs-lookup"><span data-stu-id="849a5-106">Get the properties and relationships of a device object.</span></span>

<span data-ttu-id="849a5-107">Puesto que el recurso de **dispositivo** es compatible con [las extensiones](/graph/extensibility-overview), también puede usar el `GET` operación para obtener las propiedades personalizadas y los datos de extensión en una instancia de **dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="849a5-107">Since the **device** resource supports [extensions](/graph/extensibility-overview), you can also use the `GET` operation to get custom properties and extension data in a **device** instance.</span></span>

## <a name="permissions"></a><span data-ttu-id="849a5-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="849a5-108">Permissions</span></span>
<span data-ttu-id="849a5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="849a5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="849a5-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="849a5-111">Permission type</span></span>      | <span data-ttu-id="849a5-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="849a5-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="849a5-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="849a5-113">Delegated (work or school account)</span></span> | <span data-ttu-id="849a5-114">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="849a5-114">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="849a5-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="849a5-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="849a5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="849a5-116">Not supported.</span></span>    |
|<span data-ttu-id="849a5-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="849a5-117">Application</span></span> | <span data-ttu-id="849a5-118">Device.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="849a5-118">Device.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="849a5-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="849a5-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /devices/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="849a5-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="849a5-120">Optional query parameters</span></span>
<span data-ttu-id="849a5-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="849a5-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="849a5-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="849a5-122">Request headers</span></span>
| <span data-ttu-id="849a5-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="849a5-123">Name</span></span>       | <span data-ttu-id="849a5-124">Type</span><span class="sxs-lookup"><span data-stu-id="849a5-124">Type</span></span> | <span data-ttu-id="849a5-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="849a5-125">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="849a5-126">Autorización</span><span class="sxs-lookup"><span data-stu-id="849a5-126">Authorization</span></span>  | <span data-ttu-id="849a5-127">string</span><span class="sxs-lookup"><span data-stu-id="849a5-127">string</span></span>  | <span data-ttu-id="849a5-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="849a5-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="849a5-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="849a5-130">Request body</span></span>
<span data-ttu-id="849a5-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="849a5-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="849a5-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="849a5-132">Response</span></span>

<span data-ttu-id="849a5-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [device](../resources/device.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="849a5-133">If successful, this method returns a `200 OK` response code and [device](../resources/device.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="849a5-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="849a5-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="849a5-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="849a5-135">Request</span></span>
<span data-ttu-id="849a5-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="849a5-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_device"
}-->
```http
GET https://graph.microsoft.com/beta/devices/{id}
```

> <span data-ttu-id="849a5-137">Nota: El "id" de la solicitud es la propiedad "id" del dispositivo, no la propiedad "deviceId".</span><span class="sxs-lookup"><span data-stu-id="849a5-137">Note: The "id" in the request is the "id" property of the device, not the "deviceId" property.</span></span>

##### <a name="response"></a><span data-ttu-id="849a5-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="849a5-138">Response</span></span>
<span data-ttu-id="849a5-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="849a5-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.device"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 322

{
  "accountEnabled": true,
  "approximateLastSignInDateTime": "2016-10-19T10:37:00Z",
  "deviceId": "deviceId-value",
  "deviceMetadata": "deviceMetadata-value",
  "deviceVersion": 99
}
```

## <a name="see-also"></a><span data-ttu-id="849a5-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="849a5-142">See also</span></span>

- [<span data-ttu-id="849a5-143">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="849a5-143">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="849a5-144">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="849a5-144">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
- [<span data-ttu-id="849a5-145">Agregar datos personalizados a grupos mediante extensiones de esquema (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="849a5-145">Add custom data to groups using schema extensions (preview)</span></span>](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get device",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->