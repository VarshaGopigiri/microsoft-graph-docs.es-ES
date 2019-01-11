---
title: Obtener hilo de conversación
description: Obtiene un objeto de conversación.
author: dkershaw10
localization_priority: Normal
ms.openlocfilehash: 72ca77aa21a40ddeba84f6977b160996f94869b7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27838048"
---
# <a name="get-conversation-thread"></a><span data-ttu-id="fe1cc-103">Obtener hilo de conversación</span><span class="sxs-lookup"><span data-stu-id="fe1cc-103">Get conversation thread</span></span>
<span data-ttu-id="fe1cc-104">Obtiene un objeto de [conversación](../resources/conversationthread.md).</span><span class="sxs-lookup"><span data-stu-id="fe1cc-104">Get a [thread](../resources/conversationthread.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="fe1cc-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="fe1cc-105">Permissions</span></span>
<span data-ttu-id="fe1cc-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fe1cc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fe1cc-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fe1cc-108">Permission type</span></span>      | <span data-ttu-id="fe1cc-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fe1cc-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fe1cc-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fe1cc-110">Delegated (work or school account)</span></span> | <span data-ttu-id="fe1cc-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fe1cc-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="fe1cc-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fe1cc-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fe1cc-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fe1cc-113">Not supported.</span></span>    |
|<span data-ttu-id="fe1cc-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fe1cc-114">Application</span></span> | <span data-ttu-id="fe1cc-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fe1cc-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="fe1cc-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fe1cc-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/threads/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="fe1cc-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="fe1cc-117">Optional query parameters</span></span>
<span data-ttu-id="fe1cc-118">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fe1cc-118">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="fe1cc-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fe1cc-119">Request headers</span></span>
| <span data-ttu-id="fe1cc-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fe1cc-120">Header</span></span>       | <span data-ttu-id="fe1cc-121">Valor</span><span class="sxs-lookup"><span data-stu-id="fe1cc-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="fe1cc-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="fe1cc-122">Authorization</span></span>  | <span data-ttu-id="fe1cc-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fe1cc-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="fe1cc-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fe1cc-125">Request body</span></span>
<span data-ttu-id="fe1cc-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="fe1cc-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="fe1cc-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fe1cc-127">Response</span></span>
<span data-ttu-id="fe1cc-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto de [conversación](../resources/conversationthread.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fe1cc-128">If successful, this method returns a `200 OK` response code and a [thread](../resources/conversationthread.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fe1cc-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fe1cc-129">Example</span></span>
#### <a name="request"></a><span data-ttu-id="fe1cc-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fe1cc-130">Request</span></span>
<span data-ttu-id="fe1cc-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fe1cc-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["02bd9fd6-8f93-4758-87c3-1fb73740a315", "AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgMkABAAG5c7eC4NYEynIoXsuxXB9RAAG5c7eC4NYEynIoXsuxXB9Q=="],
  "name": "get_group_thread"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/02bd9fd6-8f93-4758-87c3-1fb73740a315/threads/AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgMkABAAG5c7eC4NYEynIoXsuxXB9RAAG5c7eC4NYEynIoXsuxXB9Q==
```

#### <a name="response"></a><span data-ttu-id="fe1cc-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fe1cc-132">Response</span></span>
<span data-ttu-id="fe1cc-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fe1cc-133">The following is an example of the response.</span></span>
><span data-ttu-id="fe1cc-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fe1cc-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversationThread"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 655

{
    "id": "AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgMkABAAG5c7eC4NYEynIoXsuxXB9RAAG5c7eC4NYEynIoXsuxXB9Q==",
    "topic": "New Training Plans",
    "hasAttachments": false,
    "lastDeliveredDateTime": "2017-07-31T18:59:05Z",
    "uniqueSenders": [
        "HR Taskforce"
    ],
    "preview": "Meeting to plan new trainings.\r\n\r\n\r\n\r\nJoin Microsoft Teams Online Meeting<https://teams.microsoft.com/l/meetup-join/19%3a900876baa3134907b0dcb41a0d220e31%40thread.skype/1501527539926?tenantId=dcd219dd-bc68-4b9b-bf0b-4a33a796be35>",
    "isLocked": false
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get conversation thread",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
