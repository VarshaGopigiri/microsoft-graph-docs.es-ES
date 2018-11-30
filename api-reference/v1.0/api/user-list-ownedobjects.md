---
title: List ownedObjects
description: Obtiene la lista de objetos de directorio que son propiedad del usuario.
ms.openlocfilehash: d88340f26f3243d14fd89aa049888b2ff7ca87e9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028825"
---
# <a name="list-ownedobjects"></a><span data-ttu-id="52540-103">List ownedObjects</span><span class="sxs-lookup"><span data-stu-id="52540-103">List ownedObjects</span></span>

<span data-ttu-id="52540-104">Obtiene la lista de objetos de directorio que son propiedad del usuario.</span><span class="sxs-lookup"><span data-stu-id="52540-104">Get the list of directory objects that are owned by the user.</span></span>
## <a name="permissions"></a><span data-ttu-id="52540-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="52540-105">Permissions</span></span>
<span data-ttu-id="52540-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="52540-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="52540-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="52540-108">Permission type</span></span>      | <span data-ttu-id="52540-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="52540-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="52540-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="52540-110">Delegated (work or school account)</span></span> | <span data-ttu-id="52540-111">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="52540-111">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="52540-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="52540-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="52540-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="52540-113">Not supported.</span></span>    |
|<span data-ttu-id="52540-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="52540-114">Application</span></span> | <span data-ttu-id="52540-115">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="52540-115">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="52540-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="52540-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/ownedObjects
```
## <a name="optional-query-parameters"></a><span data-ttu-id="52540-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="52540-117">Optional query parameters</span></span>
<span data-ttu-id="52540-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="52540-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="52540-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="52540-119">Request headers</span></span>
| <span data-ttu-id="52540-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52540-120">Header</span></span>       | <span data-ttu-id="52540-121">Valor</span><span class="sxs-lookup"><span data-stu-id="52540-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="52540-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="52540-122">Authorization</span></span>  | <span data-ttu-id="52540-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="52540-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="52540-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="52540-125">Accept</span></span>  | <span data-ttu-id="52540-126">application/json</span><span class="sxs-lookup"><span data-stu-id="52540-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="52540-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="52540-127">Request body</span></span>
<span data-ttu-id="52540-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="52540-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="52540-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="52540-129">Response</span></span>

<span data-ttu-id="52540-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="52540-130">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="52540-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="52540-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="52540-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="52540-132">Request</span></span>
<span data-ttu-id="52540-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="52540-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_ownedobjects"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/ownedObjects
```
##### <a name="response"></a><span data-ttu-id="52540-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="52540-134">Response</span></span>
<span data-ttu-id="52540-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="52540-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "List ownedObjects",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->