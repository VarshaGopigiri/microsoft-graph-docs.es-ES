---
title: Eliminar hilo de conversación
description: Elimina un objeto de conversación.
author: dkershaw10
localization_priority: Normal
ms.prod: groups
ms.openlocfilehash: f4e40763a1221575fbe45e8294aad0d2e0bdf764
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27935790"
---
# <a name="delete-conversation-thread"></a><span data-ttu-id="7dd19-103">Eliminar hilo de conversación</span><span class="sxs-lookup"><span data-stu-id="7dd19-103">Delete conversation thread</span></span>

> <span data-ttu-id="7dd19-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7dd19-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7dd19-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7dd19-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7dd19-106">Elimina un objeto de [conversación](../resources/conversationthread.md).</span><span class="sxs-lookup"><span data-stu-id="7dd19-106">Delete a [thread](../resources/conversationthread.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="7dd19-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="7dd19-107">Permissions</span></span>
<span data-ttu-id="7dd19-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7dd19-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7dd19-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7dd19-110">Permission type</span></span>      | <span data-ttu-id="7dd19-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7dd19-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7dd19-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7dd19-112">Delegated (work or school account)</span></span> | <span data-ttu-id="7dd19-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7dd19-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="7dd19-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7dd19-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7dd19-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7dd19-115">Not supported.</span></span>    |
|<span data-ttu-id="7dd19-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7dd19-116">Application</span></span> | <span data-ttu-id="7dd19-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7dd19-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="7dd19-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7dd19-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/threads/{id}
```

## <a name="request-headers"></a><span data-ttu-id="7dd19-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7dd19-119">Request headers</span></span>
| <span data-ttu-id="7dd19-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="7dd19-120">Name</span></span>       | <span data-ttu-id="7dd19-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="7dd19-121">Type</span></span> | <span data-ttu-id="7dd19-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="7dd19-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="7dd19-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="7dd19-123">Authorization</span></span>  | <span data-ttu-id="7dd19-124">string</span><span class="sxs-lookup"><span data-stu-id="7dd19-124">string</span></span>  | <span data-ttu-id="7dd19-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7dd19-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="7dd19-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7dd19-127">Request body</span></span>
<span data-ttu-id="7dd19-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7dd19-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7dd19-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7dd19-129">Response</span></span>
<span data-ttu-id="7dd19-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7dd19-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7dd19-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7dd19-132">Example</span></span>
#### <a name="request"></a><span data-ttu-id="7dd19-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7dd19-133">Request</span></span>
<span data-ttu-id="7dd19-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7dd19-134">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_group_thread"
}-->
```http
DELETE https://graph.microsoft.com/beta/groups/02bd9fd6-8f93-4758-87c3-1fb73740a315/threads/AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgMkABAAG5c7eC4NYEynIoXsuxXB9RAAG5c7eC4NYEynIoXsuxXB9Q==
```

#### <a name="response"></a><span data-ttu-id="7dd19-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7dd19-135">Response</span></span>
<span data-ttu-id="7dd19-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7dd19-136">The following is an example of the response.</span></span> 
><span data-ttu-id="7dd19-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7dd19-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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
