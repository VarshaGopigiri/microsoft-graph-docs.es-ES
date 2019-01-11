---
title: Obtener sectionGroup
description: Recupera las propiedades y relaciones de un objeto sectionGroup.
localization_priority: Normal
ms.openlocfilehash: b574c1a0cdfe8b615e24a7cf44a438c3eec139d4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27871760"
---
# <a name="get-sectiongroup"></a><span data-ttu-id="573c8-103">Obtener sectionGroup</span><span class="sxs-lookup"><span data-stu-id="573c8-103">Get sectionGroup</span></span>

<span data-ttu-id="573c8-104">Recupera las propiedades y relaciones de un objeto [sectionGroup](../resources/sectiongroup.md).</span><span class="sxs-lookup"><span data-stu-id="573c8-104">Retrieve the properties and relationships of a [sectionGroup](../resources/sectiongroup.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="573c8-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="573c8-105">Permissions</span></span>
<span data-ttu-id="573c8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="573c8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="573c8-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="573c8-108">Permission type</span></span>      | <span data-ttu-id="573c8-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="573c8-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="573c8-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="573c8-110">Delegated (work or school account)</span></span> | <span data-ttu-id="573c8-111">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="573c8-111">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="573c8-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="573c8-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="573c8-113">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="573c8-113">Notes.Create, Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="573c8-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="573c8-114">Application</span></span> | <span data-ttu-id="573c8-115">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="573c8-115">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="573c8-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="573c8-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/sectionGroups/{id}
GET /users/{id | userPrincipalName}/onenote/sectionGroups/{id}
GET /groups/{id}/onenote/sectionGroups/{id}
GET /sites/{id}/onenote/sectionGroups/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="573c8-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="573c8-117">Optional query parameters</span></span>
<span data-ttu-id="573c8-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="573c8-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="573c8-p102">La consulta predeterminada expande `parentNotebook` y selecciona sus propiedades `id`, `name` y `self`. Los valores válidos de `expand` de los grupos de secciones son `parentNotebook` y `parentSectionGroup`.</span><span class="sxs-lookup"><span data-stu-id="573c8-p102">The default query expands `parentNotebook` and selects its `id`, `name`, and `self` properties. Valid `expand` values for section groups are `parentNotebook` and `parentSectionGroup`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="573c8-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="573c8-121">Request headers</span></span>
| <span data-ttu-id="573c8-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="573c8-122">Name</span></span>       | <span data-ttu-id="573c8-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="573c8-123">Type</span></span> | <span data-ttu-id="573c8-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="573c8-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="573c8-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="573c8-125">Authorization</span></span>  | <span data-ttu-id="573c8-126">string</span><span class="sxs-lookup"><span data-stu-id="573c8-126">string</span></span>  | <span data-ttu-id="573c8-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="573c8-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="573c8-129">Aceptar</span><span class="sxs-lookup"><span data-stu-id="573c8-129">Accept</span></span> | <span data-ttu-id="573c8-130">string</span><span class="sxs-lookup"><span data-stu-id="573c8-130">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="573c8-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="573c8-131">Request body</span></span>
<span data-ttu-id="573c8-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="573c8-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="573c8-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="573c8-133">Response</span></span>

<span data-ttu-id="573c8-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [sectionGroup](../resources/sectiongroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="573c8-134">If successful, this method returns a `200 OK` response code and a [sectionGroup](../resources/sectiongroup.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="573c8-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="573c8-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="573c8-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="573c8-136">Request</span></span>
<span data-ttu-id="573c8-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="573c8-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_sectiongroup"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/sectionGroups/{id}
```
##### <a name="response"></a><span data-ttu-id="573c8-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="573c8-138">Response</span></span>
<span data-ttu-id="573c8-p104">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="573c8-p104">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.sectionGroup"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 305

{
  "sectionsUrl": "sectionsUrl-value",
  "sectionGroupsUrl": "sectionGroupsUrl-value",
  "displayName": "name-value",  
  "createdBy": {
    "user": {
      "id": "id-value",
      "displayName": "displayName-value"
    }
  },
  "lastModifiedBy": {
    "user": {
      "id": "id-value",
      "displayName": "displayName-value"
    }
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get sectionGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
