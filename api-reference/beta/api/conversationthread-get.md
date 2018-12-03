---
title: Get conversationThread
description: 'Obtenga un hilo específico que pertenece a un grupo. Puede especificar la conversación primario y el subproceso, o bien, '
ms.openlocfilehash: b9a99be2e44b7639fe9a44b475bdf0161efa303c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084286"
---
# <a name="get-conversationthread"></a><span data-ttu-id="76f9e-104">Get conversationThread</span><span class="sxs-lookup"><span data-stu-id="76f9e-104">Get conversationThread</span></span>

> <span data-ttu-id="76f9e-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="76f9e-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="76f9e-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="76f9e-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="76f9e-p103">Obtiene un hilo específico que pertenece a un grupo. Puede especificar la conversación primaria y el hilo, o bien, especificar el hilo sin hacer referencia a la conversación primaria.</span><span class="sxs-lookup"><span data-stu-id="76f9e-p103">Get a specific thread that belongs to a group. You can specify both the parent conversation and the thread, or, you can specify the thread without referencing the parent conversation.</span></span> 
## <a name="permissions"></a><span data-ttu-id="76f9e-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="76f9e-109">Permissions</span></span>
<span data-ttu-id="76f9e-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="76f9e-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="76f9e-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="76f9e-112">Permission type</span></span>      | <span data-ttu-id="76f9e-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="76f9e-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="76f9e-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="76f9e-114">Delegated (work or school account)</span></span> | <span data-ttu-id="76f9e-115">Group.ReadWrite.All, Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="76f9e-115">Group.ReadWrite.All, Group.Read.All</span></span>    |
|<span data-ttu-id="76f9e-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="76f9e-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="76f9e-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="76f9e-117">Not supported.</span></span>    |
|<span data-ttu-id="76f9e-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="76f9e-118">Application</span></span> | <span data-ttu-id="76f9e-119">Group.ReadWrite.All, Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="76f9e-119">Group.ReadWrite.All, Group.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="76f9e-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="76f9e-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/threads/{id}
GET /groups/{id}/conversations/{id}/threads/{id}

```
## <a name="optional-query-parameters"></a><span data-ttu-id="76f9e-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="76f9e-121">Optional query parameters</span></span>
<span data-ttu-id="76f9e-122">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="76f9e-122">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="76f9e-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="76f9e-123">Request headers</span></span>
| <span data-ttu-id="76f9e-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="76f9e-124">Header</span></span>       | <span data-ttu-id="76f9e-125">Valor</span><span class="sxs-lookup"><span data-stu-id="76f9e-125">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="76f9e-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="76f9e-126">Authorization</span></span>  | <span data-ttu-id="76f9e-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="76f9e-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="76f9e-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="76f9e-129">Request body</span></span>
<span data-ttu-id="76f9e-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="76f9e-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="76f9e-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="76f9e-131">Response</span></span>

<span data-ttu-id="76f9e-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [conversationThread](../resources/conversationthread.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="76f9e-132">If successful, this method returns a `200 OK` response code and [conversationThread](../resources/conversationthread.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="76f9e-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="76f9e-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="76f9e-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="76f9e-134">Request</span></span>
<span data-ttu-id="76f9e-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="76f9e-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_conversationthread"
}-->
```http
GET https://graph.microsoft.com/beta/groups/{id}/threads/{id}
```
##### <a name="response"></a><span data-ttu-id="76f9e-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="76f9e-136">Response</span></span>
<span data-ttu-id="76f9e-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="76f9e-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversationThread"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 419

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
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get conversationThread",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->