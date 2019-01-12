---
title: List registeredUsers
description: Recupera una lista de usuarios que son usuarios registrados del dispositivo.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: d3a5e8dbc92860ac4829f4aa4c3e509e6f4ec9b4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27980604"
---
# <a name="list-registeredusers"></a><span data-ttu-id="6b715-103">List registeredUsers</span><span class="sxs-lookup"><span data-stu-id="6b715-103">List registeredUsers</span></span>

> <span data-ttu-id="6b715-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6b715-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6b715-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6b715-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6b715-106">Recupera una lista de usuarios que son usuarios registrados del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6b715-106">Retrieve a list of users that are registered users of the device.</span></span>

<span data-ttu-id="6b715-107">En el caso de los dispositivos unidos a la nube y los dispositivos personales registrados, los usuarios registrados se establecen en el mismo valor que los propietarios registrados en el momento del registro.</span><span class="sxs-lookup"><span data-stu-id="6b715-107">For cloud joined devices and registered personal devices, registered users are set to the same value as registered owners at the time of registration.</span></span>

## <a name="permissions"></a><span data-ttu-id="6b715-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="6b715-108">Permissions</span></span>
<span data-ttu-id="6b715-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6b715-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6b715-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6b715-111">Permission type</span></span>      | <span data-ttu-id="6b715-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6b715-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6b715-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6b715-113">Delegated (work or school account)</span></span> | <span data-ttu-id="6b715-114">Directory.Read.All o Directory.ReadWrite.All o Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="6b715-114">Directory.Read.All or Directory.ReadWrite.All or Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="6b715-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6b715-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6b715-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6b715-116">Not supported.</span></span> |
|<span data-ttu-id="6b715-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6b715-117">Application</span></span> | <span data-ttu-id="6b715-118">Directory.Read.All o Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6b715-118">Directory.Read.All or Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="6b715-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6b715-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /devices/{id}/registeredUsers
```

> <span data-ttu-id="6b715-120">Nota: El "id" de la solicitud es la propiedad "id" del dispositivo, no la propiedad "deviceId".</span><span class="sxs-lookup"><span data-stu-id="6b715-120">Note: The "id" in the request is the "id" property of the device, not the "deviceId" property.</span></span>

## <a name="optional-query-parameters"></a><span data-ttu-id="6b715-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="6b715-121">Optional query parameters</span></span>
<span data-ttu-id="6b715-122">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6b715-122">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="6b715-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6b715-123">Request headers</span></span>
| <span data-ttu-id="6b715-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="6b715-124">Name</span></span>       | <span data-ttu-id="6b715-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="6b715-125">Type</span></span> | <span data-ttu-id="6b715-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b715-126">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="6b715-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="6b715-127">Authorization</span></span>  | <span data-ttu-id="6b715-128">string</span><span class="sxs-lookup"><span data-stu-id="6b715-128">string</span></span>  | <span data-ttu-id="6b715-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6b715-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6b715-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6b715-131">Request body</span></span>
<span data-ttu-id="6b715-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6b715-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6b715-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6b715-133">Response</span></span>

<span data-ttu-id="6b715-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6b715-134">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6b715-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6b715-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6b715-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6b715-136">Request</span></span>
<span data-ttu-id="6b715-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6b715-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_registeredusers"
}-->
```http
GET https://graph.microsoft.com/beta/devices/{id}/registeredUsers
```
##### <a name="response"></a><span data-ttu-id="6b715-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6b715-138">Response</span></span>
<span data-ttu-id="6b715-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6b715-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 55

{
  "value": [
    {
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List registeredUsers",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
