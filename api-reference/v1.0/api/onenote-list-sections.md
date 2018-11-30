---
title: Enumerar secciones
description: Recuperar una lista de objetos de onenoteSection.
ms.openlocfilehash: ab6ee09acba2c6c0d30c02925e199af4484914ad
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032481"
---
# <a name="list-sections"></a><span data-ttu-id="875d4-103">Enumerar secciones</span><span class="sxs-lookup"><span data-stu-id="875d4-103">List sections</span></span>

<span data-ttu-id="875d4-104">Recuperar una lista de objetos de [onenoteSection](../resources/section.md) .</span><span class="sxs-lookup"><span data-stu-id="875d4-104">Retrieve a list of [onenoteSection](../resources/section.md) objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="875d4-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="875d4-105">Permissions</span></span>
<span data-ttu-id="875d4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="875d4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="875d4-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="875d4-108">Permission type</span></span>      | <span data-ttu-id="875d4-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="875d4-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="875d4-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="875d4-110">Delegated (work or school account)</span></span> | <span data-ttu-id="875d4-111">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="875d4-111">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="875d4-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="875d4-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="875d4-113">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="875d4-113">Notes.Create, Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="875d4-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="875d4-114">Application</span></span> | <span data-ttu-id="875d4-115">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="875d4-115">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="875d4-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="875d4-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/sections
GET /users/{id | userPrincipalName}/onenote/sections
GET /groups/{id}/onenote/sections
GET /sites/{id}/onenote/sections
```
## <a name="optional-query-parameters"></a><span data-ttu-id="875d4-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="875d4-117">Optional query parameters</span></span>
<span data-ttu-id="875d4-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="875d4-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="875d4-119">El criterio de ordenación predeterminado es `name asc`.</span><span class="sxs-lookup"><span data-stu-id="875d4-119">The default sort order is `name asc`.</span></span>

<span data-ttu-id="875d4-p102">La consulta predeterminada expande `parentNotebook` y selecciona sus propiedades `id`, `displayName` y `self`. Los valores válidos de `expand` para las secciones son `parentNotebook` y `parentSectionGroup`.</span><span class="sxs-lookup"><span data-stu-id="875d4-p102">The default query expands `parentNotebook` and selects its `id`, `displayName`, and `self` properties. Valid `expand` values for sections are `parentNotebook` and `parentSectionGroup`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="875d4-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="875d4-122">Request headers</span></span>
| <span data-ttu-id="875d4-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="875d4-123">Name</span></span>       | <span data-ttu-id="875d4-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="875d4-124">Type</span></span> | <span data-ttu-id="875d4-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="875d4-125">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="875d4-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="875d4-126">Authorization</span></span>  | <span data-ttu-id="875d4-127">string</span><span class="sxs-lookup"><span data-stu-id="875d4-127">string</span></span>  | <span data-ttu-id="875d4-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="875d4-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="875d4-130">Aceptar</span><span class="sxs-lookup"><span data-stu-id="875d4-130">Accept</span></span> | <span data-ttu-id="875d4-131">string</span><span class="sxs-lookup"><span data-stu-id="875d4-131">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="875d4-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="875d4-132">Request body</span></span>
<span data-ttu-id="875d4-133">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="875d4-133">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="875d4-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="875d4-134">Response</span></span>

<span data-ttu-id="875d4-135">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [onenoteSection](../resources/section.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="875d4-135">If successful, this method returns a `200 OK` response code and collection of [onenoteSection](../resources/section.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="875d4-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="875d4-136">Example</span></span>
##### <a name="request"></a><span data-ttu-id="875d4-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="875d4-137">Request</span></span>
<span data-ttu-id="875d4-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="875d4-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_sections"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/sections
```
##### <a name="response"></a><span data-ttu-id="875d4-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="875d4-139">Response</span></span>
<span data-ttu-id="875d4-p104">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="875d4-p104">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.onenoteSection",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 345

{
  "value": [
    {
      "isDefault": true,
      "pagesUrl": "pagesUrl-value",
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
  "description": "List sections",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->