---
title: Obtener publicación
description: 'Obtenga las propiedades y relaciones de una publicación de un hilo determinado. Puede especificar tanto el primario '
author: dkershaw10
localization_priority: Normal
ms.prod: groups
ms.openlocfilehash: 8e724a664e708503daf5b30afdec04cccbb2fee4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27912942"
---
# <a name="get-post"></a><span data-ttu-id="1a26d-104">Obtener publicación</span><span class="sxs-lookup"><span data-stu-id="1a26d-104">Get post</span></span>

<span data-ttu-id="1a26d-p102">Obtiene las propiedades y relaciones de una publicación de un hilo determinado. Puede especificar la conversación primaria y el hilo, o bien, especificar el hilo sin hacer referencia a la conversación primaria.</span><span class="sxs-lookup"><span data-stu-id="1a26d-p102">Get the properties and relationships of a post in a specified thread. You can specify both the parent conversation and the thread, or, you can specify the thread without referencing the parent conversation.</span></span>

<span data-ttu-id="1a26d-107">Dado que el recurso **post** admite [extensiones](/graph/extensibility-overview), también puede utilizar la operación `GET` para obtener propiedades personalizadas y datos de extensión en una instancia **post**.</span><span class="sxs-lookup"><span data-stu-id="1a26d-107">Since the **post** resource supports [extensions](/graph/extensibility-overview), you can also use the `GET` operation to get custom properties and extension data in a **post** instance.</span></span>

## <a name="permissions"></a><span data-ttu-id="1a26d-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="1a26d-108">Permissions</span></span>
<span data-ttu-id="1a26d-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1a26d-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1a26d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1a26d-111">Permission type</span></span>      | <span data-ttu-id="1a26d-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1a26d-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1a26d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1a26d-113">Delegated (work or school account)</span></span> | <span data-ttu-id="1a26d-114">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1a26d-114">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="1a26d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1a26d-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1a26d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1a26d-116">Not supported.</span></span>    |
|<span data-ttu-id="1a26d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1a26d-117">Application</span></span> | <span data-ttu-id="1a26d-118">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1a26d-118">Group.Read.All, Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="1a26d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1a26d-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/threads/{id}/posts/{id}
GET /groups/{id}/conversations/{id}/threads/{id}/posts/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="1a26d-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1a26d-120">Optional query parameters</span></span>
<span data-ttu-id="1a26d-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1a26d-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="1a26d-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1a26d-122">Request headers</span></span>
| <span data-ttu-id="1a26d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1a26d-123">Header</span></span>       | <span data-ttu-id="1a26d-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1a26d-124">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="1a26d-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="1a26d-125">Authorization</span></span>  | <span data-ttu-id="1a26d-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a26d-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="1a26d-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1a26d-128">Request body</span></span>
<span data-ttu-id="1a26d-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1a26d-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1a26d-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1a26d-130">Response</span></span>

<span data-ttu-id="1a26d-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [post](../resources/post.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1a26d-131">If successful, this method returns a `200 OK` response code and [post](../resources/post.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="1a26d-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1a26d-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1a26d-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1a26d-133">Request</span></span>
<span data-ttu-id="1a26d-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1a26d-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_post"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/threads/{id}/posts/{id}
```
##### <a name="response"></a><span data-ttu-id="1a26d-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1a26d-135">Response</span></span>
<span data-ttu-id="1a26d-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1a26d-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.post"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 414

{
  "body": {
    "contentType": "",
    "content": "content-value"
  },
  "receivedDateTime": "datetime-value",
  "hasAttachments": true,
  "from": {
    "emailAddress": {
      "name": "name-value",
      "address": "address-value"
    }
  },
  "sender": {
    "emailAddress": {
      "name": "name-value",
      "address": "address-value"
    }
  }
}
```

## <a name="see-also"></a><span data-ttu-id="1a26d-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a26d-139">See also</span></span>

- [<span data-ttu-id="1a26d-140">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="1a26d-140">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="1a26d-141">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="1a26d-141">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
<!--
- [Add custom data to groups using schema extensions (preview)](/graph/extensibility-schema-groups)
-->


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get post",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
