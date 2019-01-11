---
title: List memberOf
description: 'Obtiene grupos de los que el grupo sea miembro directo. '
author: dkershaw10
localization_priority: Priority
ms.openlocfilehash: d7cfb9e21b05abc24b792e5e1288953c41492901
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27840295"
---
# <a name="list-memberof"></a><span data-ttu-id="bb9f5-103">List memberOf</span><span class="sxs-lookup"><span data-stu-id="bb9f5-103">List memberOf</span></span>
<span data-ttu-id="bb9f5-104">Obtiene grupos de los que el grupo sea miembro directo.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-104">Get groups that the group is a direct member of.</span></span> 

<span data-ttu-id="bb9f5-p101">Esta operación no es transitiva. A diferencia de la obtención de grupos de Office 365 de un usuario, devuelve todos los tipos de grupos, no solo los grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-p101">This operation is not transitive. Unlike getting a user's Office 365 Groups, this returns all types of groups, not just Office 365 groups.</span></span>

## <a name="permissions"></a><span data-ttu-id="bb9f5-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="bb9f5-107">Permissions</span></span>
<span data-ttu-id="bb9f5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bb9f5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bb9f5-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bb9f5-110">Permission type</span></span>      | <span data-ttu-id="bb9f5-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bb9f5-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bb9f5-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bb9f5-112">Delegated (work or school account)</span></span> | <span data-ttu-id="bb9f5-113">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="bb9f5-113">Group.Read.All</span></span>    |
|<span data-ttu-id="bb9f5-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bb9f5-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bb9f5-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-115">Not supported.</span></span>    |
|<span data-ttu-id="bb9f5-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bb9f5-116">Application</span></span> | <span data-ttu-id="bb9f5-117">Group.Read.All, Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="bb9f5-117">Group.Read.All, Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="bb9f5-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bb9f5-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/memberOf
```

## <a name="optional-query-parameters"></a><span data-ttu-id="bb9f5-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="bb9f5-119">Optional query parameters</span></span>
<span data-ttu-id="bb9f5-120">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-120">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="bb9f5-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bb9f5-121">Request headers</span></span>
| <span data-ttu-id="bb9f5-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="bb9f5-122">Name</span></span>       | <span data-ttu-id="bb9f5-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="bb9f5-123">Type</span></span> | <span data-ttu-id="bb9f5-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb9f5-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="bb9f5-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="bb9f5-125">Authorization</span></span>  | <span data-ttu-id="bb9f5-126">string</span><span class="sxs-lookup"><span data-stu-id="bb9f5-126">string</span></span>  | <span data-ttu-id="bb9f5-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="bb9f5-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bb9f5-129">Request body</span></span>
<span data-ttu-id="bb9f5-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bb9f5-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bb9f5-131">Response</span></span>
<span data-ttu-id="bb9f5-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-132">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bb9f5-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bb9f5-133">Example</span></span>
#### <a name="request"></a><span data-ttu-id="bb9f5-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bb9f5-134">Request</span></span>
<span data-ttu-id="bb9f5-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-135">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_memberof"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/memberOf
```

#### <a name="response"></a><span data-ttu-id="bb9f5-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bb9f5-136">Response</span></span>
<span data-ttu-id="bb9f5-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-137">The following is an example of the response.</span></span>
><span data-ttu-id="bb9f5-138">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-138">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="bb9f5-139">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bb9f5-139">All the properties will be returned from an actual call.</span></span>
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
  "description": "List memberOf",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
