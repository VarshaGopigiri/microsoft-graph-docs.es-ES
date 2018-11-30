---
title: Eliminar hilo de conversación
description: Elimina un objeto de conversación.
ms.openlocfilehash: 31a3386c8ff3da0ff1e81ddc2770adae0004b5c5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085602"
---
# <a name="delete-conversation-thread"></a><span data-ttu-id="76f3c-103">Eliminar hilo de conversación</span><span class="sxs-lookup"><span data-stu-id="76f3c-103">Delete conversation thread</span></span>

> <span data-ttu-id="76f3c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="76f3c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="76f3c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="76f3c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="76f3c-106">Elimina un objeto de [conversación](../resources/conversationthread.md).</span><span class="sxs-lookup"><span data-stu-id="76f3c-106">Delete a [thread](../resources/conversationthread.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="76f3c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="76f3c-107">Permissions</span></span>
<span data-ttu-id="76f3c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="76f3c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="76f3c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="76f3c-110">Permission type</span></span>      | <span data-ttu-id="76f3c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="76f3c-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="76f3c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="76f3c-112">Delegated (work or school account)</span></span> | <span data-ttu-id="76f3c-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="76f3c-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="76f3c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="76f3c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="76f3c-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="76f3c-115">Not supported.</span></span>    |
|<span data-ttu-id="76f3c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="76f3c-116">Application</span></span> | <span data-ttu-id="76f3c-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="76f3c-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="76f3c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="76f3c-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/threads/{id}
```

## <a name="request-headers"></a><span data-ttu-id="76f3c-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="76f3c-119">Request headers</span></span>
| <span data-ttu-id="76f3c-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="76f3c-120">Name</span></span>       | <span data-ttu-id="76f3c-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="76f3c-121">Type</span></span> | <span data-ttu-id="76f3c-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="76f3c-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="76f3c-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="76f3c-123">Authorization</span></span>  | <span data-ttu-id="76f3c-124">string</span><span class="sxs-lookup"><span data-stu-id="76f3c-124">string</span></span>  | <span data-ttu-id="76f3c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="76f3c-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="76f3c-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="76f3c-127">Request body</span></span>
<span data-ttu-id="76f3c-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="76f3c-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="76f3c-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="76f3c-129">Response</span></span>
<span data-ttu-id="76f3c-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="76f3c-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="76f3c-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="76f3c-132">Example</span></span>
#### <a name="request"></a><span data-ttu-id="76f3c-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="76f3c-133">Request</span></span>
<span data-ttu-id="76f3c-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="76f3c-134">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_group_thread"
}-->
```http
DELETE https://graph.microsoft.com/beta/groups/02bd9fd6-8f93-4758-87c3-1fb73740a315/threads/AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgMkABAAG5c7eC4NYEynIoXsuxXB9RAAG5c7eC4NYEynIoXsuxXB9Q==
```

#### <a name="response"></a><span data-ttu-id="76f3c-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="76f3c-135">Response</span></span>
<span data-ttu-id="76f3c-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="76f3c-136">The following is an example of the response.</span></span> 
><span data-ttu-id="76f3c-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="76f3c-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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