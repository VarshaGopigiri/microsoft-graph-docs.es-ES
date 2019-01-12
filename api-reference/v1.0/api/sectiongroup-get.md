---
title: Obtener sectionGroup
description: Recupera las propiedades y relaciones de un objeto sectionGroup.
localization_priority: Normal
author: jewan-microsoft
ms.prod: onenote
ms.openlocfilehash: d5b86daa6ad8fb9aaaed5b72d60e2fa5665a1648
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27919381"
---
# <a name="get-sectiongroup"></a><span data-ttu-id="397d1-103">Obtener sectionGroup</span><span class="sxs-lookup"><span data-stu-id="397d1-103">Get sectionGroup</span></span>

<span data-ttu-id="397d1-104">Recupera las propiedades y relaciones de un objeto [sectionGroup](../resources/sectiongroup.md).</span><span class="sxs-lookup"><span data-stu-id="397d1-104">Retrieve the properties and relationships of a [sectionGroup](../resources/sectiongroup.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="397d1-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="397d1-105">Permissions</span></span>
<span data-ttu-id="397d1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="397d1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="397d1-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="397d1-108">Permission type</span></span>      | <span data-ttu-id="397d1-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="397d1-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="397d1-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="397d1-110">Delegated (work or school account)</span></span> | <span data-ttu-id="397d1-111">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="397d1-111">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="397d1-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="397d1-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="397d1-113">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="397d1-113">Notes.Create, Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="397d1-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="397d1-114">Application</span></span> | <span data-ttu-id="397d1-115">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="397d1-115">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="397d1-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="397d1-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/sectionGroups/{id}
GET /users/{id | userPrincipalName}/onenote/sectionGroups/{id}
GET /groups/{id}/onenote/sectionGroups/{id}
GET /sites/{id}/onenote/sectionGroups/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="397d1-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="397d1-117">Optional query parameters</span></span>
<span data-ttu-id="397d1-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="397d1-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="397d1-p102">La consulta predeterminada expande `parentNotebook` y selecciona sus propiedades `id`, `name` y `self`. Los valores válidos de `expand` de los grupos de secciones son `parentNotebook` y `parentSectionGroup`.</span><span class="sxs-lookup"><span data-stu-id="397d1-p102">The default query expands `parentNotebook` and selects its `id`, `name`, and `self` properties. Valid `expand` values for section groups are `parentNotebook` and `parentSectionGroup`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="397d1-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="397d1-121">Request headers</span></span>
| <span data-ttu-id="397d1-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="397d1-122">Name</span></span>       | <span data-ttu-id="397d1-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="397d1-123">Type</span></span> | <span data-ttu-id="397d1-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="397d1-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="397d1-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="397d1-125">Authorization</span></span>  | <span data-ttu-id="397d1-126">string</span><span class="sxs-lookup"><span data-stu-id="397d1-126">string</span></span>  | <span data-ttu-id="397d1-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="397d1-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="397d1-129">Aceptar</span><span class="sxs-lookup"><span data-stu-id="397d1-129">Accept</span></span> | <span data-ttu-id="397d1-130">string</span><span class="sxs-lookup"><span data-stu-id="397d1-130">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="397d1-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="397d1-131">Request body</span></span>
<span data-ttu-id="397d1-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="397d1-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="397d1-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="397d1-133">Response</span></span>

<span data-ttu-id="397d1-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [sectionGroup](../resources/sectiongroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="397d1-134">If successful, this method returns a `200 OK` response code and a [sectionGroup](../resources/sectiongroup.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="397d1-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="397d1-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="397d1-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="397d1-136">Request</span></span>
<span data-ttu-id="397d1-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="397d1-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_sectiongroup"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/sectionGroups/{id}
```
##### <a name="response"></a><span data-ttu-id="397d1-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="397d1-138">Response</span></span>
<span data-ttu-id="397d1-p104">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="397d1-p104">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
