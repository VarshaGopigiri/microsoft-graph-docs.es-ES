---
title: Obtener sección
description: Recupere las propiedades y las relaciones de un objeto section.
localization_priority: Normal
author: jewan-microsoft
ms.prod: onenote
ms.openlocfilehash: ce475e0bdd8b5557eb2b6c457c6736ac635eb0be
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27953402"
---
# <a name="get-section"></a><span data-ttu-id="8be36-103">Obtener sección</span><span class="sxs-lookup"><span data-stu-id="8be36-103">Get section</span></span>

> <span data-ttu-id="8be36-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8be36-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8be36-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8be36-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8be36-106">Recupere las propiedades y las relaciones de un objeto [section](../resources/section.md).</span><span class="sxs-lookup"><span data-stu-id="8be36-106">Retrieve the properties and relationships of a [section](../resources/section.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="8be36-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="8be36-107">Permissions</span></span>
<span data-ttu-id="8be36-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8be36-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8be36-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8be36-110">Permission type</span></span>      | <span data-ttu-id="8be36-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8be36-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8be36-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8be36-112">Delegated (work or school account)</span></span> | <span data-ttu-id="8be36-113">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8be36-113">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="8be36-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8be36-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8be36-115">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8be36-115">Notes.Create, Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="8be36-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8be36-116">Application</span></span> | <span data-ttu-id="8be36-117">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8be36-117">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="8be36-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8be36-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/sections/{id}
GET /users/{id | userPrincipalName}/onenote/sections/{id}
GET /groups/{id}/onenote/sections/{id}
GET /sites/{id}/onenote/sections/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="8be36-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="8be36-119">Optional query parameters</span></span>
<span data-ttu-id="8be36-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) de `select` y `expand` a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8be36-120">This method supports the `select` and `expand` [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="8be36-p103">La consulta predeterminada expande `parentNotebook` y selecciona sus propiedades `id`, `displayName` y `self`. Los valores válidos de `expand` para las secciones son `parentNotebook` y `parentSectionGroup`.</span><span class="sxs-lookup"><span data-stu-id="8be36-p103">The default query expands `parentNotebook` and selects its `id`, `displayName`, and `self` properties. Valid `expand` values for sections are `parentNotebook` and `parentSectionGroup`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="8be36-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8be36-123">Request headers</span></span>
| <span data-ttu-id="8be36-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="8be36-124">Name</span></span>       | <span data-ttu-id="8be36-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="8be36-125">Type</span></span> | <span data-ttu-id="8be36-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="8be36-126">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="8be36-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="8be36-127">Authorization</span></span>  | <span data-ttu-id="8be36-128">string</span><span class="sxs-lookup"><span data-stu-id="8be36-128">string</span></span>  | <span data-ttu-id="8be36-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8be36-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="8be36-131">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8be36-131">Accept</span></span> | <span data-ttu-id="8be36-132">string</span><span class="sxs-lookup"><span data-stu-id="8be36-132">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="8be36-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8be36-133">Request body</span></span>
<span data-ttu-id="8be36-134">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8be36-134">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8be36-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8be36-135">Response</span></span>

<span data-ttu-id="8be36-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [section](../resources/section.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8be36-136">If successful, this method returns a `200 OK` response code and a [section](../resources/section.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="8be36-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8be36-137">Example</span></span>
##### <a name="request"></a><span data-ttu-id="8be36-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8be36-138">Request</span></span>
<span data-ttu-id="8be36-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8be36-139">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_section"
}-->
```http
GET https://graph.microsoft.com/beta/me/onenote/sections/{id}
```
##### <a name="response"></a><span data-ttu-id="8be36-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8be36-140">Response</span></span>
<span data-ttu-id="8be36-p105">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8be36-p105">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.onenoteSection"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 272

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
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get section",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
