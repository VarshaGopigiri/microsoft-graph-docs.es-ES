---
title: Enumerar propietarios
description: 'Recupera una lista de propietarios del grupo. Los propietarios son un conjunto de usuarios no administradores que tienen permiso para modificar el objeto de grupo. '
localization_priority: Priority
ms.openlocfilehash: a22e751d59d73b7bc3d3c00edafbce6c97f034f8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27814738"
---
# <a name="list-owners"></a><span data-ttu-id="34312-104">Enumerar propietarios</span><span class="sxs-lookup"><span data-stu-id="34312-104">List owners</span></span>
<span data-ttu-id="34312-p102">Recupera una lista de propietarios del grupo. Los propietarios son un conjunto de usuarios no administradores que tienen permiso para modificar el objeto de grupo.</span><span class="sxs-lookup"><span data-stu-id="34312-p102">Retrieve a list of the group's owners. The owners are a set of non-admin users who are allowed to modify the group object.</span></span> 

## <a name="permissions"></a><span data-ttu-id="34312-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="34312-107">Permissions</span></span>
<span data-ttu-id="34312-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="34312-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="34312-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="34312-110">Permission type</span></span>      | <span data-ttu-id="34312-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="34312-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="34312-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="34312-112">Delegated (work or school account)</span></span> | <span data-ttu-id="34312-113">Group.Read.All y User.ReadBasic.All, Group.Read.All y User.Read.All, Group.Read.All y User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="34312-113">Group.Read.All and User.ReadBasic.All, Group.Read.All and User.Read.All, Group.Read.All and User.ReadWrite.All</span></span>   |
|<span data-ttu-id="34312-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="34312-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="34312-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="34312-115">Not supported.</span></span>    |
|<span data-ttu-id="34312-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="34312-116">Application</span></span> | <span data-ttu-id="34312-117">Group.Read.All y User.Read.All, Group.Read.All y User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="34312-117">Group.Read.All and User.Read.All, Group.Read.All and User.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="34312-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="34312-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/owners
```

## <a name="optional-query-parameters"></a><span data-ttu-id="34312-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="34312-119">Optional query parameters</span></span>
<span data-ttu-id="34312-120">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="34312-120">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="34312-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="34312-121">Request headers</span></span>
| <span data-ttu-id="34312-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="34312-122">Name</span></span>       | <span data-ttu-id="34312-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="34312-123">Type</span></span> | <span data-ttu-id="34312-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="34312-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="34312-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="34312-125">Authorization</span></span>  | <span data-ttu-id="34312-126">string</span><span class="sxs-lookup"><span data-stu-id="34312-126">string</span></span>  | <span data-ttu-id="34312-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="34312-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="34312-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="34312-129">Request body</span></span>
<span data-ttu-id="34312-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="34312-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="34312-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34312-131">Response</span></span>
<span data-ttu-id="34312-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [user](../resources/user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="34312-132">If successful, this method returns a `200 OK` response code and collection of [user](../resources/user.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="34312-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="34312-133">Example</span></span>
#### <a name="request"></a><span data-ttu-id="34312-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="34312-134">Request</span></span>
<span data-ttu-id="34312-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="34312-135">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_owners"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/owners
```

#### <a name="response"></a><span data-ttu-id="34312-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34312-136">Response</span></span>
<span data-ttu-id="34312-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="34312-137">The following is an example of the response.</span></span>
><span data-ttu-id="34312-138">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="34312-138">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="34312-139">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="34312-139">All the properties will be returned from an actual call.</span></span>
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
      "@odata.type": "#microsoft.graph.user"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List owners",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
