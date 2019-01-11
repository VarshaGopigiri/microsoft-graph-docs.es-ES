---
title: Create Message
description: Usa esta API para crear un objeto Message en una mailfolder.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: 18c72dc42d2ced2f1aaee5819598da1e28a5c8bd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27848275"
---
# <a name="create-message"></a><span data-ttu-id="61b37-103">Create Message</span><span class="sxs-lookup"><span data-stu-id="61b37-103">Create Message</span></span>

<span data-ttu-id="61b37-104">Usa esta API para crear un objeto Message en una mailfolder.</span><span class="sxs-lookup"><span data-stu-id="61b37-104">Use this API to create a new Message in a mailfolder.</span></span>
## <a name="permissions"></a><span data-ttu-id="61b37-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="61b37-105">Permissions</span></span>
<span data-ttu-id="61b37-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="61b37-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="61b37-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="61b37-108">Permission type</span></span>      | <span data-ttu-id="61b37-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="61b37-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="61b37-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="61b37-110">Delegated (work or school account)</span></span> | <span data-ttu-id="61b37-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="61b37-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="61b37-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="61b37-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="61b37-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="61b37-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="61b37-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="61b37-114">Application</span></span> | <span data-ttu-id="61b37-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="61b37-115">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="61b37-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="61b37-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/mailFolders/{id}/messages
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages
```
## <a name="request-headers"></a><span data-ttu-id="61b37-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="61b37-117">Request headers</span></span>
| <span data-ttu-id="61b37-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="61b37-118">Header</span></span>       | <span data-ttu-id="61b37-119">Valor</span><span class="sxs-lookup"><span data-stu-id="61b37-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="61b37-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="61b37-120">Authorization</span></span>  | <span data-ttu-id="61b37-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="61b37-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="61b37-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="61b37-123">Content-Type</span></span>  | <span data-ttu-id="61b37-p103">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="61b37-p103">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="61b37-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="61b37-126">Request body</span></span>
<span data-ttu-id="61b37-127">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Message](../resources/message.md).</span><span class="sxs-lookup"><span data-stu-id="61b37-127">In the request body, supply a JSON representation of [Message](../resources/message.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="61b37-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="61b37-128">Response</span></span>

<span data-ttu-id="61b37-129">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [Message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="61b37-129">If successful, this method returns `201 Created` response code and [Message](../resources/message.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="61b37-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="61b37-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="61b37-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="61b37-131">Request</span></span>
<span data-ttu-id="61b37-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="61b37-132">Here is an example of the request.</span></span>
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
<span data-ttu-id="61b37-133">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [message](../resources/message.md).</span><span class="sxs-lookup"><span data-stu-id="61b37-133">In the request body, supply a JSON representation of [message](../resources/message.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="61b37-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="61b37-134">Response</span></span>
<span data-ttu-id="61b37-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="61b37-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
