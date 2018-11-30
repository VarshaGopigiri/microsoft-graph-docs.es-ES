---
title: Enumerar sectionGroups
description: Recupera una lista de objetos sectionGroup.
ms.openlocfilehash: 79f62fc91b97ce06aebab35ccc9308e6cfac5a3d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030326"
---
# <a name="list-sectiongroups"></a><span data-ttu-id="70d8a-103">Enumerar sectionGroups</span><span class="sxs-lookup"><span data-stu-id="70d8a-103">List sectionGroups</span></span>

<span data-ttu-id="70d8a-104">Recupera una lista de objetos [sectionGroup](../resources/sectiongroup.md).</span><span class="sxs-lookup"><span data-stu-id="70d8a-104">Retrieve a list of [sectionGroup](../resources/sectiongroup.md) objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="70d8a-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="70d8a-105">Permissions</span></span>
<span data-ttu-id="70d8a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="70d8a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="70d8a-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="70d8a-108">Permission type</span></span>      | <span data-ttu-id="70d8a-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="70d8a-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="70d8a-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="70d8a-110">Delegated (work or school account)</span></span> | <span data-ttu-id="70d8a-111">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="70d8a-111">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="70d8a-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="70d8a-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="70d8a-113">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="70d8a-113">Notes.Create, Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="70d8a-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="70d8a-114">Application</span></span> | <span data-ttu-id="70d8a-115">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="70d8a-115">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="70d8a-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="70d8a-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/sectionGroups
GET /users/{id | userPrincipalName}/onenote/sectionGroups
GET /groups/{id}/onenote/sectionGroups
GET /sites/{id}/onenote/sectionGroups
```
## <a name="optional-query-parameters"></a><span data-ttu-id="70d8a-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="70d8a-117">Optional query parameters</span></span>
<span data-ttu-id="70d8a-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="70d8a-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="70d8a-119">El criterio de ordenación predeterminado es `name asc`.</span><span class="sxs-lookup"><span data-stu-id="70d8a-119">The default sort order is `name asc`.</span></span>

<span data-ttu-id="70d8a-p102">La consulta predeterminada expande `parentNotebook` y selecciona sus propiedades `id`, `displayName` y `self`. Los valores válidos de `expand` de los grupos de secciones son `sections`, `sectionGroups`, `parentNotebook` y `parentSectionGroup`.</span><span class="sxs-lookup"><span data-stu-id="70d8a-p102">The default query expands `parentNotebook` and selects its `id`, `displayName`, and `self` properties. Valid `expand` values for section groups are `sections`, `sectionGroups`, `parentNotebook`, and `parentSectionGroup`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="70d8a-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="70d8a-122">Request headers</span></span>
| <span data-ttu-id="70d8a-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="70d8a-123">Name</span></span>       | <span data-ttu-id="70d8a-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="70d8a-124">Type</span></span> | <span data-ttu-id="70d8a-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="70d8a-125">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="70d8a-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="70d8a-126">Authorization</span></span>  | <span data-ttu-id="70d8a-127">string</span><span class="sxs-lookup"><span data-stu-id="70d8a-127">string</span></span>  | <span data-ttu-id="70d8a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="70d8a-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="70d8a-130">Aceptar</span><span class="sxs-lookup"><span data-stu-id="70d8a-130">Accept</span></span> | <span data-ttu-id="70d8a-131">string</span><span class="sxs-lookup"><span data-stu-id="70d8a-131">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="70d8a-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="70d8a-132">Request body</span></span>
<span data-ttu-id="70d8a-133">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="70d8a-133">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="70d8a-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="70d8a-134">Response</span></span>

<span data-ttu-id="70d8a-135">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [sectionGroup](../resources/sectiongroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="70d8a-135">If successful, this method returns a `200 OK` response code and collection of [sectionGroup](../resources/sectiongroup.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="70d8a-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="70d8a-136">Example</span></span>
##### <a name="request"></a><span data-ttu-id="70d8a-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="70d8a-137">Request</span></span>
<span data-ttu-id="70d8a-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="70d8a-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_sectiongroups"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/sectionGroups
```
##### <a name="response"></a><span data-ttu-id="70d8a-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="70d8a-139">Response</span></span>
<span data-ttu-id="70d8a-p104">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="70d8a-p104">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.sectionGroup",
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