---
title: List ownedObjects
description: Obtiene la lista de objetos de directorio que son propiedad del usuario.
author: dkershaw10
localization_priority: Normal
ms.openlocfilehash: fc9a39ef672d62cb0f68a8cca09aecf8d6507b90
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27811504"
---
# <a name="list-ownedobjects"></a><span data-ttu-id="3af19-103">List ownedObjects</span><span class="sxs-lookup"><span data-stu-id="3af19-103">List ownedObjects</span></span>

<span data-ttu-id="3af19-104">Obtiene la lista de objetos de directorio que son propiedad del usuario.</span><span class="sxs-lookup"><span data-stu-id="3af19-104">Get the list of directory objects that are owned by the user.</span></span>
## <a name="permissions"></a><span data-ttu-id="3af19-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="3af19-105">Permissions</span></span>
<span data-ttu-id="3af19-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3af19-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3af19-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3af19-108">Permission type</span></span>      | <span data-ttu-id="3af19-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3af19-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3af19-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3af19-110">Delegated (work or school account)</span></span> | <span data-ttu-id="3af19-111">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="3af19-111">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="3af19-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3af19-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3af19-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3af19-113">Not supported.</span></span>    |
|<span data-ttu-id="3af19-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3af19-114">Application</span></span> | <span data-ttu-id="3af19-115">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3af19-115">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="3af19-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3af19-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/ownedObjects
```
## <a name="optional-query-parameters"></a><span data-ttu-id="3af19-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="3af19-117">Optional query parameters</span></span>
<span data-ttu-id="3af19-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3af19-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="3af19-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3af19-119">Request headers</span></span>
| <span data-ttu-id="3af19-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3af19-120">Header</span></span>       | <span data-ttu-id="3af19-121">Valor</span><span class="sxs-lookup"><span data-stu-id="3af19-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="3af19-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="3af19-122">Authorization</span></span>  | <span data-ttu-id="3af19-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3af19-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="3af19-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="3af19-125">Accept</span></span>  | <span data-ttu-id="3af19-126">application/json</span><span class="sxs-lookup"><span data-stu-id="3af19-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3af19-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3af19-127">Request body</span></span>
<span data-ttu-id="3af19-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3af19-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3af19-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3af19-129">Response</span></span>

<span data-ttu-id="3af19-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3af19-130">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="3af19-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3af19-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3af19-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3af19-132">Request</span></span>
<span data-ttu-id="3af19-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3af19-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_ownedobjects"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/ownedObjects
```
##### <a name="response"></a><span data-ttu-id="3af19-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3af19-134">Response</span></span>
<span data-ttu-id="3af19-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3af19-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
