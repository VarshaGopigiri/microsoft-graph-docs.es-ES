---
title: 'mailFolder: delta'
description: Obtenga un conjunto de carpetas de correo que se hayan agregado, eliminado o quitado del buzón del usuario.
localization_priority: Normal
ms.openlocfilehash: 58b8d0b6b8129b45f9b1d9a205a37657d5eec5d7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27810986"
---
# <a name="mailfolder-delta"></a><span data-ttu-id="7b86c-103">mailFolder: delta</span><span class="sxs-lookup"><span data-stu-id="7b86c-103">mailFolder: delta</span></span>

<span data-ttu-id="7b86c-104">Obtenga un conjunto de carpetas de correo que se hayan agregado, eliminado o quitado del buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="7b86c-104">Get a set of mail folders that have been added, deleted, or removed from the user's mailbox.</span></span>

<span data-ttu-id="7b86c-p101">Las llamadas de una función **delta** para las carpetas de correo de un buzón funcionan de forma similar a una solicitud GET, salvo que, al aplicar correctamente [tokens de estado](/graph/delta-query-overview) en al menos una de estas llamadas, puede realizar una consulta para obtener los cambios incrementales en las carpetas de correo. Esto permite mantener y sincronizar un almacén local de carpetas de correo de un usuario, sin tener que capturar cada vez todas las carpetas de correo de ese buzón desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="7b86c-p101">A **delta** function call for mail folders in a mailbox is similar to a GET request, except that by appropriately applying [state tokens](/graph/delta-query-overview) in one or more of these calls, you can query for incremental changes in the mail folders. This allows you to maintain and synchronize a local store of a user's mail folders without having to fetch all the mail folders of that mailbox from the server every time.</span></span>

