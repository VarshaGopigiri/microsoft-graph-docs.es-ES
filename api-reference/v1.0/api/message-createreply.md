---
title: 'message: createReply'
description: Cree un borrador de la respuesta al mensaje especificado. Después, puede actualizar el borrador para agregar el contenido de la respuesta al **cuerpo**, cambiar otras propiedades del mensaje o, simplemente, enviar el borrador.
ms.openlocfilehash: 0b98b7f5baea1067097d09b27c13872ef6fc139f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032653"
---
# <a name="message-createreply"></a><span data-ttu-id="00fbd-104">message: createReply</span><span class="sxs-lookup"><span data-stu-id="00fbd-104">message: createReply</span></span>

<span data-ttu-id="00fbd-105">Cree un borrador de la respuesta al [mensaje](../resources/message.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="00fbd-105">Create a draft of the reply to the specified [message](../resources/message.md).</span></span> <span data-ttu-id="00fbd-106">Después, puede [actualizar](../api/message-update.md) el borrador para agregar el contenido de la respuesta al **cuerpo**, cambiar otras propiedades del mensaje o, simplemente, [enviar](../api/message-send.md) el borrador.</span><span class="sxs-lookup"><span data-stu-id="00fbd-106">You can then [update](../api/message-update.md) the draft to add reply content to the **body** or change other message properties, or, simply [send](../api/message-send.md) the draft.</span></span>

## <a name="permissions"></a><span data-ttu-id="00fbd-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="00fbd-107">Permissions</span></span>
<span data-ttu-id="00fbd-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="00fbd-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="00fbd-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="00fbd-110">Permission type</span></span>      | <span data-ttu-id="00fbd-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="00fbd-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="00fbd-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="00fbd-112">Delegated (work or school account)</span></span> | <span data-ttu-id="00fbd-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="00fbd-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="00fbd-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="00fbd-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="00fbd-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="00fbd-115">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="00fbd-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="00fbd-116">Application</span></span> | <span data-ttu-id="00fbd-117">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="00fbd-117">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="00fbd-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="00fbd-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/{id}/createReply
POST /users/{id | userPrincipalName}/messages/{id}/createReply
POST /me/mailFolders/{id}/messages/{id}/createReply
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/createReply
```
## <a name="request-headers"></a><span data-ttu-id="00fbd-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="00fbd-119">Request headers</span></span>
| <span data-ttu-id="00fbd-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="00fbd-120">Name</span></span>       | <span data-ttu-id="00fbd-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="00fbd-121">Type</span></span> | <span data-ttu-id="00fbd-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="00fbd-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="00fbd-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="00fbd-123">Authorization</span></span>  | <span data-ttu-id="00fbd-124">string</span><span class="sxs-lookup"><span data-stu-id="00fbd-124">string</span></span>  | <span data-ttu-id="00fbd-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="00fbd-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="00fbd-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="00fbd-127">Request body</span></span>
<span data-ttu-id="00fbd-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="00fbd-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="00fbd-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="00fbd-129">Response</span></span>

<span data-ttu-id="00fbd-130">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [Message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="00fbd-130">If successful, this method returns `201 Created` response code and [Message](../resources/message.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="00fbd-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="00fbd-131">Example</span></span>
<span data-ttu-id="00fbd-132">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="00fbd-132">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="00fbd-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="00fbd-133">Request</span></span>
<span data-ttu-id="00fbd-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="00fbd-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_createreply"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/createReply
```

##### <a name="response"></a><span data-ttu-id="00fbd-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="00fbd-135">Response</span></span>
<span data-ttu-id="00fbd-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="00fbd-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "message: createReply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
