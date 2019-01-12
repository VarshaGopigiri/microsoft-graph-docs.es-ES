---
title: 'contacto: delta'
description: Obtiene un conjunto de contactos que se hayan agregado, eliminado o actualizado en una carpeta determinada.
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 500895404d92c1eb74b06bc80dd380b9f7c224e2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27916225"
---
# <a name="contact-delta"></a><span data-ttu-id="90a06-103">contacto: delta</span><span class="sxs-lookup"><span data-stu-id="90a06-103">contact: delta</span></span>

> <span data-ttu-id="90a06-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="90a06-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="90a06-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="90a06-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="90a06-106">Obtiene un conjunto de contactos que se hayan agregado, eliminado o actualizado en una carpeta determinada.</span><span class="sxs-lookup"><span data-stu-id="90a06-106">Get a set of contacts that have been added, deleted, or updated in a specified folder.</span></span>

<span data-ttu-id="90a06-p102">La llamada de una función **delta** para los contactos de una carpeta funciona de forma similar a una solicitud GET, salvo que, al aplicar correctamente [tokens de estado](/graph/delta-query-overview) en al menos una de estas llamadas, puede realizar una consulta para obtener los cambios incrementales en los contactos de la carpeta. Esto permite mantener y sincronizar un almacén local de contactos de un usuario, sin tener que capturar cada vez todo el conjunto de contactos desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="90a06-p102">A **delta** function call for contacts in a folder is similar to a GET request, except that by appropriately applying [state tokens](/graph/delta-query-overview) in one or more of these calls, you can query for incremental changes in the contacts in that folder. This allows you to maintain and synchronize a local store of a user's contacts without having to fetch the entire set of contacts from the server every time.</span></span>  

