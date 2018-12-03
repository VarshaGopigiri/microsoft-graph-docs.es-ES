---
title: List threads
description: Obtiene todos los hilos de una conversación de grupo.
ms.openlocfilehash: 85d694261b71e0aa6eb68d9c2e2db00794c20f4c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087793"
---
# <a name="list-threads"></a><span data-ttu-id="a836a-103">List threads</span><span class="sxs-lookup"><span data-stu-id="a836a-103">List threads</span></span>

> <span data-ttu-id="a836a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a836a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a836a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a836a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a836a-106">Obtiene todos los hilos de una conversación de grupo.</span><span class="sxs-lookup"><span data-stu-id="a836a-106">Get all the threads in a group conversation.</span></span>
<span data-ttu-id="a836a-107">Nota: También puede [obtener todos los hilos de un grupo](group-list-threads.md).</span><span class="sxs-lookup"><span data-stu-id="a836a-107">Note: You can also [get all the threads of a group](group-list-threads.md).</span></span> 

## <a name="permissions"></a><span data-ttu-id="a836a-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="a836a-108">Permissions</span></span>
<span data-ttu-id="a836a-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a836a-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a836a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a836a-111">Permission type</span></span>      | <span data-ttu-id="a836a-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a836a-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a836a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a836a-113">Delegated (work or school account)</span></span> | <span data-ttu-id="a836a-114">Group.ReadWrite.All, Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="a836a-114">Group.ReadWrite.All, Group.Read.All</span></span>    |
|<span data-ttu-id="a836a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a836a-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a836a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a836a-116">Not supported.</span></span>    |
|<span data-ttu-id="a836a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a836a-117">Application</span></span> | <span data-ttu-id="a836a-118">Group.ReadWrite.All, Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="a836a-118">Group.ReadWrite.All, Group.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="a836a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a836a-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/conversations/{id}/threads
```
## <a name="optional-query-parameters"></a><span data-ttu-id="a836a-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a836a-120">Optional query parameters</span></span>
<span data-ttu-id="a836a-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a836a-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="a836a-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a836a-122">Request headers</span></span>
| <span data-ttu-id="a836a-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a836a-123">Header</span></span>       | <span data-ttu-id="a836a-124">Valor</span><span class="sxs-lookup"><span data-stu-id="a836a-124">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="a836a-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="a836a-125">Authorization</span></span>  | <span data-ttu-id="a836a-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a836a-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="a836a-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a836a-128">Request body</span></span>
<span data-ttu-id="a836a-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a836a-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a836a-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a836a-130">Response</span></span>

<span data-ttu-id="a836a-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [conversationThread](../resources/conversationthread.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a836a-131">If successful, this method returns a `200 OK` response code and collection of [conversationThread](../resources/conversationthread.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="a836a-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a836a-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a836a-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a836a-133">Request</span></span>
<span data-ttu-id="a836a-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a836a-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_threads"
}-->
```http
GET https://graph.microsoft.com/beta/groups/{id}/conversations/{id}/threads
```
##### <a name="response"></a><span data-ttu-id="a836a-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a836a-135">Response</span></span>
<span data-ttu-id="a836a-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a836a-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "List threads",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->