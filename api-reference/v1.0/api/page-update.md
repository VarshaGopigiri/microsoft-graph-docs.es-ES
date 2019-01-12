---
title: Actualizar página
description: Actualiza el contenido de una página de OneNote.
localization_priority: Normal
author: jewan-microsoft
ms.prod: onenote
ms.openlocfilehash: ef51342aba7bab49fde6d69ea0c77c62dc841b7d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27971714"
---
# <a name="update-page"></a><span data-ttu-id="b45f0-103">Actualizar página</span><span class="sxs-lookup"><span data-stu-id="b45f0-103">Update page</span></span>

<span data-ttu-id="b45f0-104">Actualiza el contenido de una página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="b45f0-104">Update the content of a OneNote page.</span></span>
## <a name="permissions"></a><span data-ttu-id="b45f0-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="b45f0-105">Permissions</span></span>
<span data-ttu-id="b45f0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b45f0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b45f0-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b45f0-108">Permission type</span></span>      | <span data-ttu-id="b45f0-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b45f0-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b45f0-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b45f0-110">Delegated (work or school account)</span></span> | <span data-ttu-id="b45f0-111">Notes.ReadWrite, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b45f0-111">Notes.ReadWrite, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="b45f0-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b45f0-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b45f0-113">Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b45f0-113">Notes.ReadWrite</span></span>    |
|<span data-ttu-id="b45f0-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b45f0-114">Application</span></span> | <span data-ttu-id="b45f0-115">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b45f0-115">Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="b45f0-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b45f0-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/onenote/pages/{id}/content
PATCH /users/{id | userPrincipalName}/onenote/pages/{id}/content
PATCH /groups/{id}/onenote/pages/{id}/content
PATCH /sites/{id}/onenote/pages/{id}/content
```
## <a name="request-headers"></a><span data-ttu-id="b45f0-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b45f0-117">Request headers</span></span>
| <span data-ttu-id="b45f0-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="b45f0-118">Name</span></span>       | <span data-ttu-id="b45f0-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="b45f0-119">Type</span></span> | <span data-ttu-id="b45f0-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="b45f0-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="b45f0-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="b45f0-121">Authorization</span></span>  | <span data-ttu-id="b45f0-122">string</span><span class="sxs-lookup"><span data-stu-id="b45f0-122">string</span></span>  | <span data-ttu-id="b45f0-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b45f0-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="b45f0-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="b45f0-125">Content-Type</span></span> | <span data-ttu-id="b45f0-126">string</span><span class="sxs-lookup"><span data-stu-id="b45f0-126">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="b45f0-127">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="b45f0-127">Request body</span></span>
<span data-ttu-id="b45f0-p103">En el cuerpo de la solicitud, proporcione una matriz de objetos [patchContentCommand](../resources/patchcontentcommand.md) que representen los cambios a la página. Para obtener más información y ejemplos, consulte <a href="https://msdn.microsoft.com/office/office365/howto/onenote-update-page">Actualizar páginas de OneNote</a>.</span><span class="sxs-lookup"><span data-stu-id="b45f0-p103">In the request body, supply an array of [patchContentCommand](../resources/patchcontentcommand.md) objects that represent the changes to the page. For more information and examples, see <a href="https://msdn.microsoft.com/office/office365/howto/onenote-update-page">Update OneNote pages</a>.</span></span>

## <a name="response"></a><span data-ttu-id="b45f0-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b45f0-130">Response</span></span>

<span data-ttu-id="b45f0-p104">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.  No se devuelven datos JSON para una solicitud PATCH.</span><span class="sxs-lookup"><span data-stu-id="b45f0-p104">If successful, this method returns a `204 No Content` response code.  No JSON data is returned for a PATCH request.</span></span>
## <a name="example"></a><span data-ttu-id="b45f0-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b45f0-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b45f0-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b45f0-134">Request</span></span>
<span data-ttu-id="b45f0-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b45f0-135">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="b45f0-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b45f0-136">Response</span></span>
<span data-ttu-id="b45f0-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b45f0-137">Here is an example of the response.</span></span> 
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
