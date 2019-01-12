---
title: Obtener bloc de notas
description: Recupera las propiedades y las relaciones de un objeto notebook.
author: jewan-microsoft
localization_priority: Normal
ms.prod: onenote
ms.openlocfilehash: befabbe46950b6b68819be992f0257cc121a2075
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27927642"
---
# <a name="get-notebook"></a><span data-ttu-id="9ce69-103">Obtener bloc de notas</span><span class="sxs-lookup"><span data-stu-id="9ce69-103">Get notebook</span></span>

> <span data-ttu-id="9ce69-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9ce69-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9ce69-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9ce69-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9ce69-106">Recupera las propiedades y las relaciones de un objeto [notebook](../resources/notebook.md).</span><span class="sxs-lookup"><span data-stu-id="9ce69-106">Retrieve the properties and relationships of a [notebook](../resources/notebook.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="9ce69-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="9ce69-107">Permissions</span></span>
<span data-ttu-id="9ce69-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9ce69-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9ce69-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9ce69-110">Permission type</span></span>      | <span data-ttu-id="9ce69-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9ce69-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9ce69-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9ce69-112">Delegated (work or school account)</span></span> | <span data-ttu-id="9ce69-113">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9ce69-113">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="9ce69-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9ce69-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9ce69-115">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9ce69-115">Notes.Create, Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="9ce69-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9ce69-116">Application</span></span> | <span data-ttu-id="9ce69-117">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9ce69-117">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="9ce69-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9ce69-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/notebooks/{id}
GET /users/{id | userPrincipalName}/onenote/notebooks/{id}
GET /groups/{id}/onenote/notebooks/{id}
GET /sites/{id}/onenote/notebooks/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="9ce69-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="9ce69-119">Optional query parameters</span></span>
<span data-ttu-id="9ce69-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) de `select` y `expand` a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9ce69-120">This method supports the `select` and `expand` [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="9ce69-121">`sections` y `sectionGroups` son valores de `expand` para los blocs de notas.</span><span class="sxs-lookup"><span data-stu-id="9ce69-121">Valid `expand` values for notebooks are `sections` and `sectionGroups`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="9ce69-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9ce69-122">Request headers</span></span>
| <span data-ttu-id="9ce69-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="9ce69-123">Name</span></span>       | <span data-ttu-id="9ce69-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="9ce69-124">Type</span></span> | <span data-ttu-id="9ce69-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="9ce69-125">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="9ce69-126">Autorización</span><span class="sxs-lookup"><span data-stu-id="9ce69-126">Authorization</span></span>  | <span data-ttu-id="9ce69-127">string</span><span class="sxs-lookup"><span data-stu-id="9ce69-127">string</span></span>  | <span data-ttu-id="9ce69-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9ce69-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="9ce69-130">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9ce69-130">Accept</span></span> | <span data-ttu-id="9ce69-131">string</span><span class="sxs-lookup"><span data-stu-id="9ce69-131">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="9ce69-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9ce69-132">Request body</span></span>
<span data-ttu-id="9ce69-133">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9ce69-133">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9ce69-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9ce69-134">Response</span></span>

<span data-ttu-id="9ce69-135">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [notebook](../resources/notebook.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9ce69-135">If successful, this method returns a `200 OK` response code and a [notebook](../resources/notebook.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="9ce69-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9ce69-136">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9ce69-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9ce69-137">Request</span></span>
<span data-ttu-id="9ce69-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9ce69-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_notebook"
}-->
```http
GET https://graph.microsoft.com/beta/me/onenote/notebooks/{id}
```
##### <a name="response"></a><span data-ttu-id="9ce69-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9ce69-139">Response</span></span>
<span data-ttu-id="9ce69-p104">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9ce69-p104">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.notebook"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 284

{
  "isDefault": true,
  "userRole": {
  },
  "id": "8fcb5dbc-d5aa-4681-8e31-b001d5168d79",
  "isShared": true,
  "sectionsUrl": "sectionsUrl-value",
  "sectionGroupsUrl": "sectionGroupsUrl-value",
  "links": {
    "oneNoteClientUrl": {
      "href": "href-value"
    },
    "oneNoteWebUrl": {
      "href": "href-value"
    }
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get notebook",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
