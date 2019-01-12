---
title: Miembro de lista grupo transitiva
description: Obtener grupos y unidades administrativas que el grupo es un miembro de.  Esta operación es transitiva y también incluirá todos los grupos que este grupo es un miembro anidado de. A diferencia de la introducción Office 365 grupos de un usuario, esto devuelve todos los tipos de grupos, no sólo Office 365 grupos.
localization_priority: Normal
author: dkershaw10
ms.prod: groups
ms.openlocfilehash: ec03ca6fce354f2a0b81cf0f81bf3061db504365
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27921671"
---
# <a name="list-group-transitive-memberof"></a><span data-ttu-id="eced1-105">Miembro de lista grupo transitiva</span><span class="sxs-lookup"><span data-stu-id="eced1-105">List group transitive memberOf</span></span>

> <span data-ttu-id="eced1-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="eced1-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="eced1-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="eced1-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="eced1-108">Obtener grupos y unidades administrativas que el grupo es un miembro de.</span><span class="sxs-lookup"><span data-stu-id="eced1-108">Get groups and administrative units that the group is a member of.</span></span>  <span data-ttu-id="eced1-109">Esta operación es transitiva y también incluirá todos los grupos que este grupo es un miembro anidado de.</span><span class="sxs-lookup"><span data-stu-id="eced1-109">This operation is transitive and will also include all groups that this groups is a nested member of.</span></span> <span data-ttu-id="eced1-110">A diferencia de la introducción Office 365 grupos de un usuario, esto devuelve todos los tipos de grupos, no sólo Office 365 grupos.</span><span class="sxs-lookup"><span data-stu-id="eced1-110">Unlike getting a user's Office 365 Groups, this returns all types of groups, not just Office 365 Groups.</span></span>

## <a name="permissions"></a><span data-ttu-id="eced1-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="eced1-111">Permissions</span></span>

<span data-ttu-id="eced1-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="eced1-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="eced1-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eced1-114">Permission type</span></span>      | <span data-ttu-id="eced1-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eced1-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="eced1-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eced1-116">Delegated (work or school account)</span></span> | <span data-ttu-id="eced1-117">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="eced1-117">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="eced1-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eced1-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="eced1-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eced1-119">Not supported.</span></span>    |
|<span data-ttu-id="eced1-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eced1-120">Application</span></span> | <span data-ttu-id="eced1-121">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="eced1-121">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="eced1-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eced1-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/transitiveMemberOf
```

## <a name="optional-query-parameters"></a><span data-ttu-id="eced1-123">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="eced1-123">Optional query parameters</span></span>
<span data-ttu-id="eced1-124">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eced1-124">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="eced1-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eced1-125">Request headers</span></span>
| <span data-ttu-id="eced1-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="eced1-126">Name</span></span>       | <span data-ttu-id="eced1-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="eced1-127">Type</span></span> | <span data-ttu-id="eced1-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="eced1-128">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="eced1-129">Autorización</span><span class="sxs-lookup"><span data-stu-id="eced1-129">Authorization</span></span>  | <span data-ttu-id="eced1-130">string</span><span class="sxs-lookup"><span data-stu-id="eced1-130">string</span></span>  | <span data-ttu-id="eced1-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="eced1-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="eced1-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eced1-133">Request body</span></span>
<span data-ttu-id="eced1-134">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="eced1-134">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="eced1-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eced1-135">Response</span></span>
<span data-ttu-id="eced1-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eced1-136">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="eced1-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eced1-137">Example</span></span>

### <a name="request"></a><span data-ttu-id="eced1-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eced1-138">Request</span></span>
<span data-ttu-id="eced1-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eced1-139">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_group_transitivememberof"
}-->

```http
GET https://graph.microsoft.com/beta/groups/{id}/transitiveMemberOf
```

### <a name="response"></a><span data-ttu-id="eced1-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eced1-140">Response</span></span>

<span data-ttu-id="eced1-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eced1-141">The following is an example of the response.</span></span>
><span data-ttu-id="eced1-142">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="eced1-142">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="eced1-143">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="eced1-143">All the properties will be returned from an actual call.</span></span>
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
  "description": "List group transitive memberOf",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
