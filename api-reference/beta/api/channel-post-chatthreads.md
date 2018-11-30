---
title: Crear un subproceso de chat
description: Crear un nuevo subproceso de chat en el canal especificado mediante el suministro de los mensajes de raíz.
ms.openlocfilehash: 9a2a35a086c6689d1b76a56b70cd3637ec23c3a4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083354"
---
# <a name="create-chat-thread"></a><span data-ttu-id="6409c-103">Crear un subproceso de chat</span><span class="sxs-lookup"><span data-stu-id="6409c-103">Create chat thread</span></span>

> <span data-ttu-id="6409c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6409c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6409c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6409c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6409c-106">Crear un nuevo subproceso de chat en el [canal](../resources/channel.md) de especificado mediante el suministro de los mensajes de raíz.</span><span class="sxs-lookup"><span data-stu-id="6409c-106">Create a new chat thread in the specified [channel](../resources/channel.md) by supplying the root messages.</span></span>

## <a name="permissions"></a><span data-ttu-id="6409c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="6409c-107">Permissions</span></span>
<span data-ttu-id="6409c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6409c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6409c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6409c-110">Permission type</span></span>      | <span data-ttu-id="6409c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6409c-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6409c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6409c-112">Delegated (work or school account)</span></span> | <span data-ttu-id="6409c-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6409c-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="6409c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6409c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6409c-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6409c-115">Not supported.</span></span>    |
|<span data-ttu-id="6409c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6409c-116">Application</span></span> | <span data-ttu-id="6409c-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6409c-117">Not supported.</span></span> |

> <span data-ttu-id="6409c-118">Actualmente, se admiten sólo [delegar permisos](/graph/permissions-reference) para esta operación.</span><span class="sxs-lookup"><span data-stu-id="6409c-118">Currently, only [delegated permissions](/graph/permissions-reference) are supported for this operation.</span></span>  <span data-ttu-id="6409c-119">Versiones futuras será compatible con los permisos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6409c-119">Future releases will support application permissions.</span></span> 

## <a name="http-request"></a><span data-ttu-id="6409c-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6409c-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{id}/channels/{id}/chatThreads
```
## <a name="request-headers"></a><span data-ttu-id="6409c-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6409c-121">Request headers</span></span>
| <span data-ttu-id="6409c-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="6409c-122">Name</span></span>       | <span data-ttu-id="6409c-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="6409c-123">Type</span></span> | <span data-ttu-id="6409c-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="6409c-124">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="6409c-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="6409c-125">Authorization</span></span>  | <span data-ttu-id="6409c-126">string</span><span class="sxs-lookup"><span data-stu-id="6409c-126">string</span></span>  | <span data-ttu-id="6409c-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6409c-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6409c-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6409c-129">Request body</span></span>
<span data-ttu-id="6409c-130">En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto [chatThread](../resources/chatthread.md) que contiene la propiedad rootMessage.</span><span class="sxs-lookup"><span data-stu-id="6409c-130">In the request body, supply a JSON representation of a [chatThread](../resources/chatthread.md) object that contains the rootMessage property.</span></span>

## <a name="response"></a><span data-ttu-id="6409c-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6409c-131">Response</span></span>

<span data-ttu-id="6409c-132">Si tiene éxito, este método devuelve `201 Created` código de respuesta con un cuerpo de respuesta vacío.</span><span class="sxs-lookup"><span data-stu-id="6409c-132">If successful, this method returns `201 Created` response code with an empty reponse body.</span></span>

## <a name="example"></a><span data-ttu-id="6409c-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6409c-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6409c-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6409c-134">Request</span></span>
<span data-ttu-id="6409c-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6409c-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_chatthread_from_channel"
}-->
```http
POST https://graph.microsoft.com/beta/teams/{id}/channels/{id}/chatThreads
Content-type: application/json

{
  "rootMessage": {
      "body": {
        "contentType": 1,
        "content": "<h1>Hello world</h1>"
      }
  }
}
```

> <span data-ttu-id="6409c-136">Actualmente, el contentType debe especificarse como un número entero en lugar de una cadena: 0 para "text" o 1 para "html".</span><span class="sxs-lookup"><span data-stu-id="6409c-136">Currently, the contentType must be specified as an integer rather than a string: 0 for "text" or 1 for "html".</span></span>  <span data-ttu-id="6409c-137">Versiones futuras de API va a solucionar este problema.</span><span class="sxs-lookup"><span data-stu-id="6409c-137">Future API releases will fix this.</span></span>

##### <a name="response"></a><span data-ttu-id="6409c-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6409c-138">Response</span></span>

<span data-ttu-id="6409c-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6409c-139">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chatThread"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 160

{
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create thread",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
