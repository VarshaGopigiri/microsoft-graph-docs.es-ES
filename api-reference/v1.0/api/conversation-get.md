---
title: Get conversation
description: Recupera las propiedades y relaciones del objeto conversation.
author: dkershaw10
localization_priority: Normal
ms.prod: groups
ms.openlocfilehash: 174d5a5b5309348de5ebf01d38445d032d9e31ff
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27980394"
---
# <a name="get-conversation"></a><span data-ttu-id="09642-103">Get conversation</span><span class="sxs-lookup"><span data-stu-id="09642-103">Get conversation</span></span>

<span data-ttu-id="09642-104">Recupera las propiedades y relaciones del objeto conversation.</span><span class="sxs-lookup"><span data-stu-id="09642-104">Retrieve the properties and relationships of conversation object.</span></span>
## <a name="permissions"></a><span data-ttu-id="09642-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="09642-105">Permissions</span></span>
<span data-ttu-id="09642-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="09642-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="09642-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="09642-108">Permission type</span></span>      | <span data-ttu-id="09642-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="09642-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="09642-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="09642-110">Delegated (work or school account)</span></span> | <span data-ttu-id="09642-111">Group.ReadWrite.All, Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="09642-111">Group.ReadWrite.All, Group.Read.All</span></span>    |
|<span data-ttu-id="09642-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="09642-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="09642-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="09642-113">Not supported.</span></span>    |
|<span data-ttu-id="09642-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="09642-114">Application</span></span> | <span data-ttu-id="09642-115">Group.ReadWrite.All, Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="09642-115">Group.ReadWrite.All, Group.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="09642-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="09642-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/conversations/{id}

```
## <a name="optional-query-parameters"></a><span data-ttu-id="09642-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="09642-117">Optional query parameters</span></span>
<span data-ttu-id="09642-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="09642-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="09642-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="09642-119">Request headers</span></span>
| <span data-ttu-id="09642-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09642-120">Header</span></span>       | <span data-ttu-id="09642-121">Valor</span><span class="sxs-lookup"><span data-stu-id="09642-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="09642-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="09642-122">Authorization</span></span>  | <span data-ttu-id="09642-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="09642-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="09642-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="09642-125">Request body</span></span>
<span data-ttu-id="09642-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="09642-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="09642-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="09642-127">Response</span></span>

<span data-ttu-id="09642-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [conversation](../resources/conversation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="09642-128">If successful, this method returns a `200 OK` response code and [conversation](../resources/conversation.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="09642-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="09642-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="09642-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="09642-130">Request</span></span>
<span data-ttu-id="09642-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="09642-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_conversation"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/conversations/{id}
```
##### <a name="response"></a><span data-ttu-id="09642-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="09642-132">Response</span></span>
<span data-ttu-id="09642-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="09642-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversation"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 201

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
