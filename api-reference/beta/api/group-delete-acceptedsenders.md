---
title: Remove acceptedSender
description: 'Quita un usuario o grupo de la lista de acceptedSenders. '
author: dkershaw10
ms.openlocfilehash: 7028f2f63e340c9f5c3f300f6e3724a05f87d288
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27313912"
---
# <a name="remove-acceptedsender"></a><span data-ttu-id="1a4de-103">Remove acceptedSender</span><span class="sxs-lookup"><span data-stu-id="1a4de-103">Remove acceptedSender</span></span>

> <span data-ttu-id="1a4de-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1a4de-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1a4de-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1a4de-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1a4de-106">Quita un usuario o grupo de la lista de acceptedSenders.</span><span class="sxs-lookup"><span data-stu-id="1a4de-106">Remove a user or group from the acceptedSenders list.</span></span> 

## <a name="permissions"></a><span data-ttu-id="1a4de-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="1a4de-107">Permissions</span></span>
<span data-ttu-id="1a4de-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1a4de-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="1a4de-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1a4de-110">Permission type</span></span>                        | <span data-ttu-id="1a4de-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1a4de-111">Permissions (from least to most privileged)</span></span>  |
|:---------------------------------------|:-------------------------------------------- |
| <span data-ttu-id="1a4de-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1a4de-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="1a4de-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1a4de-113">Group.ReadWrite.All</span></span>    |
| <span data-ttu-id="1a4de-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1a4de-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1a4de-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1a4de-115">Not supported.</span></span>|
| <span data-ttu-id="1a4de-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1a4de-116">Application</span></span>                            | <span data-ttu-id="1a4de-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1a4de-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1a4de-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1a4de-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/acceptedSenders/$ref?$id=<id>
```

## <a name="request-headers"></a><span data-ttu-id="1a4de-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1a4de-119">Request headers</span></span>
| <span data-ttu-id="1a4de-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1a4de-120">Header</span></span>         | <span data-ttu-id="1a4de-121">Valor</span><span class="sxs-lookup"><span data-stu-id="1a4de-121">Value</span></span>                      |
|:---------------|:---------------------------|
| <span data-ttu-id="1a4de-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="1a4de-122">Authorization</span></span>  | <span data-ttu-id="1a4de-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a4de-p103">Bearer {token}. Required.</span></span>  

## <a name="request-body"></a><span data-ttu-id="1a4de-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1a4de-125">Request body</span></span>
<span data-ttu-id="1a4de-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1a4de-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1a4de-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1a4de-127">Response</span></span>
<span data-ttu-id="1a4de-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1a4de-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1a4de-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1a4de-130">Example</span></span>
#### <a name="request"></a><span data-ttu-id="1a4de-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1a4de-131">Request</span></span>
<span data-ttu-id="1a4de-132">Estos son un par de ejemplos de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1a4de-132">The following are a couple of examples of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_group"
}-->
```http
DELETE https://graph.microsoft.com/beta/groups/{id}/acceptedSenders/$ref?$id=https://graph.microsoft.com/beta/users/{id}

DELETE https://graph.microsoft.com/beta/groups/{id}/acceptedSenders/$ref?$id=https://graph.microsoft.com/beta/groups/{id}
```

#### <a name="response"></a><span data-ttu-id="1a4de-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1a4de-133">Response</span></span>
<span data-ttu-id="1a4de-134">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1a4de-134">The following is an example of the response.</span></span> 

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