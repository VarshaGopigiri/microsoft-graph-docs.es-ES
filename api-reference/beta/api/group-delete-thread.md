---
title: Eliminar hilo de conversación
description: Elimina un objeto de conversación.
author: dkershaw10
ms.openlocfilehash: eec28f92fcdee1755b1e000225ea9458241f01c6
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27352951"
---
# <a name="delete-conversation-thread"></a><span data-ttu-id="abae6-103">Eliminar hilo de conversación</span><span class="sxs-lookup"><span data-stu-id="abae6-103">Delete conversation thread</span></span>

> <span data-ttu-id="abae6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="abae6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="abae6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="abae6-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="abae6-106">Elimina un objeto de [conversación](../resources/conversationthread.md).</span><span class="sxs-lookup"><span data-stu-id="abae6-106">Delete a [thread](../resources/conversationthread.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="abae6-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="abae6-107">Permissions</span></span>
<span data-ttu-id="abae6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="abae6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="abae6-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="abae6-110">Permission type</span></span>      | <span data-ttu-id="abae6-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="abae6-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="abae6-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="abae6-112">Delegated (work or school account)</span></span> | <span data-ttu-id="abae6-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="abae6-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="abae6-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="abae6-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="abae6-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="abae6-115">Not supported.</span></span>    |
|<span data-ttu-id="abae6-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="abae6-116">Application</span></span> | <span data-ttu-id="abae6-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="abae6-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="abae6-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="abae6-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/threads/{id}
```

## <a name="request-headers"></a><span data-ttu-id="abae6-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="abae6-119">Request headers</span></span>
| <span data-ttu-id="abae6-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="abae6-120">Name</span></span>       | <span data-ttu-id="abae6-121">Type</span><span class="sxs-lookup"><span data-stu-id="abae6-121">Type</span></span> | <span data-ttu-id="abae6-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="abae6-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="abae6-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="abae6-123">Authorization</span></span>  | <span data-ttu-id="abae6-124">string</span><span class="sxs-lookup"><span data-stu-id="abae6-124">string</span></span>  | <span data-ttu-id="abae6-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="abae6-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="abae6-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="abae6-127">Request body</span></span>
<span data-ttu-id="abae6-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="abae6-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="abae6-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="abae6-129">Response</span></span>
<span data-ttu-id="abae6-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="abae6-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="abae6-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="abae6-132">Example</span></span>
#### <a name="request"></a><span data-ttu-id="abae6-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="abae6-133">Request</span></span>
<span data-ttu-id="abae6-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="abae6-134">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_group_thread"
}-->
```http
DELETE https://graph.microsoft.com/beta/groups/02bd9fd6-8f93-4758-87c3-1fb73740a315/threads/AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgMkABAAG5c7eC4NYEynIoXsuxXB9RAAG5c7eC4NYEynIoXsuxXB9Q==
```

#### <a name="response"></a><span data-ttu-id="abae6-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="abae6-135">Response</span></span>
<span data-ttu-id="abae6-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="abae6-136">The following is an example of the response.</span></span> 
><span data-ttu-id="abae6-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="abae6-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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