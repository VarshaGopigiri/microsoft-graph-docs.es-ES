---
title: List threads
description: Obtenga todos los hilos de un grupo.
author: dkershaw10
localization_priority: Normal
ms.openlocfilehash: 4317ddb197832993bec589bf0c0d402317d0d862
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27866153"
---
# <a name="list-threads"></a><span data-ttu-id="13b67-103">List threads</span><span class="sxs-lookup"><span data-stu-id="13b67-103">List threads</span></span>
<span data-ttu-id="13b67-104">Obtenga todos los hilos de un grupo.</span><span class="sxs-lookup"><span data-stu-id="13b67-104">Get all the threads of a group.</span></span>

><span data-ttu-id="13b67-105">Nota: También puede [obtener todos los hilos de una conversación](conversation-list-threads.md).</span><span class="sxs-lookup"><span data-stu-id="13b67-105">Note: You can also [get all the threads of a conversation](conversation-list-threads.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="13b67-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="13b67-106">Permissions</span></span>
<span data-ttu-id="13b67-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="13b67-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="13b67-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="13b67-109">Permission type</span></span>      | <span data-ttu-id="13b67-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="13b67-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="13b67-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="13b67-111">Delegated (work or school account)</span></span> | <span data-ttu-id="13b67-112">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="13b67-112">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="13b67-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="13b67-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="13b67-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="13b67-114">Not supported.</span></span>    |
|<span data-ttu-id="13b67-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="13b67-115">Application</span></span> | <span data-ttu-id="13b67-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="13b67-116">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="13b67-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="13b67-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/threads
```

## <a name="optional-query-parameters"></a><span data-ttu-id="13b67-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="13b67-118">Optional query parameters</span></span>
<span data-ttu-id="13b67-119">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="13b67-119">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="13b67-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="13b67-120">Request headers</span></span>
| <span data-ttu-id="13b67-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13b67-121">Header</span></span>       | <span data-ttu-id="13b67-122">Valor</span><span class="sxs-lookup"><span data-stu-id="13b67-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="13b67-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="13b67-123">Authorization</span></span>  | <span data-ttu-id="13b67-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="13b67-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="13b67-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="13b67-126">Request body</span></span>
<span data-ttu-id="13b67-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="13b67-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="13b67-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="13b67-128">Response</span></span>
<span data-ttu-id="13b67-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [ConversationThread](../resources/conversationthread.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="13b67-129">If successful, this method returns a `200 OK` response code and collection of [ConversationThread](../resources/conversationthread.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="13b67-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="13b67-130">Example</span></span>
#### <a name="request"></a><span data-ttu-id="13b67-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="13b67-131">Request</span></span>
<span data-ttu-id="13b67-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="13b67-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_threads"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/threads
```

#### <a name="response"></a><span data-ttu-id="13b67-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="13b67-133">Response</span></span>
<span data-ttu-id="13b67-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="13b67-134">The following is an example of the response.</span></span>
><span data-ttu-id="13b67-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="13b67-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversationThread",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 536

{
  "value": [
    {
      "toRecipients": [
        {
          "emailAddress": {
            "name": "name-value",
            "address": "address-value"
          }
        }
      ],
      "topic": "topic-value",
      "hasAttachments": true,
      "lastDeliveredDateTime": "datetime-value",
      "uniqueSenders": [
        "uniqueSenders-value"
      ],
      "ccRecipients": [
        {
          "emailAddress": {
            "name": "name-value",
            "address": "address-value"
          }
        }
      ]
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List threads",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
