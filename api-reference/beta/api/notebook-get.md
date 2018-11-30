---
title: Obtener bloc de notas
description: Recupera las propiedades y las relaciones de un objeto notebook.
ms.openlocfilehash: 9dd264dd2498e0c775629b9e178b7660426a8d69
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090028"
---
# <a name="get-notebook"></a><span data-ttu-id="58151-103">Obtener bloc de notas</span><span class="sxs-lookup"><span data-stu-id="58151-103">Get notebook</span></span>

> <span data-ttu-id="58151-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="58151-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="58151-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="58151-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="58151-106">Recupera las propiedades y las relaciones de un objeto [notebook](../resources/notebook.md).</span><span class="sxs-lookup"><span data-stu-id="58151-106">Retrieve the properties and relationships of a [notebook](../resources/notebook.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="58151-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="58151-107">Permissions</span></span>
<span data-ttu-id="58151-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="58151-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="58151-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="58151-110">Permission type</span></span>      | <span data-ttu-id="58151-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="58151-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="58151-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="58151-112">Delegated (work or school account)</span></span> | <span data-ttu-id="58151-113">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="58151-113">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="58151-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="58151-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="58151-115">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="58151-115">Notes.Create, Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="58151-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="58151-116">Application</span></span> | <span data-ttu-id="58151-117">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="58151-117">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="58151-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="58151-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/notebooks/{id}
GET /users/{id | userPrincipalName}/onenote/notebooks/{id}
GET /groups/{id}/onenote/notebooks/{id}
GET /sites/{id}/onenote/notebooks/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="58151-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="58151-119">Optional query parameters</span></span>
<span data-ttu-id="58151-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) de `select` y `expand` a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="58151-120">This method supports the `select` and `expand` [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="58151-121">`sections` y `sectionGroups` son valores de `expand` para los blocs de notas.</span><span class="sxs-lookup"><span data-stu-id="58151-121">Valid `expand` values for notebooks are `sections` and `sectionGroups`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="58151-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="58151-122">Request headers</span></span>
| <span data-ttu-id="58151-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="58151-123">Name</span></span>       | <span data-ttu-id="58151-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="58151-124">Type</span></span> | <span data-ttu-id="58151-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="58151-125">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="58151-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="58151-126">Authorization</span></span>  | <span data-ttu-id="58151-127">string</span><span class="sxs-lookup"><span data-stu-id="58151-127">string</span></span>  | <span data-ttu-id="58151-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="58151-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="58151-130">Aceptar</span><span class="sxs-lookup"><span data-stu-id="58151-130">Accept</span></span> | <span data-ttu-id="58151-131">string</span><span class="sxs-lookup"><span data-stu-id="58151-131">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="58151-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="58151-132">Request body</span></span>
<span data-ttu-id="58151-133">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="58151-133">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="58151-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="58151-134">Response</span></span>

<span data-ttu-id="58151-135">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [notebook](../resources/notebook.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="58151-135">If successful, this method returns a `200 OK` response code and a [notebook](../resources/notebook.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="58151-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="58151-136">Example</span></span>
##### <a name="request"></a><span data-ttu-id="58151-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="58151-137">Request</span></span>
<span data-ttu-id="58151-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="58151-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_notebook"
}-->
```http
GET https://graph.microsoft.com/beta/me/onenote/notebooks/{id}
```
##### <a name="response"></a><span data-ttu-id="58151-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="58151-139">Response</span></span>
<span data-ttu-id="58151-p104">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="58151-p104">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
