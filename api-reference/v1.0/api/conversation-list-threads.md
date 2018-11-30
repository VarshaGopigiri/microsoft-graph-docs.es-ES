---
title: List threads
description: Obtiene todos los hilos de una conversación de grupo.
ms.openlocfilehash: 9d3a981b71b369e745acae0b362e5711a18f0272
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031105"
---
# <a name="list-threads"></a><span data-ttu-id="0c6bf-103">List threads</span><span class="sxs-lookup"><span data-stu-id="0c6bf-103">List threads</span></span>

<span data-ttu-id="0c6bf-104">Obtiene todos los hilos de una conversación de grupo.</span><span class="sxs-lookup"><span data-stu-id="0c6bf-104">Get all the threads in a group conversation.</span></span>

<span data-ttu-id="0c6bf-105">Nota: También puede [obtener todos los hilos de un grupo](group-list-threads.md).</span><span class="sxs-lookup"><span data-stu-id="0c6bf-105">Note: You can also [get all the threads of a group](group-list-threads.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="0c6bf-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="0c6bf-106">Permissions</span></span>
<span data-ttu-id="0c6bf-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0c6bf-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0c6bf-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0c6bf-109">Permission type</span></span>      | <span data-ttu-id="0c6bf-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0c6bf-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0c6bf-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0c6bf-111">Delegated (work or school account)</span></span> | <span data-ttu-id="0c6bf-112">Group.ReadWrite.All, Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="0c6bf-112">Group.ReadWrite.All, Group.Read.All</span></span>    |
|<span data-ttu-id="0c6bf-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0c6bf-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0c6bf-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0c6bf-114">Not supported.</span></span>    |
|<span data-ttu-id="0c6bf-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0c6bf-115">Application</span></span> | <span data-ttu-id="0c6bf-116">Group.ReadWrite.All, Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="0c6bf-116">Group.ReadWrite.All, Group.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="0c6bf-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0c6bf-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/conversations/{id}/threads
```
## <a name="optional-query-parameters"></a><span data-ttu-id="0c6bf-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="0c6bf-118">Optional query parameters</span></span>
<span data-ttu-id="0c6bf-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0c6bf-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="0c6bf-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0c6bf-120">Request headers</span></span>
| <span data-ttu-id="0c6bf-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0c6bf-121">Header</span></span>       | <span data-ttu-id="0c6bf-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0c6bf-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="0c6bf-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="0c6bf-123">Authorization</span></span>  | <span data-ttu-id="0c6bf-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0c6bf-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="0c6bf-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0c6bf-126">Request body</span></span>
<span data-ttu-id="0c6bf-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0c6bf-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0c6bf-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0c6bf-128">Response</span></span>

<span data-ttu-id="0c6bf-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [conversationThread](../resources/conversationthread.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0c6bf-129">If successful, this method returns a `200 OK` response code and collection of [conversationThread](../resources/conversationthread.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="0c6bf-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0c6bf-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="0c6bf-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0c6bf-131">Request</span></span>
<span data-ttu-id="0c6bf-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0c6bf-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_threads"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/conversations/{id}/threads
```
##### <a name="response"></a><span data-ttu-id="0c6bf-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0c6bf-133">Response</span></span>
<span data-ttu-id="0c6bf-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0c6bf-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
