---
title: Enumerar miembros
description: Obtener una lista de los miembros del grupo directa. Un grupo puede tener los usuarios, contactos y otros grupos como miembros.
ms.openlocfilehash: d9e756ecdbedbd17a446b27d33d3fafc23822636
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030024"
---
# <a name="list-members"></a><span data-ttu-id="a0e60-104">Enumerar miembros</span><span class="sxs-lookup"><span data-stu-id="a0e60-104">List members</span></span>
<span data-ttu-id="a0e60-p102">Obtiene una lista de los miembros directos del grupo. Un grupo puede tener usuarios, contactos y otros grupos como miembros. Esta operación no es transitiva.</span><span class="sxs-lookup"><span data-stu-id="a0e60-p102">Get a list of the group's direct members. A group can have users, contacts, and other groups as members. This operation is not transitive.</span></span>

## <a name="permissions"></a><span data-ttu-id="a0e60-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="a0e60-108">Permissions</span></span>
<span data-ttu-id="a0e60-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a0e60-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a0e60-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a0e60-111">Permission type</span></span>      | <span data-ttu-id="a0e60-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a0e60-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a0e60-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a0e60-113">Delegated (work or school account)</span></span> | <span data-ttu-id="a0e60-114">User.ReadBasic.All, User.Read.All, Directory.Read.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="a0e60-114">User.ReadBasic.All, User.Read.All, Directory.Read.All, Directory.AccessAsUser.All</span></span>   |
|<span data-ttu-id="a0e60-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a0e60-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a0e60-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a0e60-116">Not supported.</span></span>    |
|<span data-ttu-id="a0e60-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a0e60-117">Application</span></span> | <span data-ttu-id="a0e60-118">User.Read.All, Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="a0e60-118">User.Read.All, Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="a0e60-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a0e60-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/members
```

## <a name="optional-query-parameters"></a><span data-ttu-id="a0e60-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a0e60-120">Optional query parameters</span></span>
<span data-ttu-id="a0e60-121">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a0e60-121">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a0e60-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a0e60-122">Request headers</span></span>
| <span data-ttu-id="a0e60-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="a0e60-123">Name</span></span>       | <span data-ttu-id="a0e60-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="a0e60-124">Type</span></span> | <span data-ttu-id="a0e60-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0e60-125">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="a0e60-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="a0e60-126">Authorization</span></span>  | <span data-ttu-id="a0e60-127">string</span><span class="sxs-lookup"><span data-stu-id="a0e60-127">string</span></span>  | <span data-ttu-id="a0e60-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a0e60-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a0e60-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a0e60-130">Request body</span></span>
<span data-ttu-id="a0e60-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a0e60-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a0e60-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a0e60-132">Response</span></span>
<span data-ttu-id="a0e60-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a0e60-133">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a0e60-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a0e60-134">Example</span></span>
#### <a name="request"></a><span data-ttu-id="a0e60-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a0e60-135">Request</span></span>
<span data-ttu-id="a0e60-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a0e60-136">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_members"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/members
```

#### <a name="response"></a><span data-ttu-id="a0e60-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a0e60-137">Response</span></span>
<span data-ttu-id="a0e60-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a0e60-138">The following is an example of the response.</span></span>
><span data-ttu-id="a0e60-139">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="a0e60-139">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="a0e60-140">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a0e60-140">All the properties will be returned from an actual call.</span></span>
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
  "description": "List members",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->