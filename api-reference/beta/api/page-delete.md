---
title: Eliminar página
description: Elimine una página de OneNote.
ms.openlocfilehash: f2e566696937ee6f7808a66f994298802be66a17
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084645"
---
# <a name="delete-page"></a><span data-ttu-id="0b5f2-103">Eliminar página</span><span class="sxs-lookup"><span data-stu-id="0b5f2-103">Delete page</span></span>

> <span data-ttu-id="0b5f2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0b5f2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0b5f2-106">Elimine una página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-106">Delete a OneNote page.</span></span>
## <a name="permissions"></a><span data-ttu-id="0b5f2-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="0b5f2-107">Permissions</span></span>
<span data-ttu-id="0b5f2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0b5f2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0b5f2-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0b5f2-110">Permission type</span></span>      | <span data-ttu-id="0b5f2-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0b5f2-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0b5f2-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0b5f2-112">Delegated (work or school account)</span></span> | <span data-ttu-id="0b5f2-113">Notes.ReadWrite, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0b5f2-113">Notes.ReadWrite, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="0b5f2-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0b5f2-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0b5f2-115">Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0b5f2-115">Notes.ReadWrite</span></span>    |
|<span data-ttu-id="0b5f2-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0b5f2-116">Application</span></span> | <span data-ttu-id="0b5f2-117">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0b5f2-117">Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="0b5f2-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0b5f2-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/onenote/pages/{id}
DELETE /users/{id | userPrincipalName}/onenote/pages/{id}
DELETE /groups/{id}/onenote/pages/{id}
DELETE /sites/{id}/onenote/pages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="0b5f2-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0b5f2-119">Request headers</span></span>
| <span data-ttu-id="0b5f2-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="0b5f2-120">Name</span></span>       | <span data-ttu-id="0b5f2-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="0b5f2-121">Type</span></span> | <span data-ttu-id="0b5f2-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b5f2-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="0b5f2-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="0b5f2-123">Authorization</span></span>  | <span data-ttu-id="0b5f2-124">string</span><span class="sxs-lookup"><span data-stu-id="0b5f2-124">string</span></span>  | <span data-ttu-id="0b5f2-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-p103">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="0b5f2-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0b5f2-127">Response</span></span>

<span data-ttu-id="0b5f2-p104">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-p104">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0b5f2-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0b5f2-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="0b5f2-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0b5f2-131">Request</span></span>
<span data-ttu-id="0b5f2-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_page"
}-->
```http
DELETE https://graph.microsoft.com/beta/me/onenote/pages/{id}
```
##### <a name="response"></a><span data-ttu-id="0b5f2-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0b5f2-133">Response</span></span>
<span data-ttu-id="0b5f2-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0b5f2-134">Here is an example of the response.</span></span>
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