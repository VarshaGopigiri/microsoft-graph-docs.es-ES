---
title: Grupos de dispositivos de la lista
description: Obtener los grupos a los que este dispositivo es miembro directo. Esta operación no es transitiva.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 1642b6ee758af5d2ab4004ea5b7a5293f33f7d01
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27912382"
---
# <a name="list-device-groups"></a><span data-ttu-id="dacce-104">Grupos de dispositivos de la lista</span><span class="sxs-lookup"><span data-stu-id="dacce-104">List device groups</span></span>

<span data-ttu-id="dacce-105">Obtener los grupos a los que este dispositivo es miembro directo.</span><span class="sxs-lookup"><span data-stu-id="dacce-105">Get groups that this device is a direct member of.</span></span> <span data-ttu-id="dacce-106">Esta operación no es transitiva.</span><span class="sxs-lookup"><span data-stu-id="dacce-106">This operation is not transitive.</span></span>

## <a name="permissions"></a><span data-ttu-id="dacce-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="dacce-107">Permissions</span></span>

<span data-ttu-id="dacce-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dacce-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dacce-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dacce-110">Permission type</span></span>      | <span data-ttu-id="dacce-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dacce-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="dacce-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dacce-112">Delegated (work or school account)</span></span> | <span data-ttu-id="dacce-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="dacce-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="dacce-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dacce-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dacce-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dacce-115">Not supported.</span></span>    |
|<span data-ttu-id="dacce-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dacce-116">Application</span></span> | <span data-ttu-id="dacce-117">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dacce-117">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="dacce-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dacce-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /devices/{id}/memberOf
```
## <a name="optional-query-parameters"></a><span data-ttu-id="dacce-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="dacce-119">Optional query parameters</span></span>
<span data-ttu-id="dacce-120">Este método admite los [parámetros de consulta de OData](/graph/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dacce-120">This method supports the [OData Query Parameters](/graph/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="dacce-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dacce-121">Request headers</span></span>
| <span data-ttu-id="dacce-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dacce-122">Header</span></span>       | <span data-ttu-id="dacce-123">Valor</span><span class="sxs-lookup"><span data-stu-id="dacce-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="dacce-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="dacce-124">Authorization</span></span>  | <span data-ttu-id="dacce-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dacce-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="dacce-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="dacce-127">Accept</span></span>  | <span data-ttu-id="dacce-128">application/json</span><span class="sxs-lookup"><span data-stu-id="dacce-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="dacce-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dacce-129">Request body</span></span>
<span data-ttu-id="dacce-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="dacce-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="dacce-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dacce-131">Response</span></span>

<span data-ttu-id="dacce-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dacce-132">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="dacce-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dacce-133">Example</span></span>

### <a name="request"></a><span data-ttu-id="dacce-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dacce-134">Request</span></span>

<span data-ttu-id="dacce-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dacce-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_user_memberof"
}-->
```http
GET https://graph.microsoft.com/v1.0/devices/{id}/memberOf
```

### <a name="response"></a><span data-ttu-id="dacce-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dacce-136">Response</span></span>
<span data-ttu-id="dacce-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dacce-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.group",
      "id": "id-value",
      "createdDateTime": null,
      "description": "All users at the company",
      "displayName": "All Users",
      "groupTypes": [],
      "mailEnabled": false,
      "securityEnabled": true,
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List memberOf",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
