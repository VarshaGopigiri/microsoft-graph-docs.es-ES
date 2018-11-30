---
title: Eliminar outlookTaskGroup
description: Eliminar el outlookTaskGroup especificado.
ms.openlocfilehash: c700b104db6c89d9b762ca7d6f7dc571d430878d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089570"
---
# <a name="delete-outlooktaskgroup"></a><span data-ttu-id="e1c5f-103">Eliminar outlookTaskGroup</span><span class="sxs-lookup"><span data-stu-id="e1c5f-103">Delete outlookTaskGroup</span></span>

> <span data-ttu-id="e1c5f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e1c5f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e1c5f-106">Eliminar el especificado [outlookTaskGroup](../resources/outlooktaskgroup.md).</span><span class="sxs-lookup"><span data-stu-id="e1c5f-106">Delete the specified [outlookTaskGroup](../resources/outlooktaskgroup.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="e1c5f-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="e1c5f-107">Permissions</span></span>
<span data-ttu-id="e1c5f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e1c5f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e1c5f-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e1c5f-110">Permission type</span></span>      | <span data-ttu-id="e1c5f-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e1c5f-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e1c5f-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e1c5f-112">Delegated (work or school account)</span></span> | <span data-ttu-id="e1c5f-113">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e1c5f-113">Tasks.ReadWrite</span></span>    |
|<span data-ttu-id="e1c5f-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e1c5f-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e1c5f-115">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e1c5f-115">Tasks.ReadWrite</span></span>    |
|<span data-ttu-id="e1c5f-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e1c5f-116">Application</span></span> | <span data-ttu-id="e1c5f-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="e1c5f-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e1c5f-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /users/{id|userPrincipalName}/outlook/taskGroups/{id}

```
## <a name="request-headers"></a><span data-ttu-id="e1c5f-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e1c5f-119">Request headers</span></span>
| <span data-ttu-id="e1c5f-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="e1c5f-120">Name</span></span>       | <span data-ttu-id="e1c5f-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1c5f-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="e1c5f-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="e1c5f-122">Authorization</span></span>  | <span data-ttu-id="e1c5f-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e1c5f-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e1c5f-125">Request body</span></span>
<span data-ttu-id="e1c5f-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e1c5f-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e1c5f-127">Response</span></span>

<span data-ttu-id="e1c5f-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e1c5f-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e1c5f-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e1c5f-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e1c5f-131">Request</span></span>
<span data-ttu-id="e1c5f-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_outlooktaskgroup"
}-->
```http
DELETE https://graph.microsoft.com/beta/me/outlook/taskgroups('AAMkADIyAAAhrbe-AAA=')
```
##### <a name="response"></a><span data-ttu-id="e1c5f-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e1c5f-133">Response</span></span>
<span data-ttu-id="e1c5f-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e1c5f-134">Here is an example of the response.</span></span>
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
  "description": "Delete outlookTaskGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->