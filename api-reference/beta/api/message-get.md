---
title: Obtener mensaje
description: Recuperar las propiedades y relaciones del objeto de mensaje.
author: angelgolfer-ms
ms.openlocfilehash: 8408e9ef0347721978eb1be00c64ce1f66f882d1
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27352686"
---
# <a name="get-message"></a><span data-ttu-id="27bc4-103">Obtener mensaje</span><span class="sxs-lookup"><span data-stu-id="27bc4-103">Get message</span></span>

> <span data-ttu-id="27bc4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="27bc4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="27bc4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="27bc4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="27bc4-106">Recuperar las propiedades y relaciones del objeto de [mensaje](../resources/message.md) .</span><span class="sxs-lookup"><span data-stu-id="27bc4-106">Retrieve the properties and relationships of the [message](../resources/message.md) object.</span></span>

<span data-ttu-id="27bc4-107">Por ejemplo, puede obtener un mensaje y expanda todas las instancias de [mencionar](../resources/mention.md) en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="27bc4-107">For example, you can get a message and expand all the [mention](../resources/mention.md) instances in the message.</span></span>

<span data-ttu-id="27bc4-108">Hay dos escenarios donde una aplicación puede obtener un mensaje en la carpeta de correo de otro usuario:</span><span class="sxs-lookup"><span data-stu-id="27bc4-108">There are two scenarios where an app can get a message in another user's mail folder:</span></span>

