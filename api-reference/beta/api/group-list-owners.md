---
title: Enumerar propietarios
description: Recupera una lista de propietarios del grupo. Los propietarios son un conjunto de usuarios no administradores que tienen permiso para modificar el objeto de grupo.
ms.openlocfilehash: 2b3584e5037c9ac36ac4bff97ef64af21643eb31
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090417"
---
# <a name="list-owners"></a><span data-ttu-id="611e6-104">Enumerar propietarios</span><span class="sxs-lookup"><span data-stu-id="611e6-104">List owners</span></span>

> <span data-ttu-id="611e6-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="611e6-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="611e6-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="611e6-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="611e6-p103">Recupera una lista de propietarios del grupo. Los propietarios son un conjunto de usuarios no administradores que tienen permiso para modificar el objeto de grupo.</span><span class="sxs-lookup"><span data-stu-id="611e6-p103">Retrieve a list of the group's owners. The owners are a set of non-admin users who are allowed to modify the group object.</span></span>

## <a name="permissions"></a><span data-ttu-id="611e6-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="611e6-109">Permissions</span></span>
<span data-ttu-id="611e6-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="611e6-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="611e6-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="611e6-112">Permission type</span></span>      | <span data-ttu-id="611e6-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="611e6-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="611e6-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="611e6-114">Delegated (work or school account)</span></span> | <span data-ttu-id="611e6-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="611e6-115">Not supported.</span></span>    |
|<span data-ttu-id="611e6-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="611e6-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="611e6-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="611e6-117">Not supported.</span></span>    |
|<span data-ttu-id="611e6-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="611e6-118">Application</span></span> | <span data-ttu-id="611e6-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="611e6-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="611e6-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="611e6-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/owners
```

## <a name="optional-query-parameters"></a><span data-ttu-id="611e6-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="611e6-121">Optional query parameters</span></span>
<span data-ttu-id="611e6-122">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="611e6-122">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="611e6-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="611e6-123">Request headers</span></span>
| <span data-ttu-id="611e6-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="611e6-124">Name</span></span>       | <span data-ttu-id="611e6-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="611e6-125">Type</span></span> | <span data-ttu-id="611e6-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="611e6-126">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="611e6-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="611e6-127">Authorization</span></span>  | <span data-ttu-id="611e6-128">string</span><span class="sxs-lookup"><span data-stu-id="611e6-128">string</span></span>  | <span data-ttu-id="611e6-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="611e6-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="611e6-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="611e6-131">Request body</span></span>
<span data-ttu-id="611e6-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="611e6-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="611e6-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="611e6-133">Response</span></span>
<span data-ttu-id="611e6-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="611e6-134">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="611e6-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="611e6-135">Example</span></span>
#### <a name="request"></a><span data-ttu-id="611e6-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="611e6-136">Request</span></span>
<span data-ttu-id="611e6-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="611e6-137">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_owners"
}-->
```http
GET https://graph.microsoft.com/beta/groups/{id}/owners
```

#### <a name="response"></a><span data-ttu-id="611e6-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="611e6-138">Response</span></span>
<span data-ttu-id="611e6-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="611e6-139">The following is an example of the response.</span></span>
><span data-ttu-id="611e6-140">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="611e6-140">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="611e6-141">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="611e6-141">All the properties will be returned from an actual call.</span></span>
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
  "description": "List owners",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->