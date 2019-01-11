---
title: Create acceptedSender
description: Agrega un nuevo usuario o grupo a la lista de acceptedSender.
author: dkershaw10
localization_priority: Normal
ms.openlocfilehash: d450d7441429f6e40477570609a9b9689ebc0a28
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27843466"
---
# <a name="create-acceptedsender"></a><span data-ttu-id="db73c-103">Create acceptedSender</span><span class="sxs-lookup"><span data-stu-id="db73c-103">Create acceptedSender</span></span>

> <span data-ttu-id="db73c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="db73c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="db73c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="db73c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="db73c-106">Agrega un nuevo usuario o grupo a la lista de acceptedSender.</span><span class="sxs-lookup"><span data-stu-id="db73c-106">Add a new user or group to the acceptedSender list.</span></span>

<span data-ttu-id="db73c-p102">En el cuerpo de la solicitud, especifique el usuario o grupo en `@odata.id`. Los usuarios de la lista de remitentes aceptados pueden publicar conversaciones del grupo. Asegúrese de no especificar el mismo usuario o grupo en las listas de remitentes aceptados y de remitentes rechazados, de lo contrario se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="db73c-p102">Specify the user or group in `@odata.id` in the request body. Users in the accepted senders list can post to conversations of the group . Make sure you do not specify the same user or group in the accepted senders and rejected senders lists, otherwise you will get an error.</span></span>

## <a name="permissions"></a><span data-ttu-id="db73c-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="db73c-110">Permissions</span></span>
<span data-ttu-id="db73c-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="db73c-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="db73c-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="db73c-113">Permission type</span></span>      | <span data-ttu-id="db73c-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="db73c-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="db73c-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="db73c-115">Delegated (work or school account)</span></span> | <span data-ttu-id="db73c-116">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="db73c-116">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="db73c-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="db73c-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="db73c-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="db73c-118">Not supported.</span></span>    |
|<span data-ttu-id="db73c-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="db73c-119">Application</span></span> | <span data-ttu-id="db73c-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="db73c-120">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="db73c-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="db73c-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/acceptedSenders/$ref
```
## <a name="request-headers"></a><span data-ttu-id="db73c-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="db73c-122">Request headers</span></span>
| <span data-ttu-id="db73c-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db73c-123">Header</span></span>       | <span data-ttu-id="db73c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="db73c-124">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="db73c-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="db73c-125">Authorization</span></span>  | <span data-ttu-id="db73c-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="db73c-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="db73c-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="db73c-128">Request body</span></span>
<span data-ttu-id="db73c-129">En el cuerpo de la solicitud, proporcione el identificador de un objeto de usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="db73c-129">In the request body, supply the id of a user or group object.</span></span>

## <a name="response"></a><span data-ttu-id="db73c-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="db73c-130">Response</span></span>
<span data-ttu-id="db73c-131">Este método devuelve el código de respuesta `204 No Content` y ningún cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="db73c-131">This method returns `204 No Content` response code and no response body.</span></span>

## <a name="example"></a><span data-ttu-id="db73c-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="db73c-132">Example</span></span>
#### <a name="request"></a><span data-ttu-id="db73c-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="db73c-133">Request</span></span>
<span data-ttu-id="db73c-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="db73c-134">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_acceptedsender"
}-->
```http
POST https://graph.microsoft.com/beta/groups/{id}/acceptedSenders/$ref
Content-type: application/json
Content-length: 30

{
  "@odata.id":"https://graph.microsoft.com/beta/users/alexd@contoso.com"
}
```

#### <a name="response"></a><span data-ttu-id="db73c-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="db73c-135">Response</span></span>
<span data-ttu-id="db73c-136">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="db73c-136">The following is an example of the response.</span></span>
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
  "description": "Create acceptedSender",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
