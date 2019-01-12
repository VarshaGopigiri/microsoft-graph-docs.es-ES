---
title: Obtener sectionGroup
description: Recupera las propiedades y relaciones de un objeto sectionGroup.
localization_priority: Normal
author: jewan-microsoft
ms.prod: onenote
ms.openlocfilehash: 81b838d01517d219fdb3375140092bf44f58f793
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27953297"
---
# <a name="get-sectiongroup"></a><span data-ttu-id="9d14b-103">Obtener sectionGroup</span><span class="sxs-lookup"><span data-stu-id="9d14b-103">Get sectionGroup</span></span>

> <span data-ttu-id="9d14b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9d14b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9d14b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9d14b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9d14b-106">Recupera las propiedades y relaciones de un objeto [sectionGroup](../resources/sectiongroup.md).</span><span class="sxs-lookup"><span data-stu-id="9d14b-106">Retrieve the properties and relationships of a [sectionGroup](../resources/sectiongroup.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="9d14b-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="9d14b-107">Permissions</span></span>
<span data-ttu-id="9d14b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9d14b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9d14b-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9d14b-110">Permission type</span></span>      | <span data-ttu-id="9d14b-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9d14b-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9d14b-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9d14b-112">Delegated (work or school account)</span></span> | <span data-ttu-id="9d14b-113">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9d14b-113">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="9d14b-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9d14b-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9d14b-115">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9d14b-115">Notes.Create, Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="9d14b-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9d14b-116">Application</span></span> | <span data-ttu-id="9d14b-117">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9d14b-117">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="9d14b-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9d14b-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/sectionGroups/{id}
GET /users/{id | userPrincipalName}/onenote/sectionGroups/{id}
GET /groups/{id}/onenote/sectionGroups/{id}
GET /sites/{id}/onenote/sectionGroups/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="9d14b-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="9d14b-119">Optional query parameters</span></span>
<span data-ttu-id="9d14b-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9d14b-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="9d14b-p103">La consulta predeterminada expande `parentNotebook` y selecciona sus propiedades `id`, `name` y `self`. Los valores válidos de `expand` de los grupos de secciones son `parentNotebook` y `parentSectionGroup`.</span><span class="sxs-lookup"><span data-stu-id="9d14b-p103">The default query expands `parentNotebook` and selects its `id`, `name`, and `self` properties. Valid `expand` values for section groups are `parentNotebook` and `parentSectionGroup`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="9d14b-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9d14b-123">Request headers</span></span>
| <span data-ttu-id="9d14b-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="9d14b-124">Name</span></span>       | <span data-ttu-id="9d14b-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="9d14b-125">Type</span></span> | <span data-ttu-id="9d14b-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d14b-126">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="9d14b-127">Autorización</span><span class="sxs-lookup"><span data-stu-id="9d14b-127">Authorization</span></span>  | <span data-ttu-id="9d14b-128">string</span><span class="sxs-lookup"><span data-stu-id="9d14b-128">string</span></span>  | <span data-ttu-id="9d14b-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9d14b-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="9d14b-131">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9d14b-131">Accept</span></span> | <span data-ttu-id="9d14b-132">string</span><span class="sxs-lookup"><span data-stu-id="9d14b-132">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="9d14b-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9d14b-133">Request body</span></span>
<span data-ttu-id="9d14b-134">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9d14b-134">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9d14b-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9d14b-135">Response</span></span>

<span data-ttu-id="9d14b-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [sectionGroup](../resources/sectiongroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9d14b-136">If successful, this method returns a `200 OK` response code and a [sectionGroup](../resources/sectiongroup.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="9d14b-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9d14b-137">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9d14b-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9d14b-138">Request</span></span>
<span data-ttu-id="9d14b-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9d14b-139">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_sectiongroup"
}-->
```http
GET https://graph.microsoft.com/beta/me/onenote/sectionGroups/{id}
```
##### <a name="response"></a><span data-ttu-id="9d14b-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9d14b-140">Response</span></span>
<span data-ttu-id="9d14b-p105">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9d14b-p105">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.sectiongroup"
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
