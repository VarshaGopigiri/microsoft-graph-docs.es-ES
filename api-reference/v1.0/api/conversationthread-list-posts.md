---
title: Enumerar publicaciones
description: 'Obtenga las publicaciones del hilo especificado. Puede especificar la conversación primario y el subproceso, o bien, '
ms.openlocfilehash: 35c4c178b02cb700ab21a324c29a4522203fad19
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030166"
---
# <a name="list-posts"></a><span data-ttu-id="afecc-104">Enumerar publicaciones</span><span class="sxs-lookup"><span data-stu-id="afecc-104">List posts</span></span>

<span data-ttu-id="afecc-p102">Obtiene las publicaciones del hilo especificado. Puede especificar la conversación primaria y el hilo, o bien, especificar el hilo sin hacer referencia a la conversación primaria.</span><span class="sxs-lookup"><span data-stu-id="afecc-p102">Get the posts of the specified thread. You can specify both the parent conversation and the thread, or, you can specify the thread without referencing the parent conversation.</span></span>

## <a name="permissions"></a><span data-ttu-id="afecc-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="afecc-107">Permissions</span></span>
<span data-ttu-id="afecc-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="afecc-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="afecc-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="afecc-110">Permission type</span></span>      | <span data-ttu-id="afecc-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="afecc-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="afecc-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="afecc-112">Delegated (work or school account)</span></span> | <span data-ttu-id="afecc-113">Group.ReadWrite.All, Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="afecc-113">Group.ReadWrite.All, Group.Read.All</span></span>    |
|<span data-ttu-id="afecc-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="afecc-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="afecc-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="afecc-115">Not supported.</span></span>    |
|<span data-ttu-id="afecc-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="afecc-116">Application</span></span> | <span data-ttu-id="afecc-117">Group.ReadWrite.All, Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="afecc-117">Group.ReadWrite.All, Group.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="afecc-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="afecc-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/threads/{id}/posts
GET /groups/{id}/conversations/{id}/threads/{id}/posts

```
## <a name="optional-query-parameters"></a><span data-ttu-id="afecc-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="afecc-119">Optional query parameters</span></span>
<span data-ttu-id="afecc-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="afecc-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="afecc-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="afecc-121">Request headers</span></span>
| <span data-ttu-id="afecc-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="afecc-122">Header</span></span>       | <span data-ttu-id="afecc-123">Valor</span><span class="sxs-lookup"><span data-stu-id="afecc-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="afecc-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="afecc-124">Authorization</span></span>  | <span data-ttu-id="afecc-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="afecc-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="afecc-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="afecc-127">Request body</span></span>
<span data-ttu-id="afecc-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="afecc-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="afecc-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="afecc-129">Response</span></span>

<span data-ttu-id="afecc-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Post](../resources/post.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="afecc-130">If successful, this method returns a `200 OK` response code and collection of [Post](../resources/post.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="afecc-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="afecc-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="afecc-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="afecc-132">Request</span></span>
<span data-ttu-id="afecc-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="afecc-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_posts"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/threads/{id}/posts
```
##### <a name="response"></a><span data-ttu-id="afecc-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="afecc-134">Response</span></span>
<span data-ttu-id="afecc-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="afecc-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.post",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 523

{
  "value": [
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
      },
      "conversationThreadId": "conversationThreadId-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List posts",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
