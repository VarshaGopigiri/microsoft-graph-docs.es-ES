---
title: Obtener sección
description: Recupere las propiedades y las relaciones de un objeto section.
localization_priority: Normal
ms.openlocfilehash: b9746715d01a51f0a35da3936e64b850020629ab
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27846952"
---
# <a name="get-section"></a><span data-ttu-id="8c91f-103">Obtener sección</span><span class="sxs-lookup"><span data-stu-id="8c91f-103">Get section</span></span>

> <span data-ttu-id="8c91f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8c91f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8c91f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8c91f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8c91f-106">Recupere las propiedades y las relaciones de un objeto [section](../resources/section.md).</span><span class="sxs-lookup"><span data-stu-id="8c91f-106">Retrieve the properties and relationships of a [section](../resources/section.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="8c91f-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="8c91f-107">Permissions</span></span>
<span data-ttu-id="8c91f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8c91f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8c91f-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8c91f-110">Permission type</span></span>      | <span data-ttu-id="8c91f-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8c91f-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8c91f-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8c91f-112">Delegated (work or school account)</span></span> | <span data-ttu-id="8c91f-113">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8c91f-113">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="8c91f-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8c91f-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8c91f-115">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8c91f-115">Notes.Create, Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="8c91f-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8c91f-116">Application</span></span> | <span data-ttu-id="8c91f-117">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8c91f-117">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="8c91f-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8c91f-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/sections/{id}
GET /users/{id | userPrincipalName}/onenote/sections/{id}
GET /groups/{id}/onenote/sections/{id}
GET /sites/{id}/onenote/sections/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="8c91f-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="8c91f-119">Optional query parameters</span></span>
<span data-ttu-id="8c91f-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) de `select` y `expand` a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8c91f-120">This method supports the `select` and `expand` [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="8c91f-p103">La consulta predeterminada expande `parentNotebook` y selecciona sus propiedades `id`, `displayName` y `self`. Los valores válidos de `expand` para las secciones son `parentNotebook` y `parentSectionGroup`.</span><span class="sxs-lookup"><span data-stu-id="8c91f-p103">The default query expands `parentNotebook` and selects its `id`, `displayName`, and `self` properties. Valid `expand` values for sections are `parentNotebook` and `parentSectionGroup`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="8c91f-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8c91f-123">Request headers</span></span>
| <span data-ttu-id="8c91f-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="8c91f-124">Name</span></span>       | <span data-ttu-id="8c91f-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="8c91f-125">Type</span></span> | <span data-ttu-id="8c91f-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c91f-126">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="8c91f-127">Autorización</span><span class="sxs-lookup"><span data-stu-id="8c91f-127">Authorization</span></span>  | <span data-ttu-id="8c91f-128">string</span><span class="sxs-lookup"><span data-stu-id="8c91f-128">string</span></span>  | <span data-ttu-id="8c91f-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8c91f-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="8c91f-131">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8c91f-131">Accept</span></span> | <span data-ttu-id="8c91f-132">string</span><span class="sxs-lookup"><span data-stu-id="8c91f-132">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="8c91f-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8c91f-133">Request body</span></span>
<span data-ttu-id="8c91f-134">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8c91f-134">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8c91f-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8c91f-135">Response</span></span>

<span data-ttu-id="8c91f-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [section](../resources/section.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8c91f-136">If successful, this method returns a `200 OK` response code and a [section](../resources/section.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="8c91f-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8c91f-137">Example</span></span>
##### <a name="request"></a><span data-ttu-id="8c91f-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8c91f-138">Request</span></span>
<span data-ttu-id="8c91f-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8c91f-139">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_section"
}-->
```http
GET https://graph.microsoft.com/beta/me/onenote/sections/{id}
```
##### <a name="response"></a><span data-ttu-id="8c91f-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8c91f-140">Response</span></span>
<span data-ttu-id="8c91f-p105">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8c91f-p105">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