## <a name="permissions"></a><span data-ttu-id="90a06-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="90a06-109">Permissions</span></span>
<span data-ttu-id="90a06-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="90a06-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="90a06-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="90a06-112">Permission type</span></span>      | <span data-ttu-id="90a06-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="90a06-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="90a06-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="90a06-114">Delegated (work or school account)</span></span> | <span data-ttu-id="90a06-115">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="90a06-115">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="90a06-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="90a06-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="90a06-117">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="90a06-117">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="90a06-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="90a06-118">Application</span></span> | <span data-ttu-id="90a06-119">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="90a06-119">Contacts.Read, Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="90a06-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="90a06-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/contactFolders/{id}/contacts/delta
GET /users/<id>/contactFolders/{id}/contacts/delta
```

## <a name="query-parameters"></a><span data-ttu-id="90a06-121">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="90a06-121">Query parameters</span></span>

<span data-ttu-id="90a06-p104">El seguimiento de cambios en los contactos conlleva al menos una llamada de una función **delta**. Si usa cualquier parámetro de consulta (distinto de `$deltatoken` y `$skiptoken`), debe especificarlo en la solicitud **delta** inicial. Microsoft Graph codifica automáticamente cualquier parámetro especificado en la parte del token de la URL `nextLink` o `deltaLink` proporcionada en la respuesta. Solo debe especificar una vez por adelantado los parámetros de consulta deseados. En solicitudes posteriores, basta con copiar y aplicar la dirección URL `nextLink` o `deltaLink` de la respuesta anterior, dado que la dirección URL ya incluye los parámetros codificados deseados.</span><span class="sxs-lookup"><span data-stu-id="90a06-p104">Tracking changes in contacts incurs a round of one or more **delta** function calls. If you use any query parameter (other than `$deltatoken` and `$skiptoken`), you must specify it in the initial **delta** request. Microsoft Graph automatically encodes any specified parameters into the token portion of the `nextLink` or `deltaLink` URL provided in the response. You only need to specify any desired query parameters once upfront. In subsequent requests, simply copy and apply the `nextLink` or `deltaLink` URL from the previous response, as that URL already includes the encoded, desired parameters.</span></span>

| <span data-ttu-id="90a06-127">Parámetro de consulta</span><span class="sxs-lookup"><span data-stu-id="90a06-127">Query parameter</span></span>      | <span data-ttu-id="90a06-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="90a06-128">Type</span></span>   |<span data-ttu-id="90a06-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="90a06-129">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="90a06-130">$deltatoken</span><span class="sxs-lookup"><span data-stu-id="90a06-130">$deltatoken</span></span> | <span data-ttu-id="90a06-131">string</span><span class="sxs-lookup"><span data-stu-id="90a06-131">string</span></span> | <span data-ttu-id="90a06-p105">[Token de estado](/graph/delta-query-overview) que se devuelve en la dirección URL de `deltaLink` de la llamada de función **delta** anterior para la misma colección de contactos. Indica el progreso de la ronda de seguimiento de cambios. Guarde y aplique toda la dirección URL `deltaLink`, incluido este token, en la primera solicitud de la siguiente ronda de seguimiento de cambios de la colección.</span><span class="sxs-lookup"><span data-stu-id="90a06-p105">A [state token](/graph/delta-query-overview) returned in the `deltaLink` URL of the previous **delta** function call for the same contact collection, indicating the completion of that round of change tracking. Save and apply the entire `deltaLink` URL including this token in the first request of the next round of change tracking for that collection.</span></span>|
| <span data-ttu-id="90a06-134">$skiptoken</span><span class="sxs-lookup"><span data-stu-id="90a06-134">$skiptoken</span></span> | <span data-ttu-id="90a06-135">string</span><span class="sxs-lookup"><span data-stu-id="90a06-135">string</span></span> | <span data-ttu-id="90a06-136">[Token de estado](/graph/delta-query-overview) que se devuelve en la dirección URL de `nextLink` de la llamada de función **delta**. Indica que debe realizarse el seguimiento de más cambios en la misma colección de contactos.</span><span class="sxs-lookup"><span data-stu-id="90a06-136">A [state token](/graph/delta-query-overview) returned in the `nextLink` URL of the previous **delta** function call, indicating there are further changes to be tracked in the same contact collection.</span></span> |

### <a name="odata-query-parameters"></a><span data-ttu-id="90a06-137">Parámetros de consulta de OData</span><span class="sxs-lookup"><span data-stu-id="90a06-137">OData query parameters</span></span>

- <span data-ttu-id="90a06-p106">Puede utilizar un parámetro de consulta `$select` como en cualquier solicitud GET para especificar solo las propiedades que necesita para un mejor rendimiento. Siempre se devuelve la propiedad _id_.</span><span class="sxs-lookup"><span data-stu-id="90a06-p106">You can use a `$select` query parameter as in any GET request to specify only the properties your need for best performance. The _id_ property is always returned.</span></span> 


## <a name="request-headers"></a><span data-ttu-id="90a06-140">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="90a06-140">Request headers</span></span>
| <span data-ttu-id="90a06-141">Nombre</span><span class="sxs-lookup"><span data-stu-id="90a06-141">Name</span></span>       | <span data-ttu-id="90a06-142">Tipo</span><span class="sxs-lookup"><span data-stu-id="90a06-142">Type</span></span> | <span data-ttu-id="90a06-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="90a06-143">Description</span></span> |
|:---------------|:----------|:----------|
| <span data-ttu-id="90a06-144">Autorización</span><span class="sxs-lookup"><span data-stu-id="90a06-144">Authorization</span></span>  | <span data-ttu-id="90a06-145">string</span><span class="sxs-lookup"><span data-stu-id="90a06-145">string</span></span>  | <span data-ttu-id="90a06-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="90a06-p107">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="90a06-148">Content-Type</span><span class="sxs-lookup"><span data-stu-id="90a06-148">Content-Type</span></span>  | <span data-ttu-id="90a06-149">string</span><span class="sxs-lookup"><span data-stu-id="90a06-149">string</span></span>  | <span data-ttu-id="90a06-p108">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="90a06-p108">application/json. Required.</span></span> |
| <span data-ttu-id="90a06-152">Prefer</span><span class="sxs-lookup"><span data-stu-id="90a06-152">Prefer</span></span> | <span data-ttu-id="90a06-153">string</span><span class="sxs-lookup"><span data-stu-id="90a06-153">string</span></span>  | <span data-ttu-id="90a06-p109">odata.maxpagesize={x}. Opcional.</span><span class="sxs-lookup"><span data-stu-id="90a06-p109">odata.maxpagesize={x}. Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="90a06-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="90a06-156">Response</span></span>

<span data-ttu-id="90a06-157">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto de colección [contacto](../resources/contact.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="90a06-157">If successful, this method returns a `200 OK` response code and [contact](../resources/contact.md) collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="90a06-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="90a06-158">Example</span></span>
##### <a name="request"></a><span data-ttu-id="90a06-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="90a06-159">Request</span></span>
<span data-ttu-id="90a06-160">En el ejemplo siguiente se muestra cómo realizar una llamada de función **delta** única, usar un parámetro `$select` para obtener solo la propiedad **displayName** de cada contacto, y limitar el número máximo de contactos en el cuerpo de la respuesta a 2.</span><span class="sxs-lookup"><span data-stu-id="90a06-160">The following example shows how to make a single **delta** function call, use the `$select` parameter to get only each contact's **displayName** property, and limit the maximum number of contacts in the response body to 2.</span></span>

<span data-ttu-id="90a06-161">Para realizar un seguimiento de los contactos en las carpetas, debería realizar al menos una llamada de función **delta**, con unos tokens de estado adecuados, para obtener el conjunto de cambios incrementales desde la última consulta delta.</span><span class="sxs-lookup"><span data-stu-id="90a06-161">To track changes in the contacts in a folder, you would make one or more **delta** function calls, with appropriate state tokens, to get the set of incremental changes since the last delta query.</span></span> 

<span data-ttu-id="90a06-p110">Encontrará un ejemplo similar en el que se muestra cómo usar los tokens de estado para realizar un seguimiento de los cambios en los mensajes de una carpeta de correo: [Obtener los cambios incrementales en los mensajes de una carpeta](/graph/delta-query-messages). Las diferencias principales entre realizar un seguimiento de los contactos y realizar un seguimiento de los mensajes en una carpeta están en las direcciones URL de consulta delta. Además, las respuestas de consulta devuelven colecciones **contact** en lugar de colecciones **message**.</span><span class="sxs-lookup"><span data-stu-id="90a06-p110">You can find a similar example that shows how to use the state tokens to track changes in the messages of a mail folder: [Get incremental changes to messages in a folder](/graph/delta-query-messages). The main differences between tracking contacts and tracking messages in a folder are in the delta query request URLs, and the query responses returning **contact** rather than **message** collections.</span></span>
 
<!-- {
  "blockType": "request",
  "name": "contact_delta"
}-->
```http
GET https://graph.microsoft.com/beta/me/contactFolders/{id}/contacts/delta?$select=displayName

Prefer: odata.maxpagesize=2
```

##### <a name="response"></a><span data-ttu-id="90a06-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="90a06-164">Response</span></span>
<span data-ttu-id="90a06-165">Si la solicitud es correcta, la respuesta debería incluir un símbolo de estado, que puede ser un _skipToken_</span><span class="sxs-lookup"><span data-stu-id="90a06-165">If the request is successful, the response would include a state token, which is either a _skipToken_</span></span>  
<span data-ttu-id="90a06-p111">(en un encabezado de respuesta de _@odata.nextLink_) o un _deltaToken_ (en un encabezado de respuesta de _@odata.deltaLink_). Respectivamente, indican si debe continuar con la ronda, o bien si ha terminado de obtener todos los cambios de la ronda.</span><span class="sxs-lookup"><span data-stu-id="90a06-p111">(in an _@odata.nextLink_ response header) or a _deltaToken_ (in an _@odata.deltaLink_ response header). Respectively, they indicate whether you should continue with the round or you have completed getting all the changes for that round.</span></span>

<span data-ttu-id="90a06-168">La respuesta siguiente muestra un _skipToken_ en un encabezado de respuesta de _@odata.nextLink_.</span><span class="sxs-lookup"><span data-stu-id="90a06-168">The response below shows a _skipToken_ in an _@odata.nextLink_ response header.</span></span>

<span data-ttu-id="90a06-p112">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="90a06-p112">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contact",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 337

{
  "@odata.nextLink":"https://graph.microsoft.com/beta/me/contactfolders('{id}')/contacts/delta?$skiptoken={_skipToken_}",
  "value": [
    {
      "parentFolderId": "parentFolderId-value",
      "birthday": "2016-10-19T10:37:00Z",
      "fileAs": "fileAs-value",
      "displayName": "displayName-value",
      "givenName": "givenName-value",
      "initials": "initials-value"
    }
  ]
}
```

### <a name="see-also"></a><span data-ttu-id="90a06-171">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="90a06-171">See also</span></span>

- [<span data-ttu-id="90a06-172">Consulta delta de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="90a06-172">Microsoft Graph delta query</span></span>](/graph/delta-query-overview)
- [<span data-ttu-id="90a06-173">Obtener los cambios incrementales en los mensajes de una carpeta</span><span class="sxs-lookup"><span data-stu-id="90a06-173">Get incremental changes to messages in a folder</span></span>](/graph/delta-query-messages)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "contact: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
