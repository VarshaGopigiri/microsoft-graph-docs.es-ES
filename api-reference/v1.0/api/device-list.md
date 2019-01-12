---
title: List devices
description: Recupera una lista de objetos de dispositivo registrados en la organización.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: d6b67d883a834c6e36c8fdde91844cea15f4ce04
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27990470"
---
# <a name="list-devices"></a><span data-ttu-id="2a67e-103">List devices</span><span class="sxs-lookup"><span data-stu-id="2a67e-103">List devices</span></span>

<span data-ttu-id="2a67e-104">Recupera una lista de objetos de dispositivo registrados en la organización.</span><span class="sxs-lookup"><span data-stu-id="2a67e-104">Retrieve a list of device objects registered in the organization.</span></span>

## <a name="permissions"></a><span data-ttu-id="2a67e-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="2a67e-105">Permissions</span></span>
<span data-ttu-id="2a67e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2a67e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="2a67e-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2a67e-108">Permission type</span></span>      | <span data-ttu-id="2a67e-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2a67e-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2a67e-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2a67e-110">Delegated (work or school account)</span></span> | <span data-ttu-id="2a67e-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="2a67e-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="2a67e-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2a67e-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2a67e-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2a67e-113">Not supported.</span></span>    |
|<span data-ttu-id="2a67e-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2a67e-114">Application</span></span> | <span data-ttu-id="2a67e-115">Device.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2a67e-115">Device.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="2a67e-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2a67e-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /devices
```
## <a name="optional-query-parameters"></a><span data-ttu-id="2a67e-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="2a67e-117">Optional query parameters</span></span>
<span data-ttu-id="2a67e-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2a67e-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="2a67e-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2a67e-119">Request headers</span></span>
| <span data-ttu-id="2a67e-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="2a67e-120">Name</span></span>       | <span data-ttu-id="2a67e-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="2a67e-121">Type</span></span> | <span data-ttu-id="2a67e-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a67e-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="2a67e-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="2a67e-123">Authorization</span></span>  | <span data-ttu-id="2a67e-124">string</span><span class="sxs-lookup"><span data-stu-id="2a67e-124">string</span></span>  | <span data-ttu-id="2a67e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2a67e-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="2a67e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2a67e-127">Request body</span></span>
<span data-ttu-id="2a67e-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2a67e-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2a67e-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2a67e-129">Response</span></span>

<span data-ttu-id="2a67e-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [device](../resources/device.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2a67e-130">If successful, this method returns a `200 OK` response code and collection of [device](../resources/device.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="2a67e-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2a67e-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2a67e-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2a67e-132">Request</span></span>
<span data-ttu-id="2a67e-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2a67e-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_devices"
}-->
```http
GET https://graph.microsoft.com/v1.0/devices
```

##### <a name="response"></a><span data-ttu-id="2a67e-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2a67e-134">Response</span></span>
<span data-ttu-id="2a67e-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2a67e-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.device",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "accountEnabled":false,
      "deviceId":"4c299165-6e8f-4b45-a5ba-c5d250a707ff",
      "displayName":"Test device",
      "id": "id-value",
      "operatingSystem":"linux",
      "operatingSystemVersion":"1"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List devices",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
