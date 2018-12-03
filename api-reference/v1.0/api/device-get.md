---
title: Obtener device
description: Obtiene las propiedades y relaciones de un objeto device.
ms.openlocfilehash: 07ee10ccc6f3cfb7649df2cb3711bfff24115036
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032118"
---
# <a name="get-device"></a><span data-ttu-id="bf221-103">Obtener device</span><span class="sxs-lookup"><span data-stu-id="bf221-103">Get device</span></span>

<span data-ttu-id="bf221-104">Obtiene las propiedades y relaciones de un objeto device.</span><span class="sxs-lookup"><span data-stu-id="bf221-104">Get the properties and relationships of a device object.</span></span>
## <a name="permissions"></a><span data-ttu-id="bf221-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="bf221-105">Permissions</span></span>
<span data-ttu-id="bf221-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bf221-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="bf221-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bf221-108">Permission type</span></span>      | <span data-ttu-id="bf221-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bf221-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bf221-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bf221-110">Delegated (work or school account)</span></span> | <span data-ttu-id="bf221-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="bf221-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="bf221-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bf221-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bf221-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bf221-113">Not supported.</span></span>    |
|<span data-ttu-id="bf221-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bf221-114">Application</span></span> | <span data-ttu-id="bf221-115">Device.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bf221-115">Device.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="bf221-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bf221-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /devices/{id}
```
> <span data-ttu-id="bf221-117">Nota: El "id" de la solicitud es la propiedad "id" del dispositivo, no la propiedad "deviceId".</span><span class="sxs-lookup"><span data-stu-id="bf221-117">Note: The "id" in the request is the "id" property of the device, not the "deviceId" property.</span></span>

## <a name="optional-query-parameters"></a><span data-ttu-id="bf221-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="bf221-118">Optional query parameters</span></span>
<span data-ttu-id="bf221-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bf221-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="bf221-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bf221-120">Request headers</span></span>
| <span data-ttu-id="bf221-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="bf221-121">Name</span></span>       | <span data-ttu-id="bf221-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="bf221-122">Type</span></span> | <span data-ttu-id="bf221-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf221-123">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="bf221-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="bf221-124">Authorization</span></span>  | <span data-ttu-id="bf221-125">string</span><span class="sxs-lookup"><span data-stu-id="bf221-125">string</span></span>  | <span data-ttu-id="bf221-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bf221-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="bf221-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bf221-128">Request body</span></span>
<span data-ttu-id="bf221-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bf221-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bf221-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf221-130">Response</span></span>

<span data-ttu-id="bf221-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [device](../resources/device.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bf221-131">If successful, this method returns a `200 OK` response code and [device](../resources/device.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="bf221-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bf221-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="bf221-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bf221-133">Request</span></span>
<span data-ttu-id="bf221-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bf221-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_device"
}-->
```http
GET https://graph.microsoft.com/v1.0/devices/{id}
```
##### <a name="response"></a><span data-ttu-id="bf221-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf221-135">Response</span></span>
<span data-ttu-id="bf221-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bf221-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.device"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "accountEnabled":false,
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
  "description": "Get device",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->