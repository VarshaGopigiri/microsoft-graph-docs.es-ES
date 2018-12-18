---
title: Delete conversationThread
description: Elimina conversationThread.
author: dkershaw10
ms.openlocfilehash: ef0f9e4eae22058c93b093a2758819e60299d4fa
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27316460"
---
# <a name="delete-conversationthread"></a><span data-ttu-id="bc4d6-103">Delete conversationThread</span><span class="sxs-lookup"><span data-stu-id="bc4d6-103">Delete conversationThread</span></span>

> <span data-ttu-id="bc4d6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bc4d6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bc4d6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bc4d6-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="bc4d6-106">Elimina conversationThread.</span><span class="sxs-lookup"><span data-stu-id="bc4d6-106">Delete conversationThread.</span></span>
## <a name="permissions"></a><span data-ttu-id="bc4d6-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="bc4d6-107">Permissions</span></span>
<span data-ttu-id="bc4d6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bc4d6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bc4d6-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bc4d6-110">Permission type</span></span>      | <span data-ttu-id="bc4d6-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bc4d6-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bc4d6-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bc4d6-112">Delegated (work or school account)</span></span> | <span data-ttu-id="bc4d6-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bc4d6-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="bc4d6-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bc4d6-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bc4d6-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bc4d6-115">Not supported.</span></span>    |
|<span data-ttu-id="bc4d6-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bc4d6-116">Application</span></span> | <span data-ttu-id="bc4d6-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bc4d6-117">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="bc4d6-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bc4d6-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/threads/{id}
DELETE /groups/{id}/conversations/{id}/threads/{id}

```
## <a name="request-headers"></a><span data-ttu-id="bc4d6-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bc4d6-119">Request headers</span></span>
| <span data-ttu-id="bc4d6-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc4d6-120">Header</span></span>       | <span data-ttu-id="bc4d6-121">Valor</span><span class="sxs-lookup"><span data-stu-id="bc4d6-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="bc4d6-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="bc4d6-122">Authorization</span></span>  | <span data-ttu-id="bc4d6-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bc4d6-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="bc4d6-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bc4d6-125">Request body</span></span>
<span data-ttu-id="bc4d6-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bc4d6-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bc4d6-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bc4d6-127">Response</span></span>

<span data-ttu-id="bc4d6-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bc4d6-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bc4d6-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bc4d6-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="bc4d6-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bc4d6-131">Request</span></span>
<span data-ttu-id="bc4d6-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bc4d6-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_conversationthread"
}-->
```http
DELETE https://graph.microsoft.com/beta/groups/{id}/threads/{id}
```
##### <a name="response"></a><span data-ttu-id="bc4d6-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bc4d6-133">Response</span></span>
<span data-ttu-id="bc4d6-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bc4d6-134">Here is an example of the response.</span></span> 
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
  "description": "Delete conversationThread",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->