* <span data-ttu-id="27bc4-109">Si la aplicación tiene permisos de aplicación, o bien,</span><span class="sxs-lookup"><span data-stu-id="27bc4-109">If the app has application permissions, or,</span></span>
* <span data-ttu-id="27bc4-110">Si la aplicación tiene la adecuada delega [los permisos](#permissions) de un usuario y otro usuario ha compartido una carpeta de correo con ese usuario o, se le concede acceso delegado a ese usuario.</span><span class="sxs-lookup"><span data-stu-id="27bc4-110">If the app has the appropriate delegated [permissions](#permissions) from one user, and another user has shared a mail folder with that user, or, has given delegated access to that user.</span></span> <span data-ttu-id="27bc4-111">Consulte los [Detalles y un ejemplo](/graph/outlook-share-messages-folders).</span><span class="sxs-lookup"><span data-stu-id="27bc4-111">See [details and an example](/graph/outlook-share-messages-folders).</span></span>

<span data-ttu-id="27bc4-112">Dado que el recurso **message** admite [extensiones](/graph/extensibility-overview), también puede utilizar la operación `GET` para obtener propiedades personalizadas y datos de extensión en una instancia **message**.</span><span class="sxs-lookup"><span data-stu-id="27bc4-112">Since the **message** resource supports [extensions](/graph/extensibility-overview), you can also use the `GET` operation to get custom properties and extension data in a **message** instance.</span></span>


## <a name="permissions"></a><span data-ttu-id="27bc4-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="27bc4-113">Permissions</span></span>
<span data-ttu-id="27bc4-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="27bc4-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="27bc4-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="27bc4-116">Permission type</span></span>      | <span data-ttu-id="27bc4-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="27bc4-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="27bc4-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="27bc4-118">Delegated (work or school account)</span></span> | <span data-ttu-id="27bc4-119">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="27bc4-119">Mail.Read</span></span>    |
|<span data-ttu-id="27bc4-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="27bc4-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="27bc4-121">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="27bc4-121">Mail.Read</span></span>    |
|<span data-ttu-id="27bc4-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="27bc4-122">Application</span></span> | <span data-ttu-id="27bc4-123">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="27bc4-123">Mail.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="27bc4-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="27bc4-124">HTTP request</span></span>

<span data-ttu-id="27bc4-125">Para obtener el mensaje especificado:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="27bc4-125">To get the specified message: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/messages/{id}
GET /users/{id | userPrincipalName}/messages/{id}
GET /me/mailFolders/{id}/messages/{id}
GET /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```

<span data-ttu-id="27bc4-126">Para obtener un mensaje y expanda todas las menciones en el mensaje:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="27bc4-126">To get a message and expand all mentions in the message: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/messages/{id}?$expand=mentions
GET /users/{id | userPrincipalName}/messages/{id}?$expand=mentions
GET /me/mailFolders/{id}/messages/{id}?$expand=mentions
GET /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}?$expand=mentions
```

## <a name="optional-query-parameters"></a><span data-ttu-id="27bc4-127">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="27bc4-127">Optional query parameters</span></span>
<span data-ttu-id="27bc4-128">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="27bc4-128">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="27bc4-129">Puede usar el `$expand` expandida del parámetro de consulta en la propiedad de navegación **menciones** para obtener un mensaje con los detalles de cada [mencionar](../resources/mention.md) en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="27bc4-129">You can use the `$expand` query parameter on the **mentions** navigation property to get a message with the details of each [mention](../resources/mention.md) in the message expanded.</span></span>



## <a name="request-headers"></a><span data-ttu-id="27bc4-130">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="27bc4-130">Request headers</span></span>
| <span data-ttu-id="27bc4-131">Nombre</span><span class="sxs-lookup"><span data-stu-id="27bc4-131">Name</span></span>       | <span data-ttu-id="27bc4-132">Type</span><span class="sxs-lookup"><span data-stu-id="27bc4-132">Type</span></span> | <span data-ttu-id="27bc4-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="27bc4-133">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="27bc4-134">Autorización</span><span class="sxs-lookup"><span data-stu-id="27bc4-134">Authorization</span></span>  | <span data-ttu-id="27bc4-135">string</span><span class="sxs-lookup"><span data-stu-id="27bc4-135">string</span></span>  | <span data-ttu-id="27bc4-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="27bc4-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="27bc4-138">Prefer: outlook.body-content-type</span><span class="sxs-lookup"><span data-stu-id="27bc4-138">Prefer: outlook.body-content-type</span></span> | <span data-ttu-id="27bc4-139">string</span><span class="sxs-lookup"><span data-stu-id="27bc4-139">string</span></span> | <span data-ttu-id="27bc4-140">Formato de las propiedades **body** y **uniqueBody** que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="27bc4-140">The format of the **body** and **uniqueBody** properties to be returned in.</span></span> <span data-ttu-id="27bc4-141">Los valores pueden ser "text" o "html".</span><span class="sxs-lookup"><span data-stu-id="27bc4-141">Values can be "text" or "html".</span></span> <span data-ttu-id="27bc4-142">Se devuelve un encabezado `Preference-Applied` como confirmación si se especifica este encabezado `Prefer`.</span><span class="sxs-lookup"><span data-stu-id="27bc4-142">A `Preference-Applied` header is returned as confirmation if this `Prefer` header is specified.</span></span> <span data-ttu-id="27bc4-143">Si no se especifica el encabezado, las propiedades **body** y **uniqueBody** se devuelven en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="27bc4-143">If the header is not specified, the **body** and **uniqueBody** properties are returned in HTML format.</span></span> <span data-ttu-id="27bc4-144">Opcional.</span><span class="sxs-lookup"><span data-stu-id="27bc4-144">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="27bc4-145">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="27bc4-145">Request body</span></span>
<span data-ttu-id="27bc4-146">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="27bc4-146">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="27bc4-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="27bc4-147">Response</span></span>

<span data-ttu-id="27bc4-148">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="27bc4-148">If successful, this method returns a `200 OK` response code and [message](../resources/message.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="27bc4-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="27bc4-149">Example</span></span>
##### <a name="request-1"></a><span data-ttu-id="27bc4-150">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="27bc4-150">Request 1</span></span>
<span data-ttu-id="27bc4-151">El primer ejemplo obtiene el mensaje especificado.</span><span class="sxs-lookup"><span data-stu-id="27bc4-151">The first example gets the specified message.</span></span> <span data-ttu-id="27bc4-152">No especifica ningún encabezado para indicar el formato deseado del cuerpo de la que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="27bc4-152">It does not specify any header to indicate the desired format of the body to be returned.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["AAMkAGI1AAAoZCfHAAA="],
  "name": "get_message"
}-->
```http
GET https://graph.microsoft.com/beta/me/messages('AAMkAGI1AAAoZCfHAAA=')
```
##### <a name="response-1"></a><span data-ttu-id="27bc4-153">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="27bc4-153">Response 1</span></span>
<span data-ttu-id="27bc4-154">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="27bc4-154">Here is an example of the response.</span></span> <span data-ttu-id="27bc4-155">Se devuelven las propiedades **body** y **uniqueBody** en el formato HTML predeterminado.</span><span class="sxs-lookup"><span data-stu-id="27bc4-155">The **body** and **uniqueBody** properties are returned in the default HTML format.</span></span>
<span data-ttu-id="27bc4-156">Nota: El objeto de respuesta que se muestra aquí se trunca por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="27bc4-156">Note: The response object shown here is truncated for brevity.</span></span> <span data-ttu-id="27bc4-157">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="27bc4-157">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 523

{
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#users('cd209b0b-3f83-4c35-82d2-d88a61820480')/messages/$entity",
    "@odata.etag":"W/\"CQAAABYAAABmWdbhEgBXTophjCWt81m9AAAoZYj4\"",
    "id":"AAMkAGI1AAAoZCfHAAA=",
    "subject":"Welcome to our group!",
    "bodyPreview":"Welcome to our group, Dana! Hope you will enjoy working with us !\r\n",
    "body":{
        "contentType":"html",
        "content":"<html>\r\n<head></head><body><p>Welcome to our group, Dana! Hope you will enjoy working with us </p></body></html>\r\n"
    },
    "uniqueBody":{
        "contentType":"html",
        "content":"<html>\r\n<head></head><body><p>Welcome to our group, Dana! Hope you will enjoy working with us </p></body></html>\r\n"
    }
}
```

##### <a name="request-2"></a><span data-ttu-id="27bc4-158">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="27bc4-158">Request 2</span></span>
<span data-ttu-id="27bc4-159">En el ejemplo siguiente, el usuario ha iniciado sesión es Dana Swope.</span><span class="sxs-lookup"><span data-stu-id="27bc4-159">In the next example, the signed-in user is Dana Swope.</span></span> <span data-ttu-id="27bc4-160">El ejemplo muestra la obtención de los detalles de todas las menciones que en el mensaje especificado en el buzón de Dana.</span><span class="sxs-lookup"><span data-stu-id="27bc4-160">The example shows getting the details of all the mentions in the specified message in Dana's mailbox.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["AQMkADJmMTUAAAgVZAAAA"],
  "name": "get_mentions_in_message"
}-->
```http
GET https://graph.microsoft.com/beta/me/messages/('AQMkADJmMTUAAAgVZAAAA')?$expand=mentions
```
##### <a name="response-2"></a><span data-ttu-id="27bc4-161">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="27bc4-161">Response 2</span></span>
<span data-ttu-id="27bc4-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="27bc4-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 2248

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#me/messages/$entity",
  "@odata.id":"https://graph.microsoft.com/beta/users('266efe5a-0fd7-4edd-877b-b2d1e561f193@ae01a323-3934-4475-a32d-af1274312bb0')/messages('AQMkADJmMTUAAAgVZAAAA')",
  "@odata.etag":"W/\"CQAAABYAAAAPFhK2FclcRbABBJhCde8iAAAAAATI\"",
  "id":"AQMkADJmMTUAAAgVZAAAA",
  "subject":"Start planning soon",
  "body":{
    "contentType":"HTML",
    "content":"<html><head></head><body><p><a href=\"mailto:danas@contoso.onmicrosoft.com\">@Dana Swope</a>,<a href=\"mailto:randiw@contoso.onmicrosoft.com\">@Randi Welch</a>, forgot to mention, I will be away&nbsp;this weekend. I can start on Monday though.</p></body></html>"
  },
  "bodyPreview":"@Dana Swope<mailto:danas@contoso.onmicrosoft.com>, @Randi Welch, forgot to mention, I will be away this weekend. I can start on Monday though.",
  "sender":{
    "emailAddress":{
      "name":"Samantha Booth",
      "address":"samanthab@contoso.onmicrosoft.com"
    }
  },
  "from":{
    "emailAddress":{
      "name":"Samantha Booth",
      "address":"samanthab@contoso.onmicrosoft.com"
    }
  },
  "toRecipients":[
    {
      "emailAddress":{
        "name":"Dana Swope",
        "address":"danas@contoso.onmicrosoft.com"
      }
    },
    {
      "emailAddress":{
        "name":"Randi Welch",
        "address":"randiw@contoso.onmicrosoft.com"
      }
    }
  ],
  "ccRecipients":[
  ],
  "bccRecipients":[
  ],
  "mentionsPreview":{
    "isMentioned":true
  },
  "mentions@odata.context":"https://graph.microsoft.com/beta/$metadata#me/messages('AQMkADJmMTUAAAgVZAAAA')/mentions",
  "mentions":[
    {
      "@odata.id":"https://graph.microsoft.com/beta/users('266efe5a-0fd7-4edd-877b-b2d1e561f193@ae01a323-3934-4475-a32d-af1274312bb0')/messages('AQMkADJmMTUAAAgVZAAAA')/mentions('138f4c0a-1130-4776-b780-bf79d73abb3f')",
      "id":"138f4c0a-1130-4776-b780-bf79d73abb3f",
      "mentioned":{
        "name":"Dana Swope",
        "address":"danas@contoso.onmicrosoft.com"
      },
      "mentionText":null,
      "clientReference":null,
      "createdBy":{
        "name":"Samantha Booth",
        "address":"samanthab@contoso.onmicrosoft.com"
      },
      "createdDateTime":"2016-07-21T07:40:20.152Z",
      "serverCreatedDateTime":"2016-07-21T07:40:20.152Z",
      "deepLink":null,
      "application":null
    },
    {
      "@odata.id":"https://graph.microsoft.com/beta/users('266efe5a-0fd7-4edd-877b-b2d1e561f193@ae01a323-3934-4475-a32d-af1274312bb0')/messages('AQMkADJmMTUAAAgVZAAAA')/mentions('7b94df1a-0086-482a-b0da-e62fae12f983')",
      "id":"7b94df1a-0086-482a-b0da-e62fae12f983",
      "mentioned":{
        "name":"Randi Welch",
        "address":"randiw@contoso.onmicrosoft.com"
      },
      "mentionText":null,
      "clientReference":null,
      "createdBy":{
        "name":"Samantha Booth",
        "address":"samanthab@contoso.onmicrosoft.com"
      },
      "createdDateTime":"2016-07-21T07:40:20.158Z",
      "serverCreatedDateTime":"2016-07-21T07:40:20.158Z",
      "deepLink":null,
      "application":null
    }
  ]
}
```


##### <a name="request-3"></a><span data-ttu-id="27bc4-165">Solicitud 3</span><span class="sxs-lookup"><span data-stu-id="27bc4-165">Request 3</span></span>

<span data-ttu-id="27bc4-166">El tercer ejemplo muestra cómo usar un `Prefer: outlook.body-content-type="text"` encabezado para obtener el **cuerpo** y el **uniqueBody** del mensaje especificado en formato de texto.</span><span class="sxs-lookup"><span data-stu-id="27bc4-166">The third example shows how to use a `Prefer: outlook.body-content-type="text"` header to get the **body** and **uniqueBody** of the specified message in text format.</span></span>

<!-- {
  "blockType": "request",
  "sampleKeys": ["AAMkAGI1AAAoZCfHAAA="],
  "name": "get_message_in_text"
}-->

```http
GET https://graph.microsoft.com/beta/me/messages('AAMkAGI1AAAoZCfHAAA=')?$select=subject,body,bodyPreview,uniqueBody
Prefer: outlook.body-content-type="text"
```

##### <a name="response-3"></a><span data-ttu-id="27bc4-167">Respuesta 3</span><span class="sxs-lookup"><span data-stu-id="27bc4-167">Response 3</span></span>

<span data-ttu-id="27bc4-168">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="27bc4-168">Here is an example of the response.</span></span> <span data-ttu-id="27bc4-169">Nota: La respuesta incluye una `Preference-Applied: outlook.body-content-type` encabezado agradecer a los `Prefer: outlook.body-content-type` encabezado de solicitud.</span><span class="sxs-lookup"><span data-stu-id="27bc4-169">Note: The response includes a `Preference-Applied: outlook.body-content-type` header to acknowledge the `Prefer: outlook.body-content-type` request header.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Preference-Applied: outlook.body-content-type="text"
Content-length: 1550

{
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#users('cd209b0b-3f83-4c35-82d2-d88a61820480')/messages(subject,body,bodyPreview,uniqueBody)/$entity",
    "@odata.etag":"W/\"CQAAABYAAABmWdbhEgBXTophjCWt81m9AAAoZYj4\"",
    "id":"AAMkAGI1AAAoZCfHAAA=",
    "subject":"Welcome to our group!",
    "bodyPreview":"Welcome to our group, Dana! Hope you will enjoy working with us !\r\n\r\nWould you like to choose a day for our orientation from the available times below:\r\n\r\n\r\nDate\r\n        Time\r\n\r\nApril 14, 2017\r\n        1-3pm\r\n\r\nApril 21, 2017\r\n        10-12noon\r\n\r\n\r\n\r\nTh",
    "body":{
        "contentType":"text",
        "content":"Welcome to our group, Dana! Hope you will enjoy working with us [\ud83d\ude0a] [\ud83d\ude0a] [\ud83d\ude0a] [\ud83d\ude0a] [\ud83d\ude0a] !\r\n\r\nWould you like to choose a day for our orientation from the available times below:\r\n\r\n\r\nDate\r\n        Time\r\n\r\nApril 14, 2017\r\n        1-3pm\r\n\r\nApril 21, 2017\r\n        10-12noon\r\n\r\n\r\n\r\nThanks!\r\n\r\n"
    },
    "uniqueBody":{
        "contentType":"text",
        "content":"Welcome to our group, Dana! Hope you will enjoy working with us [\ud83d\ude0a] [\ud83d\ude0a] [\ud83d\ude0a] [\ud83d\ude0a] [\ud83d\ude0a] !\r\nWould you like to choose a day for our orientation from the available times below:\r\n\r\nDate\r\n        Time\r\n\r\nApril 14, 2017\r\n        1-3pm\r\n\r\nApril 21, 2017\r\n        10-12noon\r\n\r\n\r\nThanks!\r\n"
    }
}
```

##### <a name="request-4"></a><span data-ttu-id="27bc4-170">Solicitud 4</span><span class="sxs-lookup"><span data-stu-id="27bc4-170">Request 4</span></span>

<span data-ttu-id="27bc4-171">El cuarto ejemplo muestra cómo obtener los encabezados de mensaje de Internet de un mensaje específico.</span><span class="sxs-lookup"><span data-stu-id="27bc4-171">The fourth example shows how to get the Internet message headers of a specific message.</span></span>  

<!-- {
  "blockType": "request",
  "sampleKeys": ["AAMkAGVmMDEz"],
  "name": "get_message_internet_headers"
}-->

```http
GET https://graph.microsoft.com/beta/me/messages('AAMkAGVmMDEz')?$select=internetMessageHeaders
```

##### <a name="response-4"></a><span data-ttu-id="27bc4-172">Respuesta 4</span><span class="sxs-lookup"><span data-stu-id="27bc4-172">Response 4</span></span>

<span data-ttu-id="27bc4-173">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="27bc4-173">Here is an example of the response.</span></span> <span data-ttu-id="27bc4-174">Nota: El número de encabezados de mensaje de Internet en el objeto de respuesta se ha reducido por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="27bc4-174">Note: The number of Internet message headers in the response object has been reduced for brevity.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#users('48d31887-5fad-4d73-a9f5-3c356e68a038')/messages(internetMessageHeaders)/$entity",
  "@odata.type":"#microsoft.graph.eventMessageRequest",
  "@odata.etag":"W/\"CwAAABYAAAAiIsqMbYjsT5e/T7KzowPTAAAa/qUB\"",
  "id":"AAMkAGVmMDEz",
  "internetMessageHeaders":[
    {
      "name":"Content-Type",
      "value":"application/ms-tnef"
    },
    {
      "name":"Content-Transfer-Encoding",
      "value":"binary"
    },
    {
      "name":"Subject",
      "value":"Cloud and Mobile Working Group"
    },
    {
      "name":"x-custom-header-group-name",
      "value":"Washington"
    },
    {
      "name":"x-custom-header-group-id",
      "value":"WA001"
    }
  ]
}
```

## <a name="see-also"></a><span data-ttu-id="27bc4-175">Vea también</span><span class="sxs-lookup"><span data-stu-id="27bc4-175">See also</span></span>

- [<span data-ttu-id="27bc4-176">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="27bc4-176">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="27bc4-177">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="27bc4-177">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
- [<span data-ttu-id="27bc4-178">Agregar datos personalizados a grupos mediante extensiones de esquema (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="27bc4-178">Add custom data to groups using schema extensions (preview)</span></span>](/graph/extensibility-schema-groups)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get message",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
