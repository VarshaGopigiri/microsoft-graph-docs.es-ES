---
title: Miembro de lista grupo transitiva
description: Obtener grupos y unidades administrativas que el grupo es un miembro de.  Esta operación es transitiva y también incluirá todos los grupos que este grupo es un miembro anidado de. A diferencia de la introducción Office 365 grupos de un usuario, esto devuelve todos los tipos de grupos, no sólo Office 365 grupos.
ms.openlocfilehash: e622ee484a4070560c38528bccfe7f12e2172d54
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085616"
---
# <a name="list-group-transitive-memberof"></a><span data-ttu-id="540e7-105">Miembro de lista grupo transitiva</span><span class="sxs-lookup"><span data-stu-id="540e7-105">List group transitive memberOf</span></span>

> <span data-ttu-id="540e7-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="540e7-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="540e7-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="540e7-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="540e7-108">Obtener grupos y unidades administrativas que el grupo es un miembro de.</span><span class="sxs-lookup"><span data-stu-id="540e7-108">Get groups and administrative units that the group is a member of.</span></span>  <span data-ttu-id="540e7-109">Esta operación es transitiva y también incluirá todos los grupos que este grupo es un miembro anidado de.</span><span class="sxs-lookup"><span data-stu-id="540e7-109">This operation is transitive and will also include all groups that this groups is a nested member of.</span></span> <span data-ttu-id="540e7-110">A diferencia de la introducción Office 365 grupos de un usuario, esto devuelve todos los tipos de grupos, no sólo Office 365 grupos.</span><span class="sxs-lookup"><span data-stu-id="540e7-110">Unlike getting a user's Office 365 Groups, this returns all types of groups, not just Office 365 Groups.</span></span>

## <a name="permissions"></a><span data-ttu-id="540e7-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="540e7-111">Permissions</span></span>

<span data-ttu-id="540e7-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="540e7-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="540e7-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="540e7-114">Permission type</span></span>      | <span data-ttu-id="540e7-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="540e7-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="540e7-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="540e7-116">Delegated (work or school account)</span></span> | <span data-ttu-id="540e7-117">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="540e7-117">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="540e7-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="540e7-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="540e7-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="540e7-119">Not supported.</span></span>    |
|<span data-ttu-id="540e7-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="540e7-120">Application</span></span> | <span data-ttu-id="540e7-121">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="540e7-121">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="540e7-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="540e7-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/transitiveMemberOf
```

## <a name="optional-query-parameters"></a><span data-ttu-id="540e7-123">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="540e7-123">Optional query parameters</span></span>
<span data-ttu-id="540e7-124">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="540e7-124">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="540e7-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="540e7-125">Request headers</span></span>
| <span data-ttu-id="540e7-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="540e7-126">Name</span></span>       | <span data-ttu-id="540e7-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="540e7-127">Type</span></span> | <span data-ttu-id="540e7-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="540e7-128">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="540e7-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="540e7-129">Authorization</span></span>  | <span data-ttu-id="540e7-130">string</span><span class="sxs-lookup"><span data-stu-id="540e7-130">string</span></span>  | <span data-ttu-id="540e7-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="540e7-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="540e7-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="540e7-133">Request body</span></span>
<span data-ttu-id="540e7-134">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="540e7-134">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="540e7-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="540e7-135">Response</span></span>
<span data-ttu-id="540e7-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="540e7-136">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="540e7-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="540e7-137">Example</span></span>

### <a name="request"></a><span data-ttu-id="540e7-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="540e7-138">Request</span></span>
<span data-ttu-id="540e7-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="540e7-139">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_group_transitivememberof"
}-->

```http
GET https://graph.microsoft.com/beta/groups/{id}/transitiveMemberOf
```

### <a name="response"></a><span data-ttu-id="540e7-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="540e7-140">Response</span></span>

<span data-ttu-id="540e7-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="540e7-141">The following is an example of the response.</span></span>
><span data-ttu-id="540e7-142">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="540e7-142">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="540e7-143">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="540e7-143">All the properties will be returned from an actual call.</span></span>
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