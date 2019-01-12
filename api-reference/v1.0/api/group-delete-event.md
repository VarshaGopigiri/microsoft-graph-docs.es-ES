---
title: Eliminar evento
description: Elimina un objeto de evento.
author: dkershaw10
localization_priority: Normal
ms.prod: groups
ms.openlocfilehash: 21f8d0579d9e78f180711998e455d360fd68dcaa
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27987394"
---
# <a name="delete-event"></a><span data-ttu-id="815ff-103">Eliminar evento</span><span class="sxs-lookup"><span data-stu-id="815ff-103">Delete event</span></span>
<span data-ttu-id="815ff-104">Elimina un objeto de [evento](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="815ff-104">Delete an [event](../resources/event.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="815ff-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="815ff-105">Permissions</span></span>
<span data-ttu-id="815ff-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="815ff-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="815ff-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="815ff-108">Permission type</span></span>      | <span data-ttu-id="815ff-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="815ff-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="815ff-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="815ff-110">Delegated (work or school account)</span></span> | <span data-ttu-id="815ff-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="815ff-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="815ff-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="815ff-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="815ff-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="815ff-113">Not supported.</span></span>    |
|<span data-ttu-id="815ff-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="815ff-114">Application</span></span> | <span data-ttu-id="815ff-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="815ff-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="815ff-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="815ff-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/events/{id}
DELETE /groups/{id}/calendar/events/{id}
```

## <a name="request-headers"></a><span data-ttu-id="815ff-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="815ff-117">Request headers</span></span>
| <span data-ttu-id="815ff-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="815ff-118">Name</span></span>       | <span data-ttu-id="815ff-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="815ff-119">Type</span></span> | <span data-ttu-id="815ff-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="815ff-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="815ff-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="815ff-121">Authorization</span></span>  | <span data-ttu-id="815ff-122">string</span><span class="sxs-lookup"><span data-stu-id="815ff-122">string</span></span>  | <span data-ttu-id="815ff-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="815ff-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="815ff-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="815ff-125">Request body</span></span>
<span data-ttu-id="815ff-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="815ff-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="815ff-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="815ff-127">Response</span></span>
<span data-ttu-id="815ff-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="815ff-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="815ff-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="815ff-130">Example</span></span>
#### <a name="request"></a><span data-ttu-id="815ff-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="815ff-131">Request</span></span>
<span data-ttu-id="815ff-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="815ff-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["02bd9fd6-8f93-4758-87c3-1fb73740a315", "AQMkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NwAzZWYARgAAA_b2VnUAiWNLj0xeSOs499YHAMT2RdsuOqRIlQZ4vOzp66YAAAIBDQAAAMT2RdsuOqRIlQZ4vOzp66YAAAIJOgAAAA=="],
  "name": "delete_group_event"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groups/02bd9fd6-8f93-4758-87c3-1fb73740a315/events/AQMkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NwAzZWYARgAAA_b2VnUAiWNLj0xeSOs499YHAMT2RdsuOqRIlQZ4vOzp66YAAAIBDQAAAMT2RdsuOqRIlQZ4vOzp66YAAAIJOgAAAA==
```

#### <a name="response"></a><span data-ttu-id="815ff-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="815ff-133">Response</span></span>
<span data-ttu-id="815ff-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="815ff-134">The following is an example of the response.</span></span> 
><span data-ttu-id="815ff-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="815ff-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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
  "description": "Delete event",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
