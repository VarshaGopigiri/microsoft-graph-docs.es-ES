---
title: Eliminar página
description: Elimine una página de OneNote.
localization_priority: Normal
ms.openlocfilehash: fc2a4a9e809cb3a335c795a27cb5ffe35487a880
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27810013"
---
# <a name="delete-page"></a><span data-ttu-id="070e3-103">Eliminar página</span><span class="sxs-lookup"><span data-stu-id="070e3-103">Delete page</span></span>

<span data-ttu-id="070e3-104">Elimine una página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="070e3-104">Delete a OneNote page.</span></span>
## <a name="permissions"></a><span data-ttu-id="070e3-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="070e3-105">Permissions</span></span>
<span data-ttu-id="070e3-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="070e3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="070e3-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="070e3-108">Permission type</span></span>      | <span data-ttu-id="070e3-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="070e3-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="070e3-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="070e3-110">Delegated (work or school account)</span></span> | <span data-ttu-id="070e3-111">Notes.ReadWrite, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="070e3-111">Notes.ReadWrite, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="070e3-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="070e3-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="070e3-113">Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="070e3-113">Notes.ReadWrite</span></span>    |
|<span data-ttu-id="070e3-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="070e3-114">Application</span></span> | <span data-ttu-id="070e3-115">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="070e3-115">Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="070e3-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="070e3-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/onenote/pages/{id}
DELETE /users/{id | userPrincipalName}/onenote/pages/{id}
DELETE /groups/{id}/onenote/pages/{id}
DELETE /sites/{id}/onenote/pages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="070e3-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="070e3-117">Request headers</span></span>
| <span data-ttu-id="070e3-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="070e3-118">Name</span></span>       | <span data-ttu-id="070e3-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="070e3-119">Type</span></span> | <span data-ttu-id="070e3-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="070e3-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="070e3-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="070e3-121">Authorization</span></span>  | <span data-ttu-id="070e3-122">string</span><span class="sxs-lookup"><span data-stu-id="070e3-122">string</span></span>  | <span data-ttu-id="070e3-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="070e3-p102">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="070e3-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="070e3-125">Response</span></span>

<span data-ttu-id="070e3-p103">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="070e3-p103">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="070e3-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="070e3-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="070e3-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="070e3-129">Request</span></span>
<span data-ttu-id="070e3-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="070e3-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_page"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/onenote/pages/{id}
```
##### <a name="response"></a><span data-ttu-id="070e3-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="070e3-131">Response</span></span>
<span data-ttu-id="070e3-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="070e3-132">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete page",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
