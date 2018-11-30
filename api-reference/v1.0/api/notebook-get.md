---
title: Obtener bloc de notas
description: Recupera las propiedades y las relaciones de un objeto notebook.
ms.openlocfilehash: e00f9eb8f7ede1bc247d41dc466f58ededb1ecd5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031778"
---
# <a name="get-notebook"></a><span data-ttu-id="b60b3-103">Obtener bloc de notas</span><span class="sxs-lookup"><span data-stu-id="b60b3-103">Get notebook</span></span>

<span data-ttu-id="b60b3-104">Recupera las propiedades y las relaciones de un objeto [notebook](../resources/notebook.md).</span><span class="sxs-lookup"><span data-stu-id="b60b3-104">Retrieve the properties and relationships of a [notebook](../resources/notebook.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="b60b3-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="b60b3-105">Permissions</span></span>
<span data-ttu-id="b60b3-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b60b3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b60b3-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b60b3-108">Permission type</span></span>      | <span data-ttu-id="b60b3-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b60b3-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b60b3-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b60b3-110">Delegated (work or school account)</span></span> | <span data-ttu-id="b60b3-111">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b60b3-111">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="b60b3-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b60b3-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b60b3-113">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b60b3-113">Notes.Create, Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="b60b3-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b60b3-114">Application</span></span> | <span data-ttu-id="b60b3-115">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b60b3-115">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="b60b3-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b60b3-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/notebooks/{id}
GET /users/{id | userPrincipalName}/onenote/notebooks/{id}
GET /groups/{id}/onenote/notebooks/{id}
GET /sites/{id}/onenote/notebooks/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="b60b3-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b60b3-117">Optional query parameters</span></span>
<span data-ttu-id="b60b3-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) de `select` y `expand` a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b60b3-118">This method supports the `select` and `expand` [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="b60b3-119">`sections` y `sectionGroups` son valores de `expand` para los blocs de notas.</span><span class="sxs-lookup"><span data-stu-id="b60b3-119">Valid `expand` values for notebooks are `sections` and `sectionGroups`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="b60b3-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b60b3-120">Request headers</span></span>
| <span data-ttu-id="b60b3-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="b60b3-121">Name</span></span>       | <span data-ttu-id="b60b3-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="b60b3-122">Type</span></span> | <span data-ttu-id="b60b3-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="b60b3-123">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="b60b3-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="b60b3-124">Authorization</span></span>  | <span data-ttu-id="b60b3-125">string</span><span class="sxs-lookup"><span data-stu-id="b60b3-125">string</span></span>  | <span data-ttu-id="b60b3-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b60b3-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="b60b3-128">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b60b3-128">Accept</span></span> | <span data-ttu-id="b60b3-129">string</span><span class="sxs-lookup"><span data-stu-id="b60b3-129">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="b60b3-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b60b3-130">Request body</span></span>
<span data-ttu-id="b60b3-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b60b3-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b60b3-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b60b3-132">Response</span></span>

<span data-ttu-id="b60b3-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [notebook](../resources/notebook.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b60b3-133">If successful, this method returns a `200 OK` response code and a [notebook](../resources/notebook.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="b60b3-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b60b3-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b60b3-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b60b3-135">Request</span></span>
<span data-ttu-id="b60b3-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b60b3-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_notebook"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/notebooks/{id}
```
##### <a name="response"></a><span data-ttu-id="b60b3-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b60b3-137">Response</span></span>
<span data-ttu-id="b60b3-p103">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b60b3-p103">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
