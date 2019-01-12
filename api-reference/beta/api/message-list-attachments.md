---
title: List attachments
description: Recupera una lista de objetos attachment asociados a un mensaje.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 584b01114f22466673568d991c824a94c6d73dd2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27983488"
---
# <a name="list-attachments"></a><span data-ttu-id="4dd7f-103">List attachments</span><span class="sxs-lookup"><span data-stu-id="4dd7f-103">List attachments</span></span>

> <span data-ttu-id="4dd7f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4dd7f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4dd7f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4dd7f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4dd7f-106">Recupera una lista de objetos [attachment](../resources/attachment.md) asociados a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="4dd7f-106">Retrieve a list of [attachment](../resources/attachment.md) objects attached to a message.</span></span>
## <a name="permissions"></a><span data-ttu-id="4dd7f-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="4dd7f-107">Permissions</span></span>
<span data-ttu-id="4dd7f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4dd7f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4dd7f-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4dd7f-110">Permission type</span></span>      | <span data-ttu-id="4dd7f-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4dd7f-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4dd7f-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4dd7f-112">Delegated (work or school account)</span></span> | <span data-ttu-id="4dd7f-113">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="4dd7f-113">Mail.Read</span></span>    |
|<span data-ttu-id="4dd7f-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4dd7f-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4dd7f-115">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="4dd7f-115">Mail.Read</span></span>    |
|<span data-ttu-id="4dd7f-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4dd7f-116">Application</span></span> | <span data-ttu-id="4dd7f-117">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="4dd7f-117">Mail.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="4dd7f-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4dd7f-118">HTTP request</span></span>
<span data-ttu-id="4dd7f-119"><!-- { "blockType": "ignored" } -->Datos adjuntos de un [mensaje](../resources/message.md) en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="4dd7f-119"><!-- { "blockType": "ignored" } --> Attachments for a [message](../resources/message.md) in a user's mailbox.</span></span>
```http
GET /me/messages/{id}/attachments
GET /users/{id | userPrincipalName}/messages/{id}/attachments
```
<span data-ttu-id="4dd7f-120">Datos adjuntos de un [message](../resources/message.md) contenido en una [mailFolder](../resources/mailfolder.md) de nivel superior en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="4dd7f-120">Attachments for a [message](../resources/message.md) contained in a top level [mailFolder](../resources/mailfolder.md) in a user's mailbox.</span></span>
```http
GET /me/mailFolders/{id}/messages/{id}/attachments
GET /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/attachments
```
<span data-ttu-id="4dd7f-p103">Datos adjuntos de un [message](../resources/message.md) contenido en una carpeta secundaria de una [mailFolder](../resources/mailfolder.md) en el buzón de un usuario.  El ejemplo siguiente muestra un nivel de anidamiento, pero un mensaje puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="4dd7f-p103">Attachments for a [message](../resources/message.md) contained in a child folder of a [mailFolder](../resources/mailfolder.md) in a user's mailbox.  The example below shows one level of nesting, but a message can be located in a child of a child and so on.</span></span>
```http
GET /me/mailFolders/{id}/childFolders/{id}/.../messages/{id}/attachments/{id}
GET /users/{id | userPrincipalName}/mailFolders/{id}/childFolders/{id}/messages/{id}/attachments/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="4dd7f-123">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="4dd7f-123">Optional query parameters</span></span>
<span data-ttu-id="4dd7f-124">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4dd7f-124">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="4dd7f-125">En concreto, puede usar el $expanda parámetro de consulta para incluir todos los datos adjuntos de mensaje en línea con el resto de las propiedades del mensaje.</span><span class="sxs-lookup"><span data-stu-id="4dd7f-125">In particular, you can use the $expand query parameter to include all of the message attachments inline with the rest of the message properties.</span></span> <span data-ttu-id="4dd7f-126">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="4dd7f-126">For example:</span></span>

```
GET https://graph.microsoft.com/beta/me/messages/{id}?$expand=attachments
```
## <a name="request-headers"></a><span data-ttu-id="4dd7f-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4dd7f-127">Request headers</span></span>
| <span data-ttu-id="4dd7f-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="4dd7f-128">Name</span></span>       | <span data-ttu-id="4dd7f-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="4dd7f-129">Type</span></span> | <span data-ttu-id="4dd7f-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="4dd7f-130">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="4dd7f-131">Autorización</span><span class="sxs-lookup"><span data-stu-id="4dd7f-131">Authorization</span></span>  | <span data-ttu-id="4dd7f-132">string</span><span class="sxs-lookup"><span data-stu-id="4dd7f-132">string</span></span>  | <span data-ttu-id="4dd7f-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4dd7f-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4dd7f-135">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4dd7f-135">Request body</span></span>
<span data-ttu-id="4dd7f-136">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4dd7f-136">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4dd7f-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4dd7f-137">Response</span></span>

<span data-ttu-id="4dd7f-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4dd7f-138">If successful, this method returns a `200 OK` response code and collection of [Attachment](../resources/attachment.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="4dd7f-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4dd7f-139">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4dd7f-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4dd7f-140">Request</span></span>
<span data-ttu-id="4dd7f-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4dd7f-141">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_attachments"
}-->
```http
GET https://graph.microsoft.com/beta/me/messages/{id}/attachments
```
##### <a name="response"></a><span data-ttu-id="4dd7f-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4dd7f-142">Response</span></span>
<span data-ttu-id="4dd7f-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4dd7f-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.attachment",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 215

{
  "value": [
    {
      "@odata.type": "#Microsoft.OutlookServices.FileAttachment",
      "contentType": "contentType-value",
      "contentLocation": "contentLocation-value",
      "contentBytes": "contentBytes-value",
      "contentId": "null",
      "lastModifiedDateTime": "2016-10-19T10:37:00Z",
      "id": "id-value",
      "isInline": false,
      "isContactPhoto": false,
      "name": "name-value",
      "size": 99
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List attachments",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
