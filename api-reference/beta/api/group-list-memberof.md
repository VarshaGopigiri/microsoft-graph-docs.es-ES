---
title: Miembro del grupo de lista
description: Obtener grupos y unidades administrativas que el grupo es miembro directo.
ms.openlocfilehash: 5c189571095676d0c52b8bb93a8d27136d4aaa3c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086158"
---
# <a name="list-group-memberof"></a><span data-ttu-id="cb443-103">Miembro del grupo de lista</span><span class="sxs-lookup"><span data-stu-id="cb443-103">List group memberOf</span></span>

> <span data-ttu-id="cb443-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cb443-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cb443-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cb443-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="cb443-106">Obtener grupos y unidades administrativas que el grupo es miembro directo.</span><span class="sxs-lookup"><span data-stu-id="cb443-106">Get groups and administrative units that the group is a direct member of.</span></span>

<span data-ttu-id="cb443-107">Esta operación no es transitiva.</span><span class="sxs-lookup"><span data-stu-id="cb443-107">This operation is not transitive.</span></span> <span data-ttu-id="cb443-108">A diferencia de la introducción Office 365 grupos de un usuario, esto devuelve todos los tipos de grupos, no sólo Office 365 grupos.</span><span class="sxs-lookup"><span data-stu-id="cb443-108">Unlike getting a user's Office 365 Groups, this returns all types of groups, not just Office 365 Groups.</span></span> 

## <a name="permissions"></a><span data-ttu-id="cb443-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="cb443-109">Permissions</span></span>

<span data-ttu-id="cb443-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cb443-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cb443-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cb443-112">Permission type</span></span>      | <span data-ttu-id="cb443-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cb443-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="cb443-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cb443-114">Delegated (work or school account)</span></span> | <span data-ttu-id="cb443-115">Group.Read.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="cb443-115">Group.Read.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="cb443-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cb443-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cb443-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cb443-117">Not supported.</span></span>    |
|<span data-ttu-id="cb443-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cb443-118">Application</span></span> | <span data-ttu-id="cb443-119">Group.Read.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cb443-119">Group.Read.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="cb443-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cb443-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/memberOf
```

## <a name="optional-query-parameters"></a><span data-ttu-id="cb443-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="cb443-121">Optional query parameters</span></span>
<span data-ttu-id="cb443-122">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cb443-122">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="cb443-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cb443-123">Request headers</span></span>
| <span data-ttu-id="cb443-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="cb443-124">Name</span></span>       | <span data-ttu-id="cb443-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="cb443-125">Type</span></span> | <span data-ttu-id="cb443-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="cb443-126">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="cb443-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="cb443-127">Authorization</span></span>  | <span data-ttu-id="cb443-128">string</span><span class="sxs-lookup"><span data-stu-id="cb443-128">string</span></span>  | <span data-ttu-id="cb443-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cb443-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="cb443-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cb443-131">Request body</span></span>
<span data-ttu-id="cb443-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="cb443-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="cb443-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cb443-133">Response</span></span>
<span data-ttu-id="cb443-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cb443-134">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cb443-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cb443-135">Example</span></span>

### <a name="request"></a><span data-ttu-id="cb443-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cb443-136">Request</span></span>

<span data-ttu-id="cb443-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cb443-137">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_memberof"
}-->
```http
GET https://graph.microsoft.com/beta/groups/{id}/memberOf
```

### <a name="response"></a><span data-ttu-id="cb443-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cb443-138">Response</span></span>

<span data-ttu-id="cb443-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cb443-139">The following is an example of the response.</span></span>
><span data-ttu-id="cb443-140">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="cb443-140">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="cb443-141">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cb443-141">All the properties will be returned from an actual call.</span></span>
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