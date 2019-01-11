---
title: Eliminar página
description: Elimine una página de OneNote.
localization_priority: Normal
ms.openlocfilehash: 5721f06f34be48f0c8a3126d82e858aa833d3e77
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27853553"
---
# <a name="delete-page"></a><span data-ttu-id="cd7f9-103">Eliminar página</span><span class="sxs-lookup"><span data-stu-id="cd7f9-103">Delete page</span></span>

> <span data-ttu-id="cd7f9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cd7f9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cd7f9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cd7f9-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="cd7f9-106">Elimine una página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="cd7f9-106">Delete a OneNote page.</span></span>
## <a name="permissions"></a><span data-ttu-id="cd7f9-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="cd7f9-107">Permissions</span></span>
<span data-ttu-id="cd7f9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cd7f9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cd7f9-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cd7f9-110">Permission type</span></span>      | <span data-ttu-id="cd7f9-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cd7f9-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="cd7f9-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cd7f9-112">Delegated (work or school account)</span></span> | <span data-ttu-id="cd7f9-113">Notes.ReadWrite, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cd7f9-113">Notes.ReadWrite, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="cd7f9-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cd7f9-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cd7f9-115">Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cd7f9-115">Notes.ReadWrite</span></span>    |
|<span data-ttu-id="cd7f9-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cd7f9-116">Application</span></span> | <span data-ttu-id="cd7f9-117">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cd7f9-117">Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="cd7f9-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cd7f9-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/onenote/pages/{id}
DELETE /users/{id | userPrincipalName}/onenote/pages/{id}
DELETE /groups/{id}/onenote/pages/{id}
DELETE /sites/{id}/onenote/pages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="cd7f9-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cd7f9-119">Request headers</span></span>
| <span data-ttu-id="cd7f9-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="cd7f9-120">Name</span></span>       | <span data-ttu-id="cd7f9-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd7f9-121">Type</span></span> | <span data-ttu-id="cd7f9-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd7f9-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="cd7f9-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="cd7f9-123">Authorization</span></span>  | <span data-ttu-id="cd7f9-124">string</span><span class="sxs-lookup"><span data-stu-id="cd7f9-124">string</span></span>  | <span data-ttu-id="cd7f9-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cd7f9-p103">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="cd7f9-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cd7f9-127">Response</span></span>

<span data-ttu-id="cd7f9-p104">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cd7f9-p104">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cd7f9-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd7f9-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="cd7f9-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cd7f9-131">Request</span></span>
<span data-ttu-id="cd7f9-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cd7f9-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_page"
}-->
```http
DELETE https://graph.microsoft.com/beta/me/onenote/pages/{id}
```
##### <a name="response"></a><span data-ttu-id="cd7f9-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cd7f9-133">Response</span></span>
<span data-ttu-id="cd7f9-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cd7f9-134">Here is an example of the response.</span></span>
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
