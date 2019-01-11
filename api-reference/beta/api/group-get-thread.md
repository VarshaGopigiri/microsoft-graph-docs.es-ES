---
title: Obtener hilo de conversación
description: Obtiene un objeto de conversación.
author: dkershaw10
localization_priority: Normal
ms.openlocfilehash: 130c07fc00ef584b34e334f41e5eb7a6cebbdc33
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27843579"
---
# <a name="get-conversation-thread"></a><span data-ttu-id="95771-103">Obtener hilo de conversación</span><span class="sxs-lookup"><span data-stu-id="95771-103">Get conversation thread</span></span>

> <span data-ttu-id="95771-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="95771-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="95771-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="95771-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="95771-106">Obtiene un objeto de [conversación](../resources/conversationthread.md).</span><span class="sxs-lookup"><span data-stu-id="95771-106">Get a [thread](../resources/conversationthread.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="95771-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="95771-107">Permissions</span></span>
<span data-ttu-id="95771-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="95771-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="95771-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="95771-110">Permission type</span></span>      | <span data-ttu-id="95771-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="95771-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="95771-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="95771-112">Delegated (work or school account)</span></span> | <span data-ttu-id="95771-113">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="95771-113">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="95771-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="95771-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="95771-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="95771-115">Not supported.</span></span>    |
|<span data-ttu-id="95771-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="95771-116">Application</span></span> | <span data-ttu-id="95771-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="95771-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="95771-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="95771-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/threads/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="95771-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="95771-119">Optional query parameters</span></span>
<span data-ttu-id="95771-120">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="95771-120">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="95771-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="95771-121">Request headers</span></span>
| <span data-ttu-id="95771-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="95771-122">Header</span></span>       | <span data-ttu-id="95771-123">Valor</span><span class="sxs-lookup"><span data-stu-id="95771-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="95771-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="95771-124">Authorization</span></span>  | <span data-ttu-id="95771-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="95771-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="95771-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="95771-127">Request body</span></span>
<span data-ttu-id="95771-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="95771-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="95771-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="95771-129">Response</span></span>
<span data-ttu-id="95771-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto de [conversación](../resources/conversationthread.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="95771-130">If successful, this method returns a `200 OK` response code and a [thread](../resources/conversationthread.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="95771-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="95771-131">Example</span></span>
#### <a name="request"></a><span data-ttu-id="95771-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="95771-132">Request</span></span>
<span data-ttu-id="95771-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="95771-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_group_thread"
}-->
```http
GET https://graph.microsoft.com/beta/groups/02bd9fd6-8f93-4758-87c3-1fb73740a315/threads/AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgMkABAAG5c7eC4NYEynIoXsuxXB9RAAG5c7eC4NYEynIoXsuxXB9Q==
```

#### <a name="response"></a><span data-ttu-id="95771-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="95771-134">Response</span></span>
<span data-ttu-id="95771-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="95771-135">The following is an example of the response.</span></span>
><span data-ttu-id="95771-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="95771-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
