---
title: Eliminar conversation
description: Elimina la conversación.
author: dkershaw10
localization_priority: Normal
ms.prod: groups
ms.openlocfilehash: addcbcafb0b19447133a75427d98e3500990f365
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27941019"
---
# <a name="delete-conversation"></a><span data-ttu-id="b5356-103">Eliminar conversación</span><span class="sxs-lookup"><span data-stu-id="b5356-103">Delete conversation</span></span>

> <span data-ttu-id="b5356-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b5356-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b5356-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b5356-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b5356-106">Elimina la conversación.</span><span class="sxs-lookup"><span data-stu-id="b5356-106">Delete conversation.</span></span>
## <a name="permissions"></a><span data-ttu-id="b5356-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="b5356-107">Permissions</span></span>
<span data-ttu-id="b5356-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b5356-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b5356-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b5356-110">Permission type</span></span>      | <span data-ttu-id="b5356-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b5356-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b5356-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b5356-112">Delegated (work or school account)</span></span> | <span data-ttu-id="b5356-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b5356-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="b5356-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b5356-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b5356-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b5356-115">Not supported.</span></span>    |
|<span data-ttu-id="b5356-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b5356-116">Application</span></span> | <span data-ttu-id="b5356-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b5356-117">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="b5356-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b5356-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/conversations/{id}
```
## <a name="request-headers"></a><span data-ttu-id="b5356-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b5356-119">Request headers</span></span>
| <span data-ttu-id="b5356-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5356-120">Header</span></span>       | <span data-ttu-id="b5356-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b5356-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="b5356-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="b5356-122">Authorization</span></span>  | <span data-ttu-id="b5356-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b5356-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b5356-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b5356-125">Request body</span></span>
<span data-ttu-id="b5356-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b5356-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b5356-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b5356-127">Response</span></span>

<span data-ttu-id="b5356-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b5356-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b5356-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b5356-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b5356-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b5356-131">Request</span></span>
<span data-ttu-id="b5356-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b5356-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_conversation"
}-->
```http
DELETE https://graph.microsoft.com/beta/groups/{id}/conversations/{id}
```
##### <a name="response"></a><span data-ttu-id="b5356-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b5356-133">Response</span></span>
<span data-ttu-id="b5356-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b5356-134">Here is an example of the response.</span></span> 
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
