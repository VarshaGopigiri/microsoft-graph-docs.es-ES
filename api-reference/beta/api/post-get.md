---
title: Obtener publicación
description: 'Obtenga las propiedades y relaciones de una publicación de un hilo determinado. Puede especificar tanto el primario '
author: dkershaw10
ms.openlocfilehash: 98bed589c1982411f3c0b989e28e04d2e6166466
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27361239"
---
# <a name="get-post"></a><span data-ttu-id="36601-104">Obtener publicación</span><span class="sxs-lookup"><span data-stu-id="36601-104">Get post</span></span>

> <span data-ttu-id="36601-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="36601-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="36601-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="36601-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="36601-p103">Obtiene las propiedades y relaciones de una publicación de un hilo determinado. Puede especificar la conversación primaria y el hilo, o bien, especificar el hilo sin hacer referencia a la conversación primaria.</span><span class="sxs-lookup"><span data-stu-id="36601-p103">Get the properties and relationships of a post in a specified thread. You can specify both the parent conversation and the thread, or, you can specify the thread without referencing the parent conversation.</span></span>

<span data-ttu-id="36601-109">Dado que el recurso **post** admite [extensiones](/graph/extensibility-overview), también puede utilizar la operación `GET` para obtener propiedades personalizadas y datos de extensión en una instancia **post**.</span><span class="sxs-lookup"><span data-stu-id="36601-109">Since the **post** resource supports [extensions](/graph/extensibility-overview), you can also use the `GET` operation to get custom properties and extension data in a **post** instance.</span></span>

## <a name="permissions"></a><span data-ttu-id="36601-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="36601-110">Permissions</span></span>
<span data-ttu-id="36601-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="36601-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="36601-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="36601-113">Permission type</span></span>      | <span data-ttu-id="36601-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="36601-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="36601-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="36601-115">Delegated (work or school account)</span></span> | <span data-ttu-id="36601-116">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="36601-116">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="36601-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="36601-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="36601-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="36601-118">Not supported.</span></span>    |
|<span data-ttu-id="36601-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="36601-119">Application</span></span> | <span data-ttu-id="36601-120">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="36601-120">Group.Read.All, Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="36601-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="36601-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/threads/{id}/posts/{id}
GET /groups/{id}/conversations/{id}/threads/{id}/posts/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="36601-122">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="36601-122">Optional query parameters</span></span>
<span data-ttu-id="36601-123">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="36601-123">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="36601-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="36601-124">Request headers</span></span>
| <span data-ttu-id="36601-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="36601-125">Header</span></span>       | <span data-ttu-id="36601-126">Valor</span><span class="sxs-lookup"><span data-stu-id="36601-126">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="36601-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="36601-127">Authorization</span></span>  | <span data-ttu-id="36601-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="36601-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="36601-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="36601-130">Request body</span></span>
<span data-ttu-id="36601-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="36601-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="36601-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="36601-132">Response</span></span>

<span data-ttu-id="36601-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [post](../resources/post.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="36601-133">If successful, this method returns a `200 OK` response code and [post](../resources/post.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="36601-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="36601-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="36601-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="36601-135">Request</span></span>
<span data-ttu-id="36601-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="36601-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_post"
}-->
```http
GET https://graph.microsoft.com/beta/groups/0d75b8dc-c42d-44dd-890a-751a99c0589f/threads/AAQkAD8EJUmcWwTJi06Cew==/posts/AQMkADgAAAIJbQAAAA==
```
##### <a name="response"></a><span data-ttu-id="36601-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="36601-137">Response</span></span>
<span data-ttu-id="36601-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="36601-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.post"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#groups('0d75b8dc-c42d-44dd-890a-751a99c0589f')/threads('AAQkAD8EJUmcWwTJi06Cew%3D%3D')/posts/$entity",
    "@odata.etag":"W/\"CQAAABYAAAC/3QURwysWS6IJYYw5exv4AAAAAAlK\"",
    "id":"AQMkADgAAAIJbQAAAA==",
    "createdDateTime":"2018-01-11T17:36:17Z",
    "lastModifiedDateTime":"2018-01-11T17:36:17Z",
    "importance": "normal",
    "changeKey":"CQAAABYAAAC/3QURwysWS6IJYYw5exv4AAAAAAlK",
    "categories":[

    ],
    "receivedDateTime":"2018-01-11T17:36:17Z",
    "hasAttachments":false,
    "body":{
        "contentType":"html",
        "content":"<html><body></body></html>"
    },
    "from":{
        "emailAddress":{
            "name":"Marketing",
            "address":"Marketing@M365B489948.onmicrosoft.com"
        }
    },
    "sender":{
        "emailAddress":{
            "name":"Marketing",
            "address":"Marketing@M365B489948.onmicrosoft.com"
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="36601-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="36601-141">See also</span></span>

- [<span data-ttu-id="36601-142">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="36601-142">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="36601-143">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="36601-143">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
- [<span data-ttu-id="36601-144">Agregar datos personalizados a grupos mediante extensiones de esquema (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="36601-144">Add custom data to groups using schema extensions (preview)</span></span>](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get post",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
