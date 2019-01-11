---
title: Enumerar secciones
description: Recupera una lista de los objetos de la sección.
author: Jewan-microsoft
localization_priority: Normal
ms.openlocfilehash: 11636dd2fbb0c39724b0036bdfa5db03bb12f0c9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27857697"
---
# <a name="list-sections"></a><span data-ttu-id="e7197-103">Enumerar secciones</span><span class="sxs-lookup"><span data-stu-id="e7197-103">List sections</span></span>

> <span data-ttu-id="e7197-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e7197-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e7197-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e7197-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e7197-106">Recupera una lista de los objetos de la [sección](../resources/section.md).</span><span class="sxs-lookup"><span data-stu-id="e7197-106">Retrieve a list of [section](../resources/section.md) objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="e7197-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="e7197-107">Permissions</span></span>
<span data-ttu-id="e7197-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e7197-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e7197-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e7197-110">Permission type</span></span>      | <span data-ttu-id="e7197-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e7197-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e7197-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e7197-112">Delegated (work or school account)</span></span> | <span data-ttu-id="e7197-113">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e7197-113">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="e7197-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e7197-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e7197-115">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e7197-115">Notes.Create, Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="e7197-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e7197-116">Application</span></span> | <span data-ttu-id="e7197-117">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e7197-117">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="e7197-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e7197-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/sections
GET /users/{id | userPrincipalName}/onenote/sections
GET /groups/{id}/onenote/sections
GET /sites/{id}/onenote/sections
```
## <a name="optional-query-parameters"></a><span data-ttu-id="e7197-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e7197-119">Optional query parameters</span></span>
<span data-ttu-id="e7197-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e7197-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="e7197-121">El criterio de ordenación predeterminado es `name asc`.</span><span class="sxs-lookup"><span data-stu-id="e7197-121">The default sort order is `name asc`.</span></span>

<span data-ttu-id="e7197-p103">La consulta predeterminada expande `parentNotebook` y selecciona sus propiedades `id`, `displayName` y `self`. Los valores válidos de `expand` para las secciones son `parentNotebook` y `parentSectionGroup`.</span><span class="sxs-lookup"><span data-stu-id="e7197-p103">The default query expands `parentNotebook` and selects its `id`, `displayName`, and `self` properties. Valid `expand` values for sections are `parentNotebook` and `parentSectionGroup`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="e7197-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e7197-124">Request headers</span></span>
| <span data-ttu-id="e7197-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="e7197-125">Name</span></span>       | <span data-ttu-id="e7197-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="e7197-126">Type</span></span> | <span data-ttu-id="e7197-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7197-127">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="e7197-128">Autorización</span><span class="sxs-lookup"><span data-stu-id="e7197-128">Authorization</span></span>  | <span data-ttu-id="e7197-129">string</span><span class="sxs-lookup"><span data-stu-id="e7197-129">string</span></span>  | <span data-ttu-id="e7197-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e7197-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="e7197-132">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e7197-132">Accept</span></span> | <span data-ttu-id="e7197-133">string</span><span class="sxs-lookup"><span data-stu-id="e7197-133">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="e7197-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e7197-134">Request body</span></span>
<span data-ttu-id="e7197-135">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e7197-135">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e7197-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e7197-136">Response</span></span>

<span data-ttu-id="e7197-137">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [section](../resources/section.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e7197-137">If successful, this method returns a `200 OK` response code and collection of [section](../resources/section.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e7197-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e7197-138">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e7197-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e7197-139">Request</span></span>
<span data-ttu-id="e7197-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e7197-140">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_sections"
}-->
```http
GET https://graph.microsoft.com/beta/me/onenote/sections
```
##### <a name="response"></a><span data-ttu-id="e7197-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e7197-141">Response</span></span>
<span data-ttu-id="e7197-p105">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e7197-p105">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
      "id": "8fcb5dbc-d5aa-4681-8e31-b001d5168d79",
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
