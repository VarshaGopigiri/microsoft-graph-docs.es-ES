---
title: Enumerar publicaciones
description: 'Obtenga las publicaciones del hilo especificado. Puede especificar la conversación primario y el subproceso, o bien, '
localization_priority: Normal
ms.openlocfilehash: 60c8cb3e369653c1ae5440a64195fb3ecfbfb513
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805323"
---
# <a name="list-posts"></a><span data-ttu-id="ba3ab-104">Enumerar publicaciones</span><span class="sxs-lookup"><span data-stu-id="ba3ab-104">List posts</span></span>

<span data-ttu-id="ba3ab-p102">Obtiene las publicaciones del hilo especificado. Puede especificar la conversación primaria y el hilo, o bien, especificar el hilo sin hacer referencia a la conversación primaria.</span><span class="sxs-lookup"><span data-stu-id="ba3ab-p102">Get the posts of the specified thread. You can specify both the parent conversation and the thread, or, you can specify the thread without referencing the parent conversation.</span></span>

## <a name="permissions"></a><span data-ttu-id="ba3ab-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="ba3ab-107">Permissions</span></span>
<span data-ttu-id="ba3ab-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ba3ab-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ba3ab-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ba3ab-110">Permission type</span></span>      | <span data-ttu-id="ba3ab-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ba3ab-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ba3ab-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ba3ab-112">Delegated (work or school account)</span></span> | <span data-ttu-id="ba3ab-113">Group.ReadWrite.All, Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="ba3ab-113">Group.ReadWrite.All, Group.Read.All</span></span>    |
|<span data-ttu-id="ba3ab-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ba3ab-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ba3ab-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ba3ab-115">Not supported.</span></span>    |
|<span data-ttu-id="ba3ab-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ba3ab-116">Application</span></span> | <span data-ttu-id="ba3ab-117">Group.ReadWrite.All, Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="ba3ab-117">Group.ReadWrite.All, Group.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="ba3ab-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ba3ab-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/threads/{id}/posts
GET /groups/{id}/conversations/{id}/threads/{id}/posts

```
## <a name="optional-query-parameters"></a><span data-ttu-id="ba3ab-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ba3ab-119">Optional query parameters</span></span>
<span data-ttu-id="ba3ab-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ba3ab-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="ba3ab-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ba3ab-121">Request headers</span></span>
| <span data-ttu-id="ba3ab-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba3ab-122">Header</span></span>       | <span data-ttu-id="ba3ab-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ba3ab-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ba3ab-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="ba3ab-124">Authorization</span></span>  | <span data-ttu-id="ba3ab-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ba3ab-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ba3ab-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ba3ab-127">Request body</span></span>
<span data-ttu-id="ba3ab-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ba3ab-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ba3ab-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ba3ab-129">Response</span></span>

<span data-ttu-id="ba3ab-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Post](../resources/post.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ba3ab-130">If successful, this method returns a `200 OK` response code and collection of [Post](../resources/post.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ba3ab-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ba3ab-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ba3ab-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ba3ab-132">Request</span></span>
<span data-ttu-id="ba3ab-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ba3ab-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_posts"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/threads/{id}/posts
```
##### <a name="response"></a><span data-ttu-id="ba3ab-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ba3ab-134">Response</span></span>
<span data-ttu-id="ba3ab-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ba3ab-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
