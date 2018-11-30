---
title: List conversations
description: Recupera la lista de conversaciones en este grupo.
ms.openlocfilehash: 97351b6b6afb8ed671704e77801d380e59694157
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090415"
---
# <a name="list-conversations"></a><span data-ttu-id="461be-103">Lista de conversaciones</span><span class="sxs-lookup"><span data-stu-id="461be-103">List conversations</span></span>

> <span data-ttu-id="461be-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="461be-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="461be-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="461be-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="461be-106">Recupera la lista de [conversaciones](../resources/conversation.md) en este grupo.</span><span class="sxs-lookup"><span data-stu-id="461be-106">Retrieve the list of [conversations](../resources/conversation.md) in this group.</span></span>

## <a name="permissions"></a><span data-ttu-id="461be-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="461be-107">Permissions</span></span>
<span data-ttu-id="461be-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="461be-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="461be-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="461be-110">Permission type</span></span>      | <span data-ttu-id="461be-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="461be-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="461be-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="461be-112">Delegated (work or school account)</span></span> | <span data-ttu-id="461be-113">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="461be-113">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="461be-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="461be-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="461be-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="461be-115">Not supported.</span></span>    |
|<span data-ttu-id="461be-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="461be-116">Application</span></span> | <span data-ttu-id="461be-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="461be-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="461be-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="461be-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/conversations
```

## <a name="optional-query-parameters"></a><span data-ttu-id="461be-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="461be-119">Optional query parameters</span></span>
<span data-ttu-id="461be-120">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="461be-120">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="461be-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="461be-121">Request headers</span></span>
| <span data-ttu-id="461be-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="461be-122">Header</span></span>       | <span data-ttu-id="461be-123">Valor</span><span class="sxs-lookup"><span data-stu-id="461be-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="461be-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="461be-124">Authorization</span></span>  | <span data-ttu-id="461be-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="461be-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="461be-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="461be-127">Request body</span></span>
<span data-ttu-id="461be-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="461be-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="461be-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="461be-129">Response</span></span>
<span data-ttu-id="461be-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos de [conversación](../resources/conversation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="461be-130">If successful, this method returns a `200 OK` response code and collection of [conversation](../resources/conversation.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="461be-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="461be-131">Example</span></span>
#### <a name="request"></a><span data-ttu-id="461be-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="461be-132">Request</span></span>
<span data-ttu-id="461be-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="461be-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_conversations"
}-->
```http
GET https://graph.microsoft.com/beta/groups/{id}/conversations
```

#### <a name="response"></a><span data-ttu-id="461be-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="461be-134">Response</span></span>
<span data-ttu-id="461be-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="461be-135">The following is an example of the response.</span></span>
><span data-ttu-id="461be-136">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="461be-136">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="461be-137">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="461be-137">All the properties will be returned from an actual call.</span></span>
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
      "lastDeliveredDateTime": "2016-10-19T10:37:00Z",
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