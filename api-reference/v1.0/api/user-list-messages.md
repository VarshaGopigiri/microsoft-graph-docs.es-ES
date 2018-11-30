---
title: Enumerar mensajes
description: Obtenga los mensajes del buzón del usuario que ha iniciado sesión (incluidas las carpetas Elementos eliminados y Otros correos).
ms.openlocfilehash: 861d56850a8a4a4a167540b221bd94b7b8e62ae0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028736"
---
# <a name="list-messages"></a><span data-ttu-id="6c10d-103">Enumerar mensajes</span><span class="sxs-lookup"><span data-stu-id="6c10d-103">List messages</span></span>

<span data-ttu-id="6c10d-104">Obtenga los mensajes del buzón del usuario que ha iniciado sesión (incluidas las carpetas Elementos eliminados y Otros correos).</span><span class="sxs-lookup"><span data-stu-id="6c10d-104">Get the messages in the signed-in user's mailbox (including the Deleted Items and Clutter folders).</span></span>

<span data-ttu-id="6c10d-105">Actualmente, esta operación devuelve los cuerpos de los mensajes solo en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="6c10d-105">Currently, this operation returns message bodies in only HTML format.</span></span>

<span data-ttu-id="6c10d-106">Hay dos escenarios donde una aplicación puede obtener los mensajes en la carpeta de correo de otro usuario:</span><span class="sxs-lookup"><span data-stu-id="6c10d-106">There are two scenarios where an app can get messages in another user's mail folder:</span></span>

* <span data-ttu-id="6c10d-107">Si la aplicación tiene permisos de aplicación, o bien,</span><span class="sxs-lookup"><span data-stu-id="6c10d-107">If the app has application permissions, or,</span></span>
* <span data-ttu-id="6c10d-108">Si la aplicación tiene la adecuada delega [los permisos](#permissions) de un usuario y otro usuario ha compartido una carpeta de correo con ese usuario o, se le concede acceso delegado a ese usuario.</span><span class="sxs-lookup"><span data-stu-id="6c10d-108">If the app has the appropriate delegated [permissions](#permissions) from one user, and another user has shared a mail folder with that user, or, has given delegated access to that user.</span></span> <span data-ttu-id="6c10d-109">Consulte los [Detalles y un ejemplo](/graph/outlook-share-messages-folders).</span><span class="sxs-lookup"><span data-stu-id="6c10d-109">See [details and an example](/graph/outlook-share-messages-folders).</span></span>

## <a name="permissions"></a><span data-ttu-id="6c10d-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="6c10d-110">Permissions</span></span>
<span data-ttu-id="6c10d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6c10d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6c10d-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6c10d-113">Permission type</span></span>      | <span data-ttu-id="6c10d-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6c10d-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6c10d-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6c10d-115">Delegated (work or school account)</span></span> | <span data-ttu-id="6c10d-116">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c10d-116">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="6c10d-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6c10d-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6c10d-118">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c10d-118">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="6c10d-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6c10d-119">Application</span></span> | <span data-ttu-id="6c10d-120">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c10d-120">Mail.Read, Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="6c10d-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6c10d-121">HTTP request</span></span>

<span data-ttu-id="6c10d-122">Para obtener todos los mensajes del buzón de un usuario:</span><span class="sxs-lookup"><span data-stu-id="6c10d-122">To get all the messages in a user's mailbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/messages
GET /users/{id | userPrincipalName}/messages
```

<span data-ttu-id="6c10d-123">Para obtener los mensajes de una carpeta específica del buzón del usuario:</span><span class="sxs-lookup"><span data-stu-id="6c10d-123">To get messages in a specific folder in the user's mailbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/{id}/messages
GET /users/{id | userPrincipalName}/mailFolders/{id}/messages
```

## <a name="optional-query-parameters"></a><span data-ttu-id="6c10d-124">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="6c10d-124">Optional query parameters</span></span>
<span data-ttu-id="6c10d-125">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6c10d-125">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="6c10d-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6c10d-126">Request headers</span></span>
| <span data-ttu-id="6c10d-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="6c10d-127">Name</span></span>       | <span data-ttu-id="6c10d-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c10d-128">Type</span></span> | <span data-ttu-id="6c10d-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c10d-129">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="6c10d-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="6c10d-130">Authorization</span></span>  | <span data-ttu-id="6c10d-131">string</span><span class="sxs-lookup"><span data-stu-id="6c10d-131">string</span></span>  | <span data-ttu-id="6c10d-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6c10d-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="6c10d-134">Prefer: outlook.body-content-type</span><span class="sxs-lookup"><span data-stu-id="6c10d-134">Prefer: outlook.body-content-type</span></span> | <span data-ttu-id="6c10d-135">string</span><span class="sxs-lookup"><span data-stu-id="6c10d-135">string</span></span> | <span data-ttu-id="6c10d-136">Formato de las propiedades **body** y **uniqueBody** que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="6c10d-136">The format of the **body** and **uniqueBody** properties to be returned in.</span></span> <span data-ttu-id="6c10d-137">Los valores pueden ser "text" o "html".</span><span class="sxs-lookup"><span data-stu-id="6c10d-137">Values can be "text" or "html".</span></span> <span data-ttu-id="6c10d-138">Si no se especifica el encabezado, las propiedades **body** y **uniqueBody** se devuelven en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="6c10d-138">If the header is not specified, the **body** and **uniqueBody** properties are returned in HTML format.</span></span> <span data-ttu-id="6c10d-139">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6c10d-139">Optional.</span></span> |


## <a name="request-body"></a><span data-ttu-id="6c10d-140">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6c10d-140">Request body</span></span>
<span data-ttu-id="6c10d-141">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6c10d-141">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6c10d-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6c10d-142">Response</span></span>

<span data-ttu-id="6c10d-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6c10d-143">If successful, this method returns a `200 OK` response code and collection of [Message](../resources/message.md) objects in the response body.</span></span>

<span data-ttu-id="6c10d-144">El tamaño de página predeterminada para esta solicitud es de 10 mensajes.</span><span class="sxs-lookup"><span data-stu-id="6c10d-144">The default page size for this request is 10 messages.</span></span>

## <a name="example"></a><span data-ttu-id="6c10d-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6c10d-145">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6c10d-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6c10d-146">Request</span></span>
<span data-ttu-id="6c10d-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6c10d-147">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_messages"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages
```
##### <a name="response"></a><span data-ttu-id="6c10d-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6c10d-148">Response</span></span>
<span data-ttu-id="6c10d-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6c10d-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 317

{
  "value": [
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
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List messages",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
