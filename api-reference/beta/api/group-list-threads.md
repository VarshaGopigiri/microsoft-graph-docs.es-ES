---
title: List threads
description: Obtenga todos los hilos de un grupo.
author: dkershaw10
localization_priority: Normal
ms.openlocfilehash: a15c9def749717f7134bc0a34cac868e0bc10897
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27870472"
---
# <a name="list-threads"></a><span data-ttu-id="5da6f-103">List threads</span><span class="sxs-lookup"><span data-stu-id="5da6f-103">List threads</span></span>

> <span data-ttu-id="5da6f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5da6f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5da6f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5da6f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5da6f-106">Obtenga todos los hilos de un grupo.</span><span class="sxs-lookup"><span data-stu-id="5da6f-106">Get all the threads of a group.</span></span>

<span data-ttu-id="5da6f-107">Nota: También puede [obtener todos los hilos de una conversación](conversation-list-threads.md).</span><span class="sxs-lookup"><span data-stu-id="5da6f-107">Note: You can also [get all the threads of a conversation](conversation-list-threads.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="5da6f-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="5da6f-108">Permissions</span></span>
<span data-ttu-id="5da6f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5da6f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5da6f-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5da6f-111">Permission type</span></span>      | <span data-ttu-id="5da6f-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5da6f-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5da6f-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5da6f-113">Delegated (work or school account)</span></span> | <span data-ttu-id="5da6f-114">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5da6f-114">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="5da6f-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5da6f-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5da6f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5da6f-116">Not supported.</span></span>    |
|<span data-ttu-id="5da6f-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5da6f-117">Application</span></span> | <span data-ttu-id="5da6f-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5da6f-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="5da6f-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5da6f-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/threads
```

## <a name="optional-query-parameters"></a><span data-ttu-id="5da6f-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="5da6f-120">Optional query parameters</span></span>
<span data-ttu-id="5da6f-121">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5da6f-121">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="5da6f-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5da6f-122">Request headers</span></span>
| <span data-ttu-id="5da6f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5da6f-123">Header</span></span>       | <span data-ttu-id="5da6f-124">Valor</span><span class="sxs-lookup"><span data-stu-id="5da6f-124">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="5da6f-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="5da6f-125">Authorization</span></span>  | <span data-ttu-id="5da6f-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5da6f-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="5da6f-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5da6f-128">Request body</span></span>
<span data-ttu-id="5da6f-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5da6f-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5da6f-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5da6f-130">Response</span></span>
<span data-ttu-id="5da6f-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [conversationThread](../resources/conversationthread.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5da6f-131">If successful, this method returns a `200 OK` response code and collection of [conversationThread](../resources/conversationthread.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5da6f-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5da6f-132">Example</span></span>
#### <a name="request"></a><span data-ttu-id="5da6f-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5da6f-133">Request</span></span>
<span data-ttu-id="5da6f-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5da6f-134">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_group_threads"
}-->
```http
GET https://graph.microsoft.com/beta/groups/{id}/threads
```

#### <a name="response"></a><span data-ttu-id="5da6f-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5da6f-135">Response</span></span>
<span data-ttu-id="5da6f-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5da6f-136">The following is an example of the response.</span></span>
><span data-ttu-id="5da6f-137">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="5da6f-137">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="5da6f-138">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5da6f-138">All the properties will be returned from an actual call.</span></span>
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
      "lastDeliveredDateTime": "2016-10-19T10:37:00Z",
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
  "description": "List group threads",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
