---
title: List attachments
description: Recupera una lista de objetos attachment asociados a un mensaje.
author: angelgolfer-ms
localization_priority: Priority
ms.prod: outlook
ms.openlocfilehash: 2e37e863d4b050a07b756b91f1e98a4349239154
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27918125"
---
# <a name="list-attachments"></a><span data-ttu-id="82383-103">List attachments</span><span class="sxs-lookup"><span data-stu-id="82383-103">List attachments</span></span>

<span data-ttu-id="82383-104">Recupera una lista de objetos [attachment](../resources/attachment.md) asociados a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="82383-104">Retrieve a list of [attachment](../resources/attachment.md) objects attached to a message.</span></span>
## <a name="permissions"></a><span data-ttu-id="82383-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="82383-105">Permissions</span></span>
<span data-ttu-id="82383-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="82383-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="82383-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="82383-108">Permission type</span></span>      | <span data-ttu-id="82383-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="82383-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="82383-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="82383-110">Delegated (work or school account)</span></span> | <span data-ttu-id="82383-111">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="82383-111">Mail.Read</span></span>    |
|<span data-ttu-id="82383-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="82383-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="82383-113">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="82383-113">Mail.Read</span></span>    |
|<span data-ttu-id="82383-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="82383-114">Application</span></span> | <span data-ttu-id="82383-115">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="82383-115">Mail.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="82383-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="82383-116">HTTP request</span></span>
<span data-ttu-id="82383-117"><!-- { "blockType": "ignored" } -->Datos adjuntos de un [mensaje](../resources/message.md) en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="82383-117"><!-- { "blockType": "ignored" } --> Attachments for a [message](../resources/message.md) in a user's mailbox.</span></span>
```http
GET /me/messages/{id}/attachments
GET /users/{id | userPrincipalName}/messages/{id}/attachments
```
<span data-ttu-id="82383-118">Datos adjuntos de un [message](../resources/message.md) contenido en una [mailFolder](../resources/mailfolder.md) de nivel superior en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="82383-118">Attachments for a [message](../resources/message.md) contained in a top level [mailFolder](../resources/mailfolder.md) in a user's mailbox.</span></span>
```http
GET /me/mailFolders/{id}/messages/{id}/attachments
GET /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/attachments
```
<span data-ttu-id="82383-p102">Datos adjuntos de un [message](../resources/message.md) contenido en una carpeta secundaria de una [mailFolder](../resources/mailfolder.md) en el buzón de un usuario.  El ejemplo siguiente muestra un nivel de anidamiento, pero un mensaje puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="82383-p102">Attachments for a [message](../resources/message.md) contained in a child folder of a [mailFolder](../resources/mailfolder.md) in a user's mailbox.  The example below shows one level of nesting, but a message can be located in a child of a child and so on.</span></span>
```http
GET /me/mailFolders/{id}/childFolders/{id}/.../messages/{id}/attachments/{id}
GET /users/{id | userPrincipalName}/mailFolders/{id}/childFolders/{id}/messages/{id}/attachments/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="82383-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="82383-121">Optional query parameters</span></span>
<span data-ttu-id="82383-122">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="82383-122">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="82383-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="82383-123">Request headers</span></span>
| <span data-ttu-id="82383-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="82383-124">Name</span></span>       | <span data-ttu-id="82383-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="82383-125">Type</span></span> | <span data-ttu-id="82383-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="82383-126">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="82383-127">Autorización</span><span class="sxs-lookup"><span data-stu-id="82383-127">Authorization</span></span>  | <span data-ttu-id="82383-128">string</span><span class="sxs-lookup"><span data-stu-id="82383-128">string</span></span>  | <span data-ttu-id="82383-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="82383-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="82383-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="82383-131">Request body</span></span>
<span data-ttu-id="82383-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="82383-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="82383-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="82383-133">Response</span></span>

<span data-ttu-id="82383-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="82383-134">If successful, this method returns a `200 OK` response code and collection of [Attachment](../resources/attachment.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="82383-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="82383-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="82383-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="82383-136">Request</span></span>
<span data-ttu-id="82383-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="82383-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_attachments"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages/{id}/attachments
```
##### <a name="response"></a><span data-ttu-id="82383-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="82383-138">Response</span></span>
<span data-ttu-id="82383-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="82383-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "collection(microsoft.graph.attachment)",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 215

{
  "value": [
    {
      "@odata.type": "microsoft.graph.fileAttachment",
      "contentType": "contentType-value",
      "contentLocation": "contentLocation-value",
      "contentBytes": "base64-contentBytes-value",
      "contentId": "null",
      "lastModifiedDateTime": "datetime-value",
      "id": "id-value",
      "isInline": false,
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
