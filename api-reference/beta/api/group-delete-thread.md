---
title: Eliminar hilo de conversación
description: Elimina un objeto de conversación.
author: dkershaw10
localization_priority: Normal
ms.openlocfilehash: 0b70cd880ed8e14291faa466431628011e01922a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27837600"
---
# <a name="delete-conversation-thread"></a><span data-ttu-id="0a2aa-103">Eliminar hilo de conversación</span><span class="sxs-lookup"><span data-stu-id="0a2aa-103">Delete conversation thread</span></span>

> <span data-ttu-id="0a2aa-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0a2aa-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0a2aa-106">Elimina un objeto de [conversación](../resources/conversationthread.md).</span><span class="sxs-lookup"><span data-stu-id="0a2aa-106">Delete a [thread](../resources/conversationthread.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="0a2aa-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="0a2aa-107">Permissions</span></span>
<span data-ttu-id="0a2aa-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0a2aa-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0a2aa-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0a2aa-110">Permission type</span></span>      | <span data-ttu-id="0a2aa-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0a2aa-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0a2aa-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0a2aa-112">Delegated (work or school account)</span></span> | <span data-ttu-id="0a2aa-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0a2aa-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="0a2aa-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0a2aa-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0a2aa-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-115">Not supported.</span></span>    |
|<span data-ttu-id="0a2aa-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0a2aa-116">Application</span></span> | <span data-ttu-id="0a2aa-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="0a2aa-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0a2aa-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/threads/{id}
```

## <a name="request-headers"></a><span data-ttu-id="0a2aa-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0a2aa-119">Request headers</span></span>
| <span data-ttu-id="0a2aa-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="0a2aa-120">Name</span></span>       | <span data-ttu-id="0a2aa-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="0a2aa-121">Type</span></span> | <span data-ttu-id="0a2aa-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a2aa-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="0a2aa-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="0a2aa-123">Authorization</span></span>  | <span data-ttu-id="0a2aa-124">string</span><span class="sxs-lookup"><span data-stu-id="0a2aa-124">string</span></span>  | <span data-ttu-id="0a2aa-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="0a2aa-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0a2aa-127">Request body</span></span>
<span data-ttu-id="0a2aa-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0a2aa-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0a2aa-129">Response</span></span>
<span data-ttu-id="0a2aa-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0a2aa-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0a2aa-132">Example</span></span>
#### <a name="request"></a><span data-ttu-id="0a2aa-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0a2aa-133">Request</span></span>
<span data-ttu-id="0a2aa-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-134">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_group_thread"
}-->
```http
DELETE https://graph.microsoft.com/beta/groups/02bd9fd6-8f93-4758-87c3-1fb73740a315/threads/AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgMkABAAG5c7eC4NYEynIoXsuxXB9RAAG5c7eC4NYEynIoXsuxXB9Q==
```

#### <a name="response"></a><span data-ttu-id="0a2aa-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0a2aa-135">Response</span></span>
<span data-ttu-id="0a2aa-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-136">The following is an example of the response.</span></span> 
><span data-ttu-id="0a2aa-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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
