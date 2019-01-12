---
title: List attachments
description: Recupera una lista de objetos attachment asociados a una publicación.
author: dkershaw10
localization_priority: Normal
ms.prod: groups
ms.openlocfilehash: 690b4ab540982dc9b7febcd1ea302afbcf8429ab
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27916302"
---
# <a name="list-attachments"></a><span data-ttu-id="66e39-103">List attachments</span><span class="sxs-lookup"><span data-stu-id="66e39-103">List attachments</span></span>

> <span data-ttu-id="66e39-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="66e39-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="66e39-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="66e39-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="66e39-106">Recupera una lista de objetos [attachment](../resources/attachment.md) asociados a una publicación.</span><span class="sxs-lookup"><span data-stu-id="66e39-106">Retrieve a list of [attachment](../resources/attachment.md) objects attached to a post.</span></span>
## <a name="permissions"></a><span data-ttu-id="66e39-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="66e39-107">Permissions</span></span>
<span data-ttu-id="66e39-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="66e39-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="66e39-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="66e39-110">Permission type</span></span>      | <span data-ttu-id="66e39-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="66e39-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="66e39-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="66e39-112">Delegated (work or school account)</span></span> | <span data-ttu-id="66e39-113">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="66e39-113">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="66e39-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="66e39-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="66e39-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="66e39-115">Not supported.</span></span>    |
|<span data-ttu-id="66e39-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="66e39-116">Application</span></span> | <span data-ttu-id="66e39-117">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="66e39-117">Group.Read.All, Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="66e39-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="66e39-118">HTTP request</span></span>
<span data-ttu-id="66e39-119"><!-- { "blockType": "ignored" } -->Datos adjuntos de una [entrada](../resources/post.md) en un [subproceso](../resources/conversationthread.md) que pertenecen a una [conversación](../resources/conversation.md) de un grupo.</span><span class="sxs-lookup"><span data-stu-id="66e39-119"><!-- { "blockType": "ignored" } --> Attachments for a [post](../resources/post.md) in a [thread](../resources/conversationthread.md) belonging to a [conversation](../resources/conversation.md) of a group.</span></span>
```http
GET /groups/{id}/threads/{id}/posts/{id}/attachments
GET /groups/{id}/conversations/{id}/threads/{id}/posts/{id}/attachments
```
## <a name="optional-query-parameters"></a><span data-ttu-id="66e39-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="66e39-120">Optional query parameters</span></span>
<span data-ttu-id="66e39-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="66e39-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="66e39-122">En concreto, puede usar el $expanda parámetro de consulta para incluir todos los datos adjuntos de post en línea con el resto de las propiedades de entrada.</span><span class="sxs-lookup"><span data-stu-id="66e39-122">In particular, you can use the $expand query parameter to include all of the post attachments inline with the rest of the post properties.</span></span> <span data-ttu-id="66e39-123">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="66e39-123">For example:</span></span>

```
GET https://graph.microsoft.com/beta/groups/{id}/threads/{id}/posts/{id}?$expand=attachments
```
## <a name="request-headers"></a><span data-ttu-id="66e39-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="66e39-124">Request headers</span></span>
| <span data-ttu-id="66e39-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66e39-125">Header</span></span>       | <span data-ttu-id="66e39-126">Valor</span><span class="sxs-lookup"><span data-stu-id="66e39-126">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="66e39-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="66e39-127">Authorization</span></span>  | <span data-ttu-id="66e39-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="66e39-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="66e39-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="66e39-130">Request body</span></span>
<span data-ttu-id="66e39-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="66e39-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="66e39-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="66e39-132">Response</span></span>

<span data-ttu-id="66e39-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="66e39-133">If successful, this method returns a `200 OK` response code and collection of [Attachment](../resources/attachment.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="66e39-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="66e39-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="66e39-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="66e39-135">Request</span></span>
<span data-ttu-id="66e39-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="66e39-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_attachments"
}-->
```http
GET https://graph.microsoft.com/beta/groups/{id}/threads/{id}/posts/{id}/attachments
```
##### <a name="response"></a><span data-ttu-id="66e39-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="66e39-137">Response</span></span>
<span data-ttu-id="66e39-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="66e39-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.attachment",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 215

{
  "value": [
    {
      "@odata.type": "#Microsoft.OutlookServices.FileAttachment",
      "id": "id-value",
      "contentType": "contentType-value",
      "contentLocation": "contentLocation-value",
      "contentBytes": "contentBytes-value",
      "contentId": "null",
      "lastModifiedDateTime": "2016-10-19T10:37:00Z",
      "isInline": false,
      "name": "name-value",
      "size": 99
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List attachments",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
