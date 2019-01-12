---
title: 'message: createForward'
description: Cree un borrador para reenviar el mensaje especificado. Después, puede actualizar el borrador para agregar contenido al **cuerpo**, cambiar otras propiedades del mensaje o, simplemente, enviar el borrador.
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 484eb33c3cfe7dc9c1dc3ec896e45cff9ecce61d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27921146"
---
# <a name="message-createforward"></a><span data-ttu-id="0e50e-104">message: createForward</span><span class="sxs-lookup"><span data-stu-id="0e50e-104">message: createForward</span></span>

<span data-ttu-id="0e50e-105">Cree un borrador para reenviar el [mensaje](../resources/message.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="0e50e-105">Create a draft to forward the specified [message](../resources/message.md).</span></span> <span data-ttu-id="0e50e-106">Después, puede [actualizar](../api/message-update.md) el borrador para agregar contenido al **cuerpo**, cambiar otras propiedades del mensaje o, simplemente, [enviar](../api/message-send.md) el borrador.</span><span class="sxs-lookup"><span data-stu-id="0e50e-106">You can then [update](../api/message-update.md) the draft to add content to the **body** or change other message properties, or, simply [send](../api/message-send.md) the draft.</span></span>

## <a name="permissions"></a><span data-ttu-id="0e50e-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="0e50e-107">Permissions</span></span>

<span data-ttu-id="0e50e-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0e50e-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0e50e-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0e50e-110">Permission type</span></span>      | <span data-ttu-id="0e50e-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0e50e-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0e50e-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0e50e-112">Delegated (work or school account)</span></span> | <span data-ttu-id="0e50e-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0e50e-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="0e50e-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0e50e-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0e50e-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0e50e-115">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="0e50e-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0e50e-116">Application</span></span> | <span data-ttu-id="0e50e-117">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0e50e-117">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="0e50e-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0e50e-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/messages/{id}/createForward
POST /users/{id | userPrincipalName}/messages/{id}/createForward
POST /me/mailFolders/{id}/messages/{id}/createForward
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/createForward
```

## <a name="request-headers"></a><span data-ttu-id="0e50e-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0e50e-119">Request headers</span></span>

| <span data-ttu-id="0e50e-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="0e50e-120">Name</span></span>       | <span data-ttu-id="0e50e-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="0e50e-121">Type</span></span> | <span data-ttu-id="0e50e-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e50e-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="0e50e-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="0e50e-123">Authorization</span></span>  | <span data-ttu-id="0e50e-124">string</span><span class="sxs-lookup"><span data-stu-id="0e50e-124">string</span></span>  | <span data-ttu-id="0e50e-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0e50e-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="0e50e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0e50e-127">Request body</span></span>

<span data-ttu-id="0e50e-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0e50e-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0e50e-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e50e-129">Response</span></span>

<span data-ttu-id="0e50e-130">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [Message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0e50e-130">If successful, this method returns `201 Created` response code and [Message](../resources/message.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0e50e-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0e50e-131">Example</span></span>

<span data-ttu-id="0e50e-132">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="0e50e-132">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="0e50e-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0e50e-133">Request</span></span>

<span data-ttu-id="0e50e-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0e50e-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_createforward"
}-->

```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/createForward
```

##### <a name="response"></a><span data-ttu-id="0e50e-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e50e-135">Response</span></span>

<span data-ttu-id="0e50e-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0e50e-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->

```http
HTTP/1.1 201 Created
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
  "description": "message: createForward",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
