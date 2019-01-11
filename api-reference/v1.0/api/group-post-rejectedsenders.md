---
title: Create rejectedSender
description: Agrega un nuevo usuario o grupo a la lista de rejectedSender.
author: dkershaw10
localization_priority: Normal
ms.openlocfilehash: dbdf31c34fb9934ff705bc8d2be03efda8f4de12
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27826918"
---
# <a name="create-rejectedsender"></a><span data-ttu-id="ecdb7-103">Create rejectedSender</span><span class="sxs-lookup"><span data-stu-id="ecdb7-103">Create rejectedSender</span></span>
<span data-ttu-id="ecdb7-104">Agrega un nuevo usuario o grupo a la lista de rejectedSender.</span><span class="sxs-lookup"><span data-stu-id="ecdb7-104">Add a new user or group to the rejectedSender list.</span></span>

<span data-ttu-id="ecdb7-p101">En el cuerpo de la solicitud, especifique el usuario o grupo en `@odata.id`. Los usuarios de la lista de remitentes rechazados no pueden publicar conversaciones del grupo (identificado en la dirección URL de solicitud POST). Asegúrese de no especificar el mismo usuario o grupo en las listas de remitentes rechazados y de remitentes aceptados, de lo contrario se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="ecdb7-p101">Specify the user or group in `@odata.id` in the request body. Users in the rejected senders list cannot post to conversations of the group (identified in the POST request URL). Make sure you do not specify the same user or group in the rejected senders and accepted senders lists, otherwise you will get an error.</span></span>

## <a name="permissions"></a><span data-ttu-id="ecdb7-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="ecdb7-108">Permissions</span></span>
<span data-ttu-id="ecdb7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ecdb7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ecdb7-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ecdb7-111">Permission type</span></span>      | <span data-ttu-id="ecdb7-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ecdb7-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ecdb7-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ecdb7-113">Delegated (work or school account)</span></span> | <span data-ttu-id="ecdb7-114">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ecdb7-114">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="ecdb7-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ecdb7-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ecdb7-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ecdb7-116">Not supported.</span></span>    |
|<span data-ttu-id="ecdb7-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ecdb7-117">Application</span></span> | <span data-ttu-id="ecdb7-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ecdb7-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="ecdb7-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ecdb7-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/rejectedSenders/$ref
```
## <a name="request-headers"></a><span data-ttu-id="ecdb7-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ecdb7-120">Request headers</span></span>
| <span data-ttu-id="ecdb7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ecdb7-121">Header</span></span>       | <span data-ttu-id="ecdb7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ecdb7-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ecdb7-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="ecdb7-123">Authorization</span></span>  | <span data-ttu-id="ecdb7-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ecdb7-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ecdb7-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ecdb7-126">Request body</span></span>
<span data-ttu-id="ecdb7-127">En el cuerpo de la solicitud, proporcione el identificador de un objeto de usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="ecdb7-127">In the request body, supply the id of a user or group object.</span></span>

## <a name="response"></a><span data-ttu-id="ecdb7-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ecdb7-128">Response</span></span>
<span data-ttu-id="ecdb7-129">Este método devuelve el código de respuesta `204 No Content` y ningún cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ecdb7-129">This method returns `204 No Content` response code and no response body.</span></span>

## <a name="example"></a><span data-ttu-id="ecdb7-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ecdb7-130">Example</span></span>
#### <a name="request"></a><span data-ttu-id="ecdb7-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ecdb7-131">Request</span></span>
<span data-ttu-id="ecdb7-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ecdb7-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_group"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/rejectedSenders/$ref
Content-type: application/json
Content-length: 30

{
  "@odata.id":"https://graph.microsoft.com/v1.0/users/alexd@contoso.com"
}
```
#### <a name="response"></a><span data-ttu-id="ecdb7-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ecdb7-133">Response</span></span>
<span data-ttu-id="ecdb7-134">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ecdb7-134">The following is an example of the response.</span></span>
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
  "description": "Create rejectedSender",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
