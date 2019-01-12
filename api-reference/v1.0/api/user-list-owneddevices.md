---
title: List ownedDevices
description: Obtiene la lista de dispositivos que son propiedad del usuario.
author: dkershaw10
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 275e2869763e8cc25728e24c8046506891d2005f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27947459"
---
# <a name="list-owneddevices"></a><span data-ttu-id="2ee6e-103">List ownedDevices</span><span class="sxs-lookup"><span data-stu-id="2ee6e-103">List ownedDevices</span></span>

<span data-ttu-id="2ee6e-104">Obtiene la lista de dispositivos que son propiedad del usuario.</span><span class="sxs-lookup"><span data-stu-id="2ee6e-104">Get the list of devices that are owned by the user.</span></span>
## <a name="permissions"></a><span data-ttu-id="2ee6e-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="2ee6e-105">Permissions</span></span>
<span data-ttu-id="2ee6e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2ee6e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2ee6e-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2ee6e-108">Permission type</span></span>      | <span data-ttu-id="2ee6e-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2ee6e-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2ee6e-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2ee6e-110">Delegated (work or school account)</span></span> | <span data-ttu-id="2ee6e-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="2ee6e-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="2ee6e-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2ee6e-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2ee6e-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2ee6e-113">Not supported.</span></span>    |
|<span data-ttu-id="2ee6e-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2ee6e-114">Application</span></span> | <span data-ttu-id="2ee6e-115">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2ee6e-115">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="2ee6e-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2ee6e-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/ownedDevices
```
## <a name="optional-query-parameters"></a><span data-ttu-id="2ee6e-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="2ee6e-117">Optional query parameters</span></span>
<span data-ttu-id="2ee6e-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ee6e-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="2ee6e-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2ee6e-119">Request headers</span></span>
| <span data-ttu-id="2ee6e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ee6e-120">Header</span></span>       | <span data-ttu-id="2ee6e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2ee6e-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="2ee6e-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="2ee6e-122">Authorization</span></span>  | <span data-ttu-id="2ee6e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2ee6e-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="2ee6e-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="2ee6e-125">Accept</span></span>  | <span data-ttu-id="2ee6e-126">application/json</span><span class="sxs-lookup"><span data-stu-id="2ee6e-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2ee6e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2ee6e-127">Request body</span></span>
<span data-ttu-id="2ee6e-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2ee6e-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2ee6e-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2ee6e-129">Response</span></span>

<span data-ttu-id="2ee6e-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ee6e-130">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="2ee6e-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2ee6e-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2ee6e-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2ee6e-132">Request</span></span>
<span data-ttu-id="2ee6e-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2ee6e-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_owneddevices"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/ownedDevices
```
##### <a name="response"></a><span data-ttu-id="2ee6e-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2ee6e-134">Response</span></span>
<span data-ttu-id="2ee6e-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2ee6e-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "List ownedDevices",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