## <a name="permissions"></a><span data-ttu-id="7b86c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="7b86c-107">Permissions</span></span>
<span data-ttu-id="7b86c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7b86c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="7b86c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7b86c-110">Permission type</span></span>      | <span data-ttu-id="7b86c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7b86c-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7b86c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7b86c-112">Delegated (work or school account)</span></span> | <span data-ttu-id="7b86c-113">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7b86c-113">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="7b86c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7b86c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7b86c-115">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7b86c-115">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="7b86c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7b86c-116">Application</span></span> | <span data-ttu-id="7b86c-117">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7b86c-117">Mail.Read, Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="7b86c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7b86c-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/delta
GET /users/{id}/mailFolders/delta
```

## <a name="query-parameters"></a><span data-ttu-id="7b86c-119">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="7b86c-119">Query parameters</span></span>

<span data-ttu-id="7b86c-p103">El seguimiento de cambios en las carpetas de correo conlleva al menos una llamada de una función **delta**. Si usa cualquier parámetro de consulta (distinto de `$deltatoken` y `$skiptoken`), debe especificarlo en la solicitud **delta** inicial. Microsoft Graph codifica automáticamente cualquier parámetro especificado en la parte del token de la URL `nextLink` o `deltaLink` proporcionada en la respuesta. Solo debe especificar los parámetros de consulta deseados una vez por adelantado. En solicitudes posteriores, basta con copiar y aplicar la dirección URL `nextLink` o `deltaLink` de la respuesta anterior, dado que la dirección URL ya incluye los parámetros codificados deseados.</span><span class="sxs-lookup"><span data-stu-id="7b86c-p103">Tracking changes in mail folders incurs a round of one or more **delta** function calls. If you use any query parameter (other than `$deltatoken` and `$skiptoken`), you must specify it in the initial **delta** request. Microsoft Graph automatically encodes any specified parameters into the token portion of the `nextLink` or `deltaLink` URL provided in the response. You only need to specify any desired query parameters once upfront. In subsequent requests, simply copy and apply the `nextLink` or `deltaLink` URL from the previous response, as that URL already includes the encoded, desired parameters.</span></span>

| <span data-ttu-id="7b86c-125">Parámetro de consulta</span><span class="sxs-lookup"><span data-stu-id="7b86c-125">Query parameter</span></span>      | <span data-ttu-id="7b86c-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="7b86c-126">Type</span></span>   |<span data-ttu-id="7b86c-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b86c-127">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="7b86c-128">$deltatoken</span><span class="sxs-lookup"><span data-stu-id="7b86c-128">$deltatoken</span></span> | <span data-ttu-id="7b86c-129">string</span><span class="sxs-lookup"><span data-stu-id="7b86c-129">string</span></span> | <span data-ttu-id="7b86c-p104">Un [token de estado](/graph/delta-query-overview) que se devuelve en la dirección URL de `deltaLink` de la llamada de función **delta** anterior para la misma colección de carpetas de correo. Indica el progreso de la ronda de seguimiento de cambios. Guarde y aplique toda la dirección URL `deltaLink`, incluido este token, en la primera solicitud de la siguiente ronda de seguimiento de cambios de la colección.</span><span class="sxs-lookup"><span data-stu-id="7b86c-p104">A [state token](/graph/delta-query-overview) returned in the `deltaLink` URL of the previous **delta** function call for the same mail folder collection, indicating the completion of that round of change tracking. Save and apply the entire `deltaLink` URL including this token in the first request of the next round of change tracking for that collection.</span></span>|
| <span data-ttu-id="7b86c-132">$skiptoken</span><span class="sxs-lookup"><span data-stu-id="7b86c-132">$skiptoken</span></span> | <span data-ttu-id="7b86c-133">string</span><span class="sxs-lookup"><span data-stu-id="7b86c-133">string</span></span> | <span data-ttu-id="7b86c-134">Un [token de estado](/graph/delta-query-overview) que se devuelve en la dirección URL de `nextLink` de la llamada de función **delta**. Indica que debe realizarse el seguimiento de más cambios en la misma colección de carpetas de correo.</span><span class="sxs-lookup"><span data-stu-id="7b86c-134">A [state token](/graph/delta-query-overview) returned in the `nextLink` URL of the previous **delta** function call, indicating there are further changes to be tracked in the same mail folder collection.</span></span> |

### <a name="odata-query-parameters"></a><span data-ttu-id="7b86c-135">Parámetros de consulta de OData</span><span class="sxs-lookup"><span data-stu-id="7b86c-135">OData query parameters</span></span>

<span data-ttu-id="7b86c-p105">Puede utilizar un parámetro de consulta `$select` como en cualquier solicitud GET para especificar solo las propiedades que necesita para un mejor rendimiento. Siempre se devuelve la propiedad _id_.</span><span class="sxs-lookup"><span data-stu-id="7b86c-p105">You can use a `$select` query parameter as in any GET request to specify only the properties your need for best performance. The _id_ property is always returned.</span></span> 

## <a name="request-headers"></a><span data-ttu-id="7b86c-138">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7b86c-138">Request headers</span></span>
| <span data-ttu-id="7b86c-139">Nombre</span><span class="sxs-lookup"><span data-stu-id="7b86c-139">Name</span></span>       | <span data-ttu-id="7b86c-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="7b86c-140">Type</span></span> | <span data-ttu-id="7b86c-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b86c-141">Description</span></span> |
|:---------------|:----------|:----------|
| <span data-ttu-id="7b86c-142">Autorización</span><span class="sxs-lookup"><span data-stu-id="7b86c-142">Authorization</span></span>  | <span data-ttu-id="7b86c-143">string</span><span class="sxs-lookup"><span data-stu-id="7b86c-143">string</span></span>  | <span data-ttu-id="7b86c-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7b86c-p106">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="7b86c-146">Content-Type</span><span class="sxs-lookup"><span data-stu-id="7b86c-146">Content-Type</span></span>  | <span data-ttu-id="7b86c-147">string</span><span class="sxs-lookup"><span data-stu-id="7b86c-147">string</span></span>  | <span data-ttu-id="7b86c-p107">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7b86c-p107">application/json. Required.</span></span> |
| <span data-ttu-id="7b86c-150">Prefer</span><span class="sxs-lookup"><span data-stu-id="7b86c-150">Prefer</span></span> | <span data-ttu-id="7b86c-151">string</span><span class="sxs-lookup"><span data-stu-id="7b86c-151">string</span></span>  | <span data-ttu-id="7b86c-p108">odata.maxpagesize={x}. Opcional.</span><span class="sxs-lookup"><span data-stu-id="7b86c-p108">odata.maxpagesize={x}. Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="7b86c-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7b86c-154">Response</span></span>

<span data-ttu-id="7b86c-155">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto de colección [mailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7b86c-155">If successful, this method returns a `200 OK` response code and [mailFolder](../resources/mailfolder.md) collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7b86c-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7b86c-156">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7b86c-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7b86c-157">Request</span></span>
<span data-ttu-id="7b86c-158">En el ejemplo siguiente se muestra cómo realizar una llamada de función **delta** única y limitar el número máximo de carpetas de correo en el cuerpo de la respuesta a 2.</span><span class="sxs-lookup"><span data-stu-id="7b86c-158">The following example shows how to make a single **delta** function call, and limit the maximum number of mail folders in the response body to 2.</span></span>

<span data-ttu-id="7b86c-159">Para realizar un seguimiento de los cambios de las carpetas de correo de un buzón, debería realizar al menos una llamada de función **delta**, con unos tokens de estado adecuados, para obtener el conjunto de cambios incrementales desde la última consulta delta.</span><span class="sxs-lookup"><span data-stu-id="7b86c-159">To track changes in the mail folders of a mailbox, you would make one or more **delta** function calls, with appropriate state tokens, to get the set of incremental changes since the last delta query.</span></span> 

<span data-ttu-id="7b86c-p109">Encontrará un ejemplo similar en el que se muestra cómo usar los tokens de estado para realizar un seguimiento de los cambios en los mensajes de una carpeta de correo: [Obtener los cambios incrementales en los mensajes de una carpeta](/graph/delta-query-messages). Las diferencias principales entre realizar un seguimiento de las carpetas de correo y realizar un seguimiento de los mensajes en una carpeta están en las direcciones URL de consulta delta. Además, las respuestas de consulta devuelven colecciones **mailFolder** en lugar de colecciones **message**.</span><span class="sxs-lookup"><span data-stu-id="7b86c-p109">You can find a similar example that shows how to use the state tokens to track changes in the messages of a mail folder: [Get incremental changes to messages in a folder](/graph/delta-query-messages). The main differences between tracking mail folders and tracking messages in a folder are in the delta query request URLs, and the query responses returning **mailFolder** rather than **message** collections.</span></span>

<!-- {
  "blockType": "request",
  "name": "mailfolder_delta"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/mailFolders/delta

Prefer: odata.maxpagesize=2
```

