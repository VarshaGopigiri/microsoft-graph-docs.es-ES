---
title: List attachments
description: Recupera una lista de objetos attachment asociados a una publicación.
ms.openlocfilehash: b1a7ea8778b2ff25ad8e3159697d12aafe180506
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032567"
---
# <a name="list-attachments"></a><span data-ttu-id="39255-103">List attachments</span><span class="sxs-lookup"><span data-stu-id="39255-103">List attachments</span></span>

<span data-ttu-id="39255-104">Recupera una lista de objetos [attachment](../resources/attachment.md) asociados a una publicación.</span><span class="sxs-lookup"><span data-stu-id="39255-104">Retrieve a list of [attachment](../resources/attachment.md) objects attached to a post.</span></span>
## <a name="permissions"></a><span data-ttu-id="39255-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="39255-105">Permissions</span></span>
<span data-ttu-id="39255-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="39255-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="39255-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="39255-108">Permission type</span></span>      | <span data-ttu-id="39255-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="39255-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="39255-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="39255-110">Delegated (work or school account)</span></span> | <span data-ttu-id="39255-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="39255-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="39255-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="39255-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="39255-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="39255-113">Not supported.</span></span>    |
|<span data-ttu-id="39255-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="39255-114">Application</span></span> | <span data-ttu-id="39255-115">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="39255-115">Group.Read.All, Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="39255-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="39255-116">HTTP request</span></span>
<span data-ttu-id="39255-117"><!-- { "blockType": "ignored" } -->Datos adjuntos de una [entrada](../resources/post.md) en un [subproceso](../resources/conversationthread.md) que pertenecen a una [conversación](../resources/conversation.md) de un grupo.</span><span class="sxs-lookup"><span data-stu-id="39255-117"><!-- { "blockType": "ignored" } --> Attachments for a [post](../resources/post.md) in a [thread](../resources/conversationthread.md) belonging to a [conversation](../resources/conversation.md) of a group.</span></span>
```http
GET /groups/{id}/threads/{id}/posts/{id}/attachments
GET /groups/{id}/conversations/{id}/threads/{id}/posts/{id}/attachments
```
## <a name="optional-query-parameters"></a><span data-ttu-id="39255-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="39255-118">Optional query parameters</span></span>
<span data-ttu-id="39255-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="39255-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="39255-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="39255-120">Request headers</span></span>
| <span data-ttu-id="39255-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39255-121">Header</span></span>       | <span data-ttu-id="39255-122">Valor</span><span class="sxs-lookup"><span data-stu-id="39255-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="39255-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="39255-123">Authorization</span></span>  | <span data-ttu-id="39255-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="39255-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="39255-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="39255-126">Request body</span></span>
<span data-ttu-id="39255-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="39255-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="39255-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="39255-128">Response</span></span>

<span data-ttu-id="39255-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="39255-129">If successful, this method returns a `200 OK` response code and collection of [Attachment](../resources/attachment.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="39255-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="39255-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="39255-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="39255-131">Request</span></span>
<span data-ttu-id="39255-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="39255-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_attachments"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/threads/{id}/posts/{id}/attachments
```
##### <a name="response"></a><span data-ttu-id="39255-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="39255-133">Response</span></span>
<span data-ttu-id="39255-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="39255-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "collection(microsoft.graph.attachment)",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 215

{
  "value": [
    {
      "@odata.type": "microsoft.graph.fileAttachment",
      "id": "id-value",
      "contentType": "contentType-value",
      "contentLocation": "contentLocation-value",
      "contentBytes": "base64-contentBytes-value",
      "contentId": "null",
      "lastModifiedDateTime": "datetime-value",
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