---
title: 'message: createReplyAll'
description: Cree un borrador para responder al remitente y a todos los destinatarios del mensaje especificado. Después, puede actualizar el borrador para agregar el contenido de la respuesta al **cuerpo**, cambiar otras propiedades del mensaje o, simplemente, enviar el borrador.
localization_priority: Normal
ms.openlocfilehash: d09de032dc515173219a00b19a64d64ba0b72195
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27804784"
---
# <a name="message-createreplyall"></a><span data-ttu-id="fb957-104">message: createReplyAll</span><span class="sxs-lookup"><span data-stu-id="fb957-104">message: createReplyAll</span></span>

<span data-ttu-id="fb957-105">Cree un borrador para responder al remitente y a todos los destinatarios del [mensaje](../resources/message.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="fb957-105">Create a draft to reply to the sender and all the recipients of the specified [message](../resources/message.md).</span></span> <span data-ttu-id="fb957-106">Después, puede [actualizar](../api/message-update.md) el borrador para agregar el contenido de la respuesta al **cuerpo**, cambiar otras propiedades del mensaje o, simplemente, [enviar](../api/message-send.md) el borrador.</span><span class="sxs-lookup"><span data-stu-id="fb957-106">You can then [update](../api/message-update.md) the draft to add reply content to the **body** or change other message properties, or, simply [send](../api/message-send.md) the draft.</span></span>

## <a name="permissions"></a><span data-ttu-id="fb957-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="fb957-107">Permissions</span></span>
<span data-ttu-id="fb957-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fb957-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fb957-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fb957-110">Permission type</span></span>      | <span data-ttu-id="fb957-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fb957-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fb957-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fb957-112">Delegated (work or school account)</span></span> | <span data-ttu-id="fb957-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fb957-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="fb957-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fb957-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fb957-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fb957-115">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="fb957-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fb957-116">Application</span></span> | <span data-ttu-id="fb957-117">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fb957-117">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="fb957-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fb957-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/{id}/createReplyAll
POST /users/{id | userPrincipalName}/messages/{id}/createReplyAll
POST /me/mailFolders/{id}/messages/{id}/createReplyAll
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/createReplyAll
```
## <a name="request-headers"></a><span data-ttu-id="fb957-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fb957-119">Request headers</span></span>
| <span data-ttu-id="fb957-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="fb957-120">Name</span></span>       | <span data-ttu-id="fb957-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb957-121">Type</span></span> | <span data-ttu-id="fb957-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb957-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="fb957-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="fb957-123">Authorization</span></span>  | <span data-ttu-id="fb957-124">string</span><span class="sxs-lookup"><span data-stu-id="fb957-124">string</span></span>  | <span data-ttu-id="fb957-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fb957-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="fb957-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fb957-127">Request body</span></span>
<span data-ttu-id="fb957-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="fb957-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="fb957-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fb957-129">Response</span></span>

<span data-ttu-id="fb957-130">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [Message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fb957-130">If successful, this method returns `201 Created` response code and [Message](../resources/message.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fb957-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fb957-131">Example</span></span>
<span data-ttu-id="fb957-132">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="fb957-132">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="fb957-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fb957-133">Request</span></span>
<span data-ttu-id="fb957-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fb957-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_createreplyall"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/createReplyAll
```

##### <a name="response"></a><span data-ttu-id="fb957-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fb957-135">Response</span></span>
<span data-ttu-id="fb957-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fb957-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "message: createReplyAll",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
