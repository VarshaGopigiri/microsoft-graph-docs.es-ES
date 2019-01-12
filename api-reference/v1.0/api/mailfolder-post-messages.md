---
title: Create Message
description: Usa esta API para crear un objeto Message en una mailfolder.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 50eac4d20ff5ce82298b74dbfff2da510bd49a27
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27920712"
---
# <a name="create-message"></a><span data-ttu-id="76efe-103">Create Message</span><span class="sxs-lookup"><span data-stu-id="76efe-103">Create Message</span></span>

<span data-ttu-id="76efe-104">Usa esta API para crear un objeto Message en una mailfolder.</span><span class="sxs-lookup"><span data-stu-id="76efe-104">Use this API to create a new Message in a mailfolder.</span></span>
## <a name="permissions"></a><span data-ttu-id="76efe-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="76efe-105">Permissions</span></span>
<span data-ttu-id="76efe-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="76efe-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="76efe-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="76efe-108">Permission type</span></span>      | <span data-ttu-id="76efe-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="76efe-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="76efe-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="76efe-110">Delegated (work or school account)</span></span> | <span data-ttu-id="76efe-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="76efe-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="76efe-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="76efe-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="76efe-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="76efe-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="76efe-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="76efe-114">Application</span></span> | <span data-ttu-id="76efe-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="76efe-115">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="76efe-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="76efe-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/mailFolders/{id}/messages
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages
```
## <a name="request-headers"></a><span data-ttu-id="76efe-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="76efe-117">Request headers</span></span>
| <span data-ttu-id="76efe-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="76efe-118">Header</span></span>       | <span data-ttu-id="76efe-119">Valor</span><span class="sxs-lookup"><span data-stu-id="76efe-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="76efe-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="76efe-120">Authorization</span></span>  | <span data-ttu-id="76efe-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="76efe-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="76efe-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="76efe-123">Content-Type</span></span>  | <span data-ttu-id="76efe-p103">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="76efe-p103">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="76efe-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="76efe-126">Request body</span></span>
<span data-ttu-id="76efe-127">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Message](../resources/message.md).</span><span class="sxs-lookup"><span data-stu-id="76efe-127">In the request body, supply a JSON representation of [Message](../resources/message.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="76efe-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="76efe-128">Response</span></span>

<span data-ttu-id="76efe-129">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [Message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="76efe-129">If successful, this method returns `201 Created` response code and [Message](../resources/message.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="76efe-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="76efe-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="76efe-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="76efe-131">Request</span></span>
<span data-ttu-id="76efe-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="76efe-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_message_from_mailfolder"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/mailFolders/{id}/messages
Content-type: application/json
Content-length: 248

{
  "receivedDateTime": "datetime-value",
  "sentDateTime": "datetime-value",
  "hasAttachments": true,
  "subject": "subject-value",
  "body": {
    "contentType": "",
    "content": "content-value"
  },
  "bodyPreview": "bodyPreview-value"
}
```
<span data-ttu-id="76efe-133">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [message](../resources/message.md).</span><span class="sxs-lookup"><span data-stu-id="76efe-133">In the request body, supply a JSON representation of [message](../resources/message.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="76efe-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="76efe-134">Response</span></span>
<span data-ttu-id="76efe-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="76efe-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "receivedDateTime": "datetime-value",
  "sentDateTime": "datetime-value",
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
