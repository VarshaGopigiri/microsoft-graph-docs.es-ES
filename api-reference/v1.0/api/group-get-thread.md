---
title: Obtener hilo de conversación
description: Obtiene un objeto de conversación.
ms.openlocfilehash: ba7bc4e008e714f8a5b10681f3f21665b92c701b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030726"
---
# <a name="get-conversation-thread"></a><span data-ttu-id="5e780-103">Obtener hilo de conversación</span><span class="sxs-lookup"><span data-stu-id="5e780-103">Get conversation thread</span></span>
<span data-ttu-id="5e780-104">Obtiene un objeto de [conversación](../resources/conversationthread.md).</span><span class="sxs-lookup"><span data-stu-id="5e780-104">Get a [thread](../resources/conversationthread.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="5e780-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="5e780-105">Permissions</span></span>
<span data-ttu-id="5e780-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5e780-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5e780-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5e780-108">Permission type</span></span>      | <span data-ttu-id="5e780-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5e780-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5e780-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5e780-110">Delegated (work or school account)</span></span> | <span data-ttu-id="5e780-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5e780-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="5e780-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5e780-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5e780-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5e780-113">Not supported.</span></span>    |
|<span data-ttu-id="5e780-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5e780-114">Application</span></span> | <span data-ttu-id="5e780-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5e780-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="5e780-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5e780-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/threads/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="5e780-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="5e780-117">Optional query parameters</span></span>
<span data-ttu-id="5e780-118">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5e780-118">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="5e780-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5e780-119">Request headers</span></span>
| <span data-ttu-id="5e780-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5e780-120">Header</span></span>       | <span data-ttu-id="5e780-121">Valor</span><span class="sxs-lookup"><span data-stu-id="5e780-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="5e780-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="5e780-122">Authorization</span></span>  | <span data-ttu-id="5e780-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5e780-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="5e780-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5e780-125">Request body</span></span>
<span data-ttu-id="5e780-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5e780-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5e780-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5e780-127">Response</span></span>
<span data-ttu-id="5e780-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto de [conversación](../resources/conversationthread.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5e780-128">If successful, this method returns a `200 OK` response code and a [thread](../resources/conversationthread.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5e780-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5e780-129">Example</span></span>
#### <a name="request"></a><span data-ttu-id="5e780-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5e780-130">Request</span></span>
<span data-ttu-id="5e780-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5e780-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["02bd9fd6-8f93-4758-87c3-1fb73740a315", "AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgMkABAAG5c7eC4NYEynIoXsuxXB9RAAG5c7eC4NYEynIoXsuxXB9Q=="],
  "name": "get_group_thread"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/02bd9fd6-8f93-4758-87c3-1fb73740a315/threads/AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgMkABAAG5c7eC4NYEynIoXsuxXB9RAAG5c7eC4NYEynIoXsuxXB9Q==
```

#### <a name="response"></a><span data-ttu-id="5e780-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5e780-132">Response</span></span>
<span data-ttu-id="5e780-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5e780-133">The following is an example of the response.</span></span>
><span data-ttu-id="5e780-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5e780-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
