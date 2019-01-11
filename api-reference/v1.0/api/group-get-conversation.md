---
title: Obtener conversación
description: Obtiene un objeto de conversación.
author: dkershaw10
localization_priority: Normal
ms.openlocfilehash: 64355f38d5cbab8d8a146125512338f98d830b62
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27863248"
---
# <a name="get-conversation"></a><span data-ttu-id="ed721-103">Obtener conversación</span><span class="sxs-lookup"><span data-stu-id="ed721-103">Get conversation</span></span>
<span data-ttu-id="ed721-104">Obtiene un objeto de [conversación](../resources/conversation.md).</span><span class="sxs-lookup"><span data-stu-id="ed721-104">Get a [conversation](../resources/conversation.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="ed721-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="ed721-105">Permissions</span></span>
<span data-ttu-id="ed721-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ed721-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ed721-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ed721-108">Permission type</span></span>      | <span data-ttu-id="ed721-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ed721-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ed721-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ed721-110">Delegated (work or school account)</span></span> | <span data-ttu-id="ed721-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed721-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="ed721-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ed721-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ed721-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ed721-113">Not supported.</span></span>    |
|<span data-ttu-id="ed721-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ed721-114">Application</span></span> | <span data-ttu-id="ed721-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ed721-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="ed721-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ed721-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/conversations/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="ed721-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ed721-117">Optional query parameters</span></span>
<span data-ttu-id="ed721-118">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ed721-118">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="ed721-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ed721-119">Request headers</span></span>
| <span data-ttu-id="ed721-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed721-120">Header</span></span>       | <span data-ttu-id="ed721-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ed721-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ed721-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="ed721-122">Authorization</span></span>  | <span data-ttu-id="ed721-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ed721-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ed721-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ed721-125">Request body</span></span>
<span data-ttu-id="ed721-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ed721-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ed721-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ed721-127">Response</span></span>
<span data-ttu-id="ed721-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto de [conversación](../resources/conversation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ed721-128">If successful, this method returns a `200 OK` response code and a [conversation](../resources/conversation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ed721-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ed721-129">Example</span></span>
#### <a name="request"></a><span data-ttu-id="ed721-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ed721-130">Request</span></span>
<span data-ttu-id="ed721-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ed721-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["02bd9fd6-8f93-4758-87c3-1fb73740a315", "AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgAQABuXO3guDWBMpyKF7LsVwfU="],
  "name": "get_group_conversation"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/02bd9fd6-8f93-4758-87c3-1fb73740a315/conversations/AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgAQABuXO3guDWBMpyKF7LsVwfU=
```

#### <a name="response"></a><span data-ttu-id="ed721-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ed721-132">Response</span></span>
<span data-ttu-id="ed721-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ed721-133">The following is an example of the response.</span></span>
><span data-ttu-id="ed721-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ed721-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversation"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 644

{
    "id": "AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgAQABuXO3guDWBMpyKF7LsVwfU=",
    "topic": "New Training Plans",
    "hasAttachments": false,
    "lastDeliveredDateTime": "2017-07-31T18:59:05Z",
    "uniqueSenders": [
        "HR Taskforce"
    ],
    "preview": "Meeting to plan new trainings.\r\n\r\n\r\n\r\nJoin Microsoft Teams Online Meeting<https://teams.microsoft.com/l/meetup-join/19%3a900876baa3134907b0dcb41a0d220e31%40thread.skype/1501527539926?tenantId=dcd219dd-bc68-4b9b-bf0b-4a33a796be35>"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get conversation",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
