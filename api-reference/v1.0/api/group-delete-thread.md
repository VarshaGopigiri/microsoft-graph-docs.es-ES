---
title: Eliminar hilo de conversación
description: Elimina un objeto de conversación.
author: dkershaw10
localization_priority: Normal
ms.prod: groups
ms.openlocfilehash: 24e779b528391e82f452f7bbe3153e39a3975b93
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27946759"
---
# <a name="delete-conversation-thread"></a><span data-ttu-id="b7b02-103">Eliminar hilo de conversación</span><span class="sxs-lookup"><span data-stu-id="b7b02-103">Delete conversation thread</span></span>
<span data-ttu-id="b7b02-104">Elimina un objeto de [conversación](../resources/conversationthread.md).</span><span class="sxs-lookup"><span data-stu-id="b7b02-104">Delete a [thread](../resources/conversationthread.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="b7b02-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="b7b02-105">Permissions</span></span>
<span data-ttu-id="b7b02-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b7b02-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b7b02-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b7b02-108">Permission type</span></span>      | <span data-ttu-id="b7b02-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b7b02-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b7b02-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b7b02-110">Delegated (work or school account)</span></span> | <span data-ttu-id="b7b02-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b7b02-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="b7b02-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b7b02-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b7b02-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b7b02-113">Not supported.</span></span>    |
|<span data-ttu-id="b7b02-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b7b02-114">Application</span></span> | <span data-ttu-id="b7b02-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b7b02-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="b7b02-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b7b02-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/threads/{id}
```

## <a name="request-headers"></a><span data-ttu-id="b7b02-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b7b02-117">Request headers</span></span>
| <span data-ttu-id="b7b02-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="b7b02-118">Name</span></span>       | <span data-ttu-id="b7b02-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="b7b02-119">Type</span></span> | <span data-ttu-id="b7b02-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="b7b02-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="b7b02-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="b7b02-121">Authorization</span></span>  | <span data-ttu-id="b7b02-122">string</span><span class="sxs-lookup"><span data-stu-id="b7b02-122">string</span></span>  | <span data-ttu-id="b7b02-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b7b02-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b7b02-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b7b02-125">Request body</span></span>
<span data-ttu-id="b7b02-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b7b02-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b7b02-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b7b02-127">Response</span></span>
<span data-ttu-id="b7b02-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b7b02-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b7b02-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b7b02-130">Example</span></span>
#### <a name="request"></a><span data-ttu-id="b7b02-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b7b02-131">Request</span></span>
<span data-ttu-id="b7b02-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b7b02-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["02bd9fd6-8f93-4758-87c3-1fb73740a315", "AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgMkABAAG5c7eC4NYEynIoXsuxXB9RAAG5c7eC4NYEynIoXsuxXB9Q=="],
  "name": "delete_group_thread"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groups/02bd9fd6-8f93-4758-87c3-1fb73740a315/threads/AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgMkABAAG5c7eC4NYEynIoXsuxXB9RAAG5c7eC4NYEynIoXsuxXB9Q==
```

#### <a name="response"></a><span data-ttu-id="b7b02-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b7b02-133">Response</span></span>
<span data-ttu-id="b7b02-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b7b02-134">The following is an example of the response.</span></span> 
><span data-ttu-id="b7b02-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b7b02-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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
  "description": "Delete conversation thread",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
