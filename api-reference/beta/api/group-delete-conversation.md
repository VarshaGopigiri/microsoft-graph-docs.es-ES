---
title: Eliminar conversación
description: Elimina un objeto de conversación.
ms.openlocfilehash: d23e57f75cb52ae0c2aab6c8525bc18d4ac0f5c0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086177"
---
# <a name="delete-conversation"></a><span data-ttu-id="17790-103">Eliminar conversación</span><span class="sxs-lookup"><span data-stu-id="17790-103">Delete conversation</span></span>

> <span data-ttu-id="17790-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="17790-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="17790-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="17790-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="17790-106">Elimina un objeto de [conversación](../resources/conversation.md).</span><span class="sxs-lookup"><span data-stu-id="17790-106">Delete a [conversation](../resources/conversation.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="17790-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="17790-107">Permissions</span></span>
<span data-ttu-id="17790-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="17790-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="17790-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="17790-110">Permission type</span></span>      | <span data-ttu-id="17790-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="17790-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="17790-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="17790-112">Delegated (work or school account)</span></span> | <span data-ttu-id="17790-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="17790-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="17790-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="17790-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="17790-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="17790-115">Not supported.</span></span>    |
|<span data-ttu-id="17790-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="17790-116">Application</span></span> | <span data-ttu-id="17790-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="17790-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="17790-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="17790-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/conversations/{id}
```

## <a name="request-headers"></a><span data-ttu-id="17790-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="17790-119">Request headers</span></span>
| <span data-ttu-id="17790-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="17790-120">Name</span></span>       | <span data-ttu-id="17790-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="17790-121">Type</span></span> | <span data-ttu-id="17790-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="17790-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="17790-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="17790-123">Authorization</span></span>  | <span data-ttu-id="17790-124">string</span><span class="sxs-lookup"><span data-stu-id="17790-124">string</span></span>  | <span data-ttu-id="17790-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="17790-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="17790-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="17790-127">Request body</span></span>
<span data-ttu-id="17790-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="17790-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="17790-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="17790-129">Response</span></span>
<span data-ttu-id="17790-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="17790-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="17790-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="17790-132">Example</span></span>
#### <a name="request"></a><span data-ttu-id="17790-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="17790-133">Request</span></span>
<span data-ttu-id="17790-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="17790-134">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_group_conversation"
}-->
```http
DELETE https://graph.microsoft.com/beta/groups/02bd9fd6-8f93-4758-87c3-1fb73740a315/conversations/AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgAQABuXO3guDWBMpyKF7LsVwfU=
```

#### <a name="response"></a><span data-ttu-id="17790-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="17790-135">Response</span></span>
<span data-ttu-id="17790-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="17790-136">The following is an example of the response.</span></span> 
><span data-ttu-id="17790-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="17790-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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
  "description": "Delete conversation",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->