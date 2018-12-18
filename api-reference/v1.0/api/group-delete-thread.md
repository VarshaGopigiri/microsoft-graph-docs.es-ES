---
title: Eliminar hilo de conversación
description: Elimina un objeto de conversación.
author: dkershaw10
ms.openlocfilehash: b8dc8d2675804fabbd6c6b5dcbb7d30ad34a211c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27339448"
---
# <a name="delete-conversation-thread"></a><span data-ttu-id="ceba3-103">Eliminar hilo de conversación</span><span class="sxs-lookup"><span data-stu-id="ceba3-103">Delete conversation thread</span></span>
<span data-ttu-id="ceba3-104">Elimina un objeto de [conversación](../resources/conversationthread.md).</span><span class="sxs-lookup"><span data-stu-id="ceba3-104">Delete a [thread](../resources/conversationthread.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="ceba3-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="ceba3-105">Permissions</span></span>
<span data-ttu-id="ceba3-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ceba3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ceba3-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ceba3-108">Permission type</span></span>      | <span data-ttu-id="ceba3-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ceba3-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ceba3-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ceba3-110">Delegated (work or school account)</span></span> | <span data-ttu-id="ceba3-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ceba3-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="ceba3-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ceba3-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ceba3-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ceba3-113">Not supported.</span></span>    |
|<span data-ttu-id="ceba3-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ceba3-114">Application</span></span> | <span data-ttu-id="ceba3-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ceba3-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="ceba3-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ceba3-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/threads/{id}
```

## <a name="request-headers"></a><span data-ttu-id="ceba3-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ceba3-117">Request headers</span></span>
| <span data-ttu-id="ceba3-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="ceba3-118">Name</span></span>       | <span data-ttu-id="ceba3-119">Type</span><span class="sxs-lookup"><span data-stu-id="ceba3-119">Type</span></span> | <span data-ttu-id="ceba3-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="ceba3-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="ceba3-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="ceba3-121">Authorization</span></span>  | <span data-ttu-id="ceba3-122">string</span><span class="sxs-lookup"><span data-stu-id="ceba3-122">string</span></span>  | <span data-ttu-id="ceba3-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ceba3-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ceba3-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ceba3-125">Request body</span></span>
<span data-ttu-id="ceba3-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ceba3-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ceba3-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ceba3-127">Response</span></span>
<span data-ttu-id="ceba3-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ceba3-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ceba3-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ceba3-130">Example</span></span>
#### <a name="request"></a><span data-ttu-id="ceba3-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ceba3-131">Request</span></span>
<span data-ttu-id="ceba3-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ceba3-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["02bd9fd6-8f93-4758-87c3-1fb73740a315", "AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgMkABAAG5c7eC4NYEynIoXsuxXB9RAAG5c7eC4NYEynIoXsuxXB9Q=="],
  "name": "delete_group_thread"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groups/02bd9fd6-8f93-4758-87c3-1fb73740a315/threads/AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgMkABAAG5c7eC4NYEynIoXsuxXB9RAAG5c7eC4NYEynIoXsuxXB9Q==
```

#### <a name="response"></a><span data-ttu-id="ceba3-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ceba3-133">Response</span></span>
<span data-ttu-id="ceba3-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ceba3-134">The following is an example of the response.</span></span> 
><span data-ttu-id="ceba3-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ceba3-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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