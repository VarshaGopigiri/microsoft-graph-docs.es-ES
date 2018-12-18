---
title: List devices
description: Recupera una lista de objetos de dispositivo registrados en la organización.
author: tfitzmac
ms.openlocfilehash: a17dcdd3fc15a04276095b2f356cc780ae6a8fee
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27314381"
---
# <a name="list-devices"></a><span data-ttu-id="b17b9-103">List devices</span><span class="sxs-lookup"><span data-stu-id="b17b9-103">List devices</span></span>

<span data-ttu-id="b17b9-104">Recupera una lista de objetos de dispositivo registrados en la organización.</span><span class="sxs-lookup"><span data-stu-id="b17b9-104">Retrieve a list of device objects registered in the organization.</span></span>

## <a name="permissions"></a><span data-ttu-id="b17b9-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="b17b9-105">Permissions</span></span>
<span data-ttu-id="b17b9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b17b9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="b17b9-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b17b9-108">Permission type</span></span>      | <span data-ttu-id="b17b9-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b17b9-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b17b9-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b17b9-110">Delegated (work or school account)</span></span> | <span data-ttu-id="b17b9-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="b17b9-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="b17b9-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b17b9-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b17b9-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b17b9-113">Not supported.</span></span>    |
|<span data-ttu-id="b17b9-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b17b9-114">Application</span></span> | <span data-ttu-id="b17b9-115">Device.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b17b9-115">Device.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="b17b9-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b17b9-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /devices
```
## <a name="optional-query-parameters"></a><span data-ttu-id="b17b9-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b17b9-117">Optional query parameters</span></span>
<span data-ttu-id="b17b9-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b17b9-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="b17b9-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b17b9-119">Request headers</span></span>
| <span data-ttu-id="b17b9-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="b17b9-120">Name</span></span>       | <span data-ttu-id="b17b9-121">Type</span><span class="sxs-lookup"><span data-stu-id="b17b9-121">Type</span></span> | <span data-ttu-id="b17b9-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="b17b9-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="b17b9-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="b17b9-123">Authorization</span></span>  | <span data-ttu-id="b17b9-124">string</span><span class="sxs-lookup"><span data-stu-id="b17b9-124">string</span></span>  | <span data-ttu-id="b17b9-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b17b9-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b17b9-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b17b9-127">Request body</span></span>
<span data-ttu-id="b17b9-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b17b9-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b17b9-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b17b9-129">Response</span></span>

<span data-ttu-id="b17b9-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [device](../resources/device.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b17b9-130">If successful, this method returns a `200 OK` response code and collection of [device](../resources/device.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="b17b9-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b17b9-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b17b9-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b17b9-132">Request</span></span>
<span data-ttu-id="b17b9-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b17b9-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_devices"
}-->
```http
GET https://graph.microsoft.com/v1.0/devices
```

##### <a name="response"></a><span data-ttu-id="b17b9-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b17b9-134">Response</span></span>
<span data-ttu-id="b17b9-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b17b9-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
