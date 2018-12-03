---
title: List conversations
description: Recupera la lista de conversaciones en este grupo.
ms.openlocfilehash: 7d62fb7f2944c2c368e842f3c0318ddf59852c47
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030677"
---
# <a name="list-conversations"></a><span data-ttu-id="541e7-103">Lista de conversaciones</span><span class="sxs-lookup"><span data-stu-id="541e7-103">List conversations</span></span>
<span data-ttu-id="541e7-104">Recupera la lista de [conversaciones](../resources/conversation.md) en este grupo.</span><span class="sxs-lookup"><span data-stu-id="541e7-104">Retrieve the list of [conversations](../resources/conversation.md) in this group.</span></span>

## <a name="permissions"></a><span data-ttu-id="541e7-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="541e7-105">Permissions</span></span>
<span data-ttu-id="541e7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="541e7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="541e7-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="541e7-108">Permission type</span></span>      | <span data-ttu-id="541e7-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="541e7-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="541e7-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="541e7-110">Delegated (work or school account)</span></span> | <span data-ttu-id="541e7-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="541e7-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="541e7-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="541e7-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="541e7-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="541e7-113">Not supported.</span></span>    |
|<span data-ttu-id="541e7-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="541e7-114">Application</span></span> | <span data-ttu-id="541e7-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="541e7-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="541e7-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="541e7-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/conversations
```

## <a name="optional-query-parameters"></a><span data-ttu-id="541e7-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="541e7-117">Optional query parameters</span></span>
<span data-ttu-id="541e7-118">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="541e7-118">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="541e7-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="541e7-119">Request headers</span></span>
| <span data-ttu-id="541e7-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="541e7-120">Header</span></span>       | <span data-ttu-id="541e7-121">Valor</span><span class="sxs-lookup"><span data-stu-id="541e7-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="541e7-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="541e7-122">Authorization</span></span>  | <span data-ttu-id="541e7-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="541e7-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="541e7-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="541e7-125">Request body</span></span>
<span data-ttu-id="541e7-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="541e7-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="541e7-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="541e7-127">Response</span></span>
<span data-ttu-id="541e7-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos de [conversación](../resources/conversation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="541e7-128">If successful, this method returns a `200 OK` response code and collection of [conversation](../resources/conversation.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="541e7-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="541e7-129">Example</span></span>
#### <a name="request"></a><span data-ttu-id="541e7-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="541e7-130">Request</span></span>
<span data-ttu-id="541e7-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="541e7-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_conversations"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/conversations
```
#### <a name="response"></a><span data-ttu-id="541e7-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="541e7-132">Response</span></span>
<span data-ttu-id="541e7-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="541e7-133">The following is an example of the response.</span></span>
><span data-ttu-id="541e7-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="541e7-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversation",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 262

{
  "value": [
    {
      "topic": "topic-value",
      "hasAttachments": true,
      "lastDeliveredDateTime": "datetime-value",
      "uniqueSenders": [
        "uniqueSenders-value"
      ],
      "preview": "preview-value",
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List conversations",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->