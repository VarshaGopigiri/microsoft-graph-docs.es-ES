---
title: Create Message
description: Usa esta API para crear un objeto Message en una mailfolder.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: 3d4bd1783d5ad2e04f99e1e3d3231a0aa9bd31fb
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27878956"
---
# <a name="create-message"></a><span data-ttu-id="b54db-103">Create Message</span><span class="sxs-lookup"><span data-stu-id="b54db-103">Create Message</span></span>

> <span data-ttu-id="b54db-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b54db-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b54db-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b54db-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b54db-106">Usa esta API para crear un objeto Message en una mailfolder.</span><span class="sxs-lookup"><span data-stu-id="b54db-106">Use this API to create a new Message in a mailfolder.</span></span>
## <a name="permissions"></a><span data-ttu-id="b54db-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="b54db-107">Permissions</span></span>
<span data-ttu-id="b54db-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b54db-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b54db-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b54db-110">Permission type</span></span>      | <span data-ttu-id="b54db-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b54db-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b54db-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b54db-112">Delegated (work or school account)</span></span> | <span data-ttu-id="b54db-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b54db-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="b54db-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b54db-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b54db-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b54db-115">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="b54db-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b54db-116">Application</span></span> | <span data-ttu-id="b54db-117">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b54db-117">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="b54db-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b54db-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/mailFolders/{id}/messages
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages
```
## <a name="request-headers"></a><span data-ttu-id="b54db-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b54db-119">Request headers</span></span>
| <span data-ttu-id="b54db-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b54db-120">Header</span></span>       | <span data-ttu-id="b54db-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b54db-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="b54db-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="b54db-122">Authorization</span></span>  | <span data-ttu-id="b54db-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b54db-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="b54db-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="b54db-125">Content-Type</span></span>  | <span data-ttu-id="b54db-p104">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b54db-p104">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b54db-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b54db-128">Request body</span></span>
<span data-ttu-id="b54db-129">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Message](../resources/message.md).</span><span class="sxs-lookup"><span data-stu-id="b54db-129">In the request body, supply a JSON representation of [Message](../resources/message.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="b54db-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b54db-130">Response</span></span>

<span data-ttu-id="b54db-131">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [Message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b54db-131">If successful, this method returns `201 Created` response code and [Message](../resources/message.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b54db-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b54db-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b54db-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b54db-133">Request</span></span>
<span data-ttu-id="b54db-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b54db-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_message_from_mailfolder"
}-->
```http
POST https://graph.microsoft.com/beta/me/mailFolders/{id}/messages
Content-type: application/json
Content-length: 248

{
  "receivedDateTime": "2016-10-19T10:37:00Z",
  "sentDateTime": "2016-10-19T10:37:00Z",
  "hasAttachments": true,
  "subject": "subject-value",
  "body": {
    "contentType": "",
    "content": "content-value"
  },
  "bodyPreview": "bodyPreview-value"
}
```
<span data-ttu-id="b54db-135">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [message](../resources/message.md).</span><span class="sxs-lookup"><span data-stu-id="b54db-135">In the request body, supply a JSON representation of [message](../resources/message.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="b54db-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b54db-136">Response</span></span>
<span data-ttu-id="b54db-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b54db-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 248

{
  "receivedDateTime": "2016-10-19T10:37:00Z",
  "sentDateTime": "2016-10-19T10:37:00Z",
  "hasAttachments": true,
  "subject": "subject-value",
  "body": {
    "contentType": "",
    "content": "content-value"
  },
  "bodyPreview": "bodyPreview-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Message",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
