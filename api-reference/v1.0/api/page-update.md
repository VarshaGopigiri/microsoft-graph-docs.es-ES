---
title: Actualizar página
description: Actualiza el contenido de una página de OneNote.
localization_priority: Normal
ms.openlocfilehash: ee5e55ce206ac1f3069c5629f8c0f674f209363c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27850179"
---
# <a name="update-page"></a><span data-ttu-id="d6034-103">Actualizar página</span><span class="sxs-lookup"><span data-stu-id="d6034-103">Update page</span></span>

<span data-ttu-id="d6034-104">Actualiza el contenido de una página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="d6034-104">Update the content of a OneNote page.</span></span>
## <a name="permissions"></a><span data-ttu-id="d6034-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="d6034-105">Permissions</span></span>
<span data-ttu-id="d6034-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d6034-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d6034-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d6034-108">Permission type</span></span>      | <span data-ttu-id="d6034-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d6034-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d6034-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d6034-110">Delegated (work or school account)</span></span> | <span data-ttu-id="d6034-111">Notes.ReadWrite, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d6034-111">Notes.ReadWrite, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="d6034-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d6034-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d6034-113">Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d6034-113">Notes.ReadWrite</span></span>    |
|<span data-ttu-id="d6034-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d6034-114">Application</span></span> | <span data-ttu-id="d6034-115">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d6034-115">Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d6034-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d6034-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/onenote/pages/{id}/content
PATCH /users/{id | userPrincipalName}/onenote/pages/{id}/content
PATCH /groups/{id}/onenote/pages/{id}/content
PATCH /sites/{id}/onenote/pages/{id}/content
```
## <a name="request-headers"></a><span data-ttu-id="d6034-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d6034-117">Request headers</span></span>
| <span data-ttu-id="d6034-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="d6034-118">Name</span></span>       | <span data-ttu-id="d6034-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6034-119">Type</span></span> | <span data-ttu-id="d6034-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6034-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="d6034-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="d6034-121">Authorization</span></span>  | <span data-ttu-id="d6034-122">string</span><span class="sxs-lookup"><span data-stu-id="d6034-122">string</span></span>  | <span data-ttu-id="d6034-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d6034-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d6034-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d6034-125">Content-Type</span></span> | <span data-ttu-id="d6034-126">string</span><span class="sxs-lookup"><span data-stu-id="d6034-126">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="d6034-127">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="d6034-127">Request body</span></span>
<span data-ttu-id="d6034-p103">En el cuerpo de la solicitud, proporcione una matriz de objetos [patchContentCommand](../resources/patchcontentcommand.md) que representen los cambios a la página. Para obtener más información y ejemplos, consulte <a href="https://msdn.microsoft.com/office/office365/howto/onenote-update-page">Actualizar páginas de OneNote</a>.</span><span class="sxs-lookup"><span data-stu-id="d6034-p103">In the request body, supply an array of [patchContentCommand](../resources/patchcontentcommand.md) objects that represent the changes to the page. For more information and examples, see <a href="https://msdn.microsoft.com/office/office365/howto/onenote-update-page">Update OneNote pages</a>.</span></span>

## <a name="response"></a><span data-ttu-id="d6034-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d6034-130">Response</span></span>

<span data-ttu-id="d6034-p104">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.  No se devuelven datos JSON para una solicitud PATCH.</span><span class="sxs-lookup"><span data-stu-id="d6034-p104">If successful, this method returns a `204 No Content` response code.  No JSON data is returned for a PATCH request.</span></span>
## <a name="example"></a><span data-ttu-id="d6034-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d6034-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d6034-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d6034-134">Request</span></span>
<span data-ttu-id="d6034-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d6034-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_page"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/onenote/pages/{id}/content
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
##### <a name="response"></a><span data-ttu-id="d6034-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d6034-136">Response</span></span>
<span data-ttu-id="d6034-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d6034-137">Here is an example of the response.</span></span> 
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
