---
title: List conversations
description: Recupera la lista de conversaciones en este grupo.
author: dkershaw10
ms.openlocfilehash: 81b5b8deb9389d5aff6be9e537bb65ef43d366b9
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27321402"
---
# <a name="list-conversations"></a><span data-ttu-id="87240-103">Lista de conversaciones</span><span class="sxs-lookup"><span data-stu-id="87240-103">List conversations</span></span>
<span data-ttu-id="87240-104">Recupera la lista de [conversaciones](../resources/conversation.md) en este grupo.</span><span class="sxs-lookup"><span data-stu-id="87240-104">Retrieve the list of [conversations](../resources/conversation.md) in this group.</span></span>

## <a name="permissions"></a><span data-ttu-id="87240-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="87240-105">Permissions</span></span>
<span data-ttu-id="87240-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="87240-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="87240-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="87240-108">Permission type</span></span>      | <span data-ttu-id="87240-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="87240-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="87240-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="87240-110">Delegated (work or school account)</span></span> | <span data-ttu-id="87240-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="87240-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="87240-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="87240-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="87240-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="87240-113">Not supported.</span></span>    |
|<span data-ttu-id="87240-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="87240-114">Application</span></span> | <span data-ttu-id="87240-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="87240-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="87240-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="87240-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/conversations
```

## <a name="optional-query-parameters"></a><span data-ttu-id="87240-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="87240-117">Optional query parameters</span></span>
<span data-ttu-id="87240-118">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="87240-118">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="87240-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="87240-119">Request headers</span></span>
| <span data-ttu-id="87240-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87240-120">Header</span></span>       | <span data-ttu-id="87240-121">Valor</span><span class="sxs-lookup"><span data-stu-id="87240-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="87240-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="87240-122">Authorization</span></span>  | <span data-ttu-id="87240-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="87240-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="87240-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="87240-125">Request body</span></span>
<span data-ttu-id="87240-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="87240-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="87240-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="87240-127">Response</span></span>
<span data-ttu-id="87240-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos de [conversación](../resources/conversation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="87240-128">If successful, this method returns a `200 OK` response code and collection of [conversation](../resources/conversation.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="87240-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="87240-129">Example</span></span>
#### <a name="request"></a><span data-ttu-id="87240-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="87240-130">Request</span></span>
<span data-ttu-id="87240-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="87240-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_conversations"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/conversations
```
#### <a name="response"></a><span data-ttu-id="87240-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="87240-132">Response</span></span>
<span data-ttu-id="87240-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="87240-133">The following is an example of the response.</span></span>
><span data-ttu-id="87240-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="87240-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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