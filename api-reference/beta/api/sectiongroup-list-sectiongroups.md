---
title: Enumerar sectionGroups
description: Recupera una lista de grupos de sección desde el grupo de sección especificado.
ms.openlocfilehash: 670adab5b8daf9a846aea06a8dfecea0a4ee07b3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087906"
---
# <a name="list-sectiongroups"></a><span data-ttu-id="5a3ef-103">Enumerar sectionGroups</span><span class="sxs-lookup"><span data-stu-id="5a3ef-103">List sectionGroups</span></span>

> <span data-ttu-id="5a3ef-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5a3ef-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5a3ef-106">Recupera una lista de [grupos de sección](../resources/sectiongroup.md) desde el grupo de sección especificado.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-106">Retrieve a list of [section groups](../resources/sectiongroup.md) from the specified section group.</span></span>
## <a name="permissions"></a><span data-ttu-id="5a3ef-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="5a3ef-107">Permissions</span></span>
<span data-ttu-id="5a3ef-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5a3ef-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5a3ef-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5a3ef-110">Permission type</span></span>      | <span data-ttu-id="5a3ef-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5a3ef-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5a3ef-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5a3ef-112">Delegated (work or school account)</span></span> | <span data-ttu-id="5a3ef-113">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5a3ef-113">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="5a3ef-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5a3ef-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5a3ef-115">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5a3ef-115">Notes.Create, Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="5a3ef-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5a3ef-116">Application</span></span> | <span data-ttu-id="5a3ef-117">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5a3ef-117">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="5a3ef-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5a3ef-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/sectionGroups/{id}/sectionGroups
GET /users/{id | userPrincipalName}/onenote/sectionGroups/{id}/sectionGroups
GET /groups/{id}/onenote/sectionGroups/{id}/sectionGroups
GET /sites/{id}/onenote/sectionGroups/{id}/sectionGroups
```
## <a name="optional-query-parameters"></a><span data-ttu-id="5a3ef-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="5a3ef-119">Optional query parameters</span></span>
<span data-ttu-id="5a3ef-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="5a3ef-121">El criterio de ordenación predeterminado es `name asc`.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-121">The default sort order is `name asc`.</span></span>

<span data-ttu-id="5a3ef-p103">La consulta predeterminada expande `parentNotebook` y selecciona sus propiedades `id`, `displayName` y `self`. Los valores válidos de `expand` de los grupos de secciones son `sections`, `sectionGroups`, `parentNotebook` y `parentSectionGroup`.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-p103">The default query expands `parentNotebook` and selects its `id`, `displayName`, and `self` properties. Valid `expand` values for section groups are `sections`, `sectionGroups`, `parentNotebook`, and `parentSectionGroup`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="5a3ef-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5a3ef-124">Request headers</span></span>
| <span data-ttu-id="5a3ef-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="5a3ef-125">Name</span></span>       | <span data-ttu-id="5a3ef-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="5a3ef-126">Type</span></span> | <span data-ttu-id="5a3ef-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="5a3ef-127">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="5a3ef-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="5a3ef-128">Authorization</span></span>  | <span data-ttu-id="5a3ef-129">string</span><span class="sxs-lookup"><span data-stu-id="5a3ef-129">string</span></span>  | <span data-ttu-id="5a3ef-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="5a3ef-132">Aceptar</span><span class="sxs-lookup"><span data-stu-id="5a3ef-132">Accept</span></span> | <span data-ttu-id="5a3ef-133">string</span><span class="sxs-lookup"><span data-stu-id="5a3ef-133">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="5a3ef-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5a3ef-134">Request body</span></span>
<span data-ttu-id="5a3ef-135">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-135">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5a3ef-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5a3ef-136">Response</span></span>

<span data-ttu-id="5a3ef-137">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [sectionGroup](../resources/sectiongroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-137">If successful, this method returns a `200 OK` response code and a collection of [sectionGroup](../resources/sectiongroup.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="5a3ef-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5a3ef-138">Example</span></span>
##### <a name="request"></a><span data-ttu-id="5a3ef-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5a3ef-139">Request</span></span>
<span data-ttu-id="5a3ef-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-140">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_sectiongroups"
}-->
```http
GET https://graph.microsoft.com/beta/me/onenote/sectionGroups/{id}/sectionGroups
```
##### <a name="response"></a><span data-ttu-id="5a3ef-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5a3ef-141">Response</span></span>
<span data-ttu-id="5a3ef-p105">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-p105">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.sectiongroup",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 378

{
  "value": [
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
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List sectionGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->