##### <a name="response"></a><span data-ttu-id="7b86c-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7b86c-162">Response</span></span>

<span data-ttu-id="7b86c-163">Si la solicitud es correcta, la respuesta debería incluir un símbolo de estado, que puede ser un _skipToken_</span><span class="sxs-lookup"><span data-stu-id="7b86c-163">If the request is successful, the response would include a state token, which is either a _skipToken_</span></span>  
<span data-ttu-id="7b86c-p110">(en un encabezado de respuesta de _@odata.nextLink_) o un _deltaToken_ (en un encabezado de respuesta de _@odata.deltaLink_). Respectivamente, indican si debe continuar con la ronda, o bien si ha terminado de obtener todos los cambios de la ronda.</span><span class="sxs-lookup"><span data-stu-id="7b86c-p110">(in an _@odata.nextLink_ response header) or a _deltaToken_ (in an _@odata.deltaLink_ response header). Respectively, they indicate whether you should continue with the round or you have completed getting all the changes for that round.</span></span>

<span data-ttu-id="7b86c-166">La respuesta siguiente muestra un _skipToken_ en un encabezado de respuesta de _@odata.nextLink_.</span><span class="sxs-lookup"><span data-stu-id="7b86c-166">The response below shows a _skipToken_ in an _@odata.nextLink_ response header.</span></span>

<span data-ttu-id="7b86c-p111">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7b86c-p111">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailFolder",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 254

{
  "@odata.nextLink":"https://graph.microsoft.com/v1.0/me/mailfolders/delta?$skiptoken={_skipToken_}",
  "value": [
    {
      "displayName": "displayName-value",
      "parentFolderId": "parentFolderId-value",
      "childFolderCount": 99,
      "unreadItemCount": 99,
      "totalItemCount": 99
    }
  ]
}
```

### <a name="see-also"></a><span data-ttu-id="7b86c-169">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7b86c-169">See also</span></span>

- [<span data-ttu-id="7b86c-170">Usar la consulta delta para realizar el seguimiento de los cambios en datos de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="7b86c-170">Use delta query to track changes in Microsoft Graph data</span></span>](/graph/delta-query-overview)
- [<span data-ttu-id="7b86c-171">Obtener los cambios incrementales en los mensajes de una carpeta</span><span class="sxs-lookup"><span data-stu-id="7b86c-171">Get incremental changes to messages in a folder</span></span>](/graph/delta-query-messages)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mailFolder: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
