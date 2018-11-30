---
title: Actualizar página
description: Actualiza el contenido de una página de OneNote.
ms.openlocfilehash: 862271da69985b7386f5025d630227b6222cd64a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088307"
---
# <a name="update-page"></a><span data-ttu-id="44471-103">Actualizar página</span><span class="sxs-lookup"><span data-stu-id="44471-103">Update page</span></span>

> <span data-ttu-id="44471-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="44471-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="44471-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="44471-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="44471-106">Actualiza el contenido de una página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="44471-106">Update the content of a OneNote page.</span></span>
## <a name="permissions"></a><span data-ttu-id="44471-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="44471-107">Permissions</span></span>
<span data-ttu-id="44471-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="44471-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="44471-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="44471-110">Permission type</span></span>      | <span data-ttu-id="44471-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="44471-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="44471-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="44471-112">Delegated (work or school account)</span></span> | <span data-ttu-id="44471-113">Notes.ReadWrite, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="44471-113">Notes.ReadWrite, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="44471-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="44471-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="44471-115">Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="44471-115">Notes.ReadWrite</span></span>    |
|<span data-ttu-id="44471-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="44471-116">Application</span></span> | <span data-ttu-id="44471-117">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="44471-117">Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="44471-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="44471-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/onenote/pages/{id}/content
PATCH /users/{id | userPrincipalName}/onenote/pages/{id}/content
PATCH /groups/{id}/onenote/pages/{id}/content
PATCH /sites/{id}/onenote/pages/{id}/content
```
## <a name="request-headers"></a><span data-ttu-id="44471-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="44471-119">Request headers</span></span>
| <span data-ttu-id="44471-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="44471-120">Name</span></span>       | <span data-ttu-id="44471-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="44471-121">Type</span></span> | <span data-ttu-id="44471-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="44471-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="44471-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="44471-123">Authorization</span></span>  | <span data-ttu-id="44471-124">string</span><span class="sxs-lookup"><span data-stu-id="44471-124">string</span></span>  | <span data-ttu-id="44471-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="44471-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="44471-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="44471-127">Content-Type</span></span> | <span data-ttu-id="44471-128">string</span><span class="sxs-lookup"><span data-stu-id="44471-128">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="44471-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="44471-129">Request body</span></span>
<span data-ttu-id="44471-130">En el cuerpo de la solicitud, proporcionar una matriz de objetos de [patchContentCommand](../resources/patchcontentcommand.md) que representan los cambios a la página.</span><span class="sxs-lookup"><span data-stu-id="44471-130">In the request body, supply an array of [patchContentCommand](../resources/patchcontentcommand.md) objects that represent the changes to the page.</span></span> <span data-ttu-id="44471-131">Para obtener más información y ejemplos, vea el [contenido de la página actualización de OneNote](/graph/onenote-update-page).</span><span class="sxs-lookup"><span data-stu-id="44471-131">For more information and examples, see [Update OneNote page content](/graph/onenote-update-page).</span></span>

## <a name="response"></a><span data-ttu-id="44471-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="44471-132">Response</span></span>

<span data-ttu-id="44471-p105">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.  No se devuelven datos JSON para una solicitud PATCH.</span><span class="sxs-lookup"><span data-stu-id="44471-p105">If successful, this method returns a `204 No Content` response code.  No JSON data is returned for a PATCH request.</span></span>
## <a name="example"></a><span data-ttu-id="44471-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="44471-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="44471-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="44471-136">Request</span></span>
<span data-ttu-id="44471-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="44471-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_page"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/onenote/pages/{id}/content
Content-type: application/json
Content-length: 312

[
   {
    'target':'#para-id',
    'action':'insert',
    'position':'before',
    'content':'<img src="image-url-or-part-name" alt="image-alt-text" />'
  }, 
  {
    'target':'#list-id',
    'action':'append',
    'content':'<li>new-page-content</li>'
  }
]
```
##### <a name="response"></a><span data-ttu-id="44471-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="44471-138">Response</span></span>
<span data-ttu-id="44471-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="44471-139">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.onenotePage"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update page",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
