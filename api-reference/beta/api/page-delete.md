---
title: Eliminar página
description: Elimine una página de OneNote.
localization_priority: Normal
author: jewan-microsoft
ms.prod: onenote
ms.openlocfilehash: ec70039fe28f4a625043f678d40deff917577848
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27979659"
---
# <a name="delete-page"></a><span data-ttu-id="61228-103">Eliminar página</span><span class="sxs-lookup"><span data-stu-id="61228-103">Delete page</span></span>

> <span data-ttu-id="61228-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="61228-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="61228-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="61228-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="61228-106">Elimine una página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="61228-106">Delete a OneNote page.</span></span>
## <a name="permissions"></a><span data-ttu-id="61228-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="61228-107">Permissions</span></span>
<span data-ttu-id="61228-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="61228-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="61228-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="61228-110">Permission type</span></span>      | <span data-ttu-id="61228-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="61228-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="61228-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="61228-112">Delegated (work or school account)</span></span> | <span data-ttu-id="61228-113">Notes.ReadWrite, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="61228-113">Notes.ReadWrite, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="61228-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="61228-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="61228-115">Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="61228-115">Notes.ReadWrite</span></span>    |
|<span data-ttu-id="61228-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="61228-116">Application</span></span> | <span data-ttu-id="61228-117">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="61228-117">Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="61228-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="61228-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/onenote/pages/{id}
DELETE /users/{id | userPrincipalName}/onenote/pages/{id}
DELETE /groups/{id}/onenote/pages/{id}
DELETE /sites/{id}/onenote/pages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="61228-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="61228-119">Request headers</span></span>
| <span data-ttu-id="61228-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="61228-120">Name</span></span>       | <span data-ttu-id="61228-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="61228-121">Type</span></span> | <span data-ttu-id="61228-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="61228-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="61228-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="61228-123">Authorization</span></span>  | <span data-ttu-id="61228-124">string</span><span class="sxs-lookup"><span data-stu-id="61228-124">string</span></span>  | <span data-ttu-id="61228-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="61228-p103">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="61228-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="61228-127">Response</span></span>

<span data-ttu-id="61228-p104">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="61228-p104">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="61228-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="61228-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="61228-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="61228-131">Request</span></span>
<span data-ttu-id="61228-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="61228-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_page"
}-->
```http
DELETE https://graph.microsoft.com/beta/me/onenote/pages/{id}
```
##### <a name="response"></a><span data-ttu-id="61228-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="61228-133">Response</span></span>
<span data-ttu-id="61228-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="61228-134">Here is an example of the response.</span></span>
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
