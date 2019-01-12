---
title: Get conversation
description: Recupera las propiedades y relaciones del objeto conversation.
author: dkershaw10
localization_priority: Normal
ms.prod: groups
ms.openlocfilehash: 08059625838d6a60489820b2369768c6a3fca071
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27931723"
---
# <a name="get-conversation"></a><span data-ttu-id="a2ba5-103">Obtener conversación</span><span class="sxs-lookup"><span data-stu-id="a2ba5-103">Get conversation</span></span>

> <span data-ttu-id="a2ba5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a2ba5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a2ba5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a2ba5-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a2ba5-106">Recupera las propiedades y relaciones del objeto conversation.</span><span class="sxs-lookup"><span data-stu-id="a2ba5-106">Retrieve the properties and relationships of conversation object.</span></span>
## <a name="permissions"></a><span data-ttu-id="a2ba5-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="a2ba5-107">Permissions</span></span>
<span data-ttu-id="a2ba5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a2ba5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a2ba5-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a2ba5-110">Permission type</span></span>      | <span data-ttu-id="a2ba5-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a2ba5-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a2ba5-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a2ba5-112">Delegated (work or school account)</span></span> | <span data-ttu-id="a2ba5-113">Group.ReadWrite.All, Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="a2ba5-113">Group.ReadWrite.All, Group.Read.All</span></span>    |
|<span data-ttu-id="a2ba5-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a2ba5-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a2ba5-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a2ba5-115">Not supported.</span></span>    |
|<span data-ttu-id="a2ba5-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a2ba5-116">Application</span></span> | <span data-ttu-id="a2ba5-117">Group.ReadWrite.All, Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="a2ba5-117">Group.ReadWrite.All, Group.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="a2ba5-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a2ba5-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/conversations/{id}

```
## <a name="optional-query-parameters"></a><span data-ttu-id="a2ba5-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a2ba5-119">Optional query parameters</span></span>
<span data-ttu-id="a2ba5-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2ba5-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="a2ba5-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a2ba5-121">Request headers</span></span>
| <span data-ttu-id="a2ba5-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2ba5-122">Header</span></span>       | <span data-ttu-id="a2ba5-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a2ba5-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="a2ba5-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="a2ba5-124">Authorization</span></span>  | <span data-ttu-id="a2ba5-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a2ba5-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="a2ba5-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a2ba5-127">Request body</span></span>
<span data-ttu-id="a2ba5-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a2ba5-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a2ba5-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2ba5-129">Response</span></span>

<span data-ttu-id="a2ba5-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [conversation](../resources/conversation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2ba5-130">If successful, this method returns a `200 OK` response code and [conversation](../resources/conversation.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="a2ba5-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a2ba5-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a2ba5-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a2ba5-132">Request</span></span>
<span data-ttu-id="a2ba5-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a2ba5-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_conversation"
}-->
```http
GET https://graph.microsoft.com/beta/groups/{id}/conversations/{id}
```
##### <a name="response"></a><span data-ttu-id="a2ba5-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2ba5-134">Response</span></span>
<span data-ttu-id="a2ba5-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a2ba5-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "lastDeliveredDateTime": "2016-10-19T10:37:00Z",
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
