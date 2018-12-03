---
title: List attachments
description: Recupera una lista de objetos attachment.
ms.openlocfilehash: c9540db402a39cf8bf8f35318d06e7e699e9c7f6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032000"
---
# <a name="list-attachments"></a><span data-ttu-id="33b41-103">List attachments</span><span class="sxs-lookup"><span data-stu-id="33b41-103">List attachments</span></span>

<span data-ttu-id="33b41-104">Recupera una lista de objetos attachment.</span><span class="sxs-lookup"><span data-stu-id="33b41-104">Retrieve a list of attachment objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="33b41-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="33b41-105">Permissions</span></span>
<span data-ttu-id="33b41-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="33b41-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="33b41-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="33b41-108">Permission type</span></span>      | <span data-ttu-id="33b41-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="33b41-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="33b41-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="33b41-110">Delegated (work or school account)</span></span> | <span data-ttu-id="33b41-111">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="33b41-111">Mail.Read</span></span>    |
|<span data-ttu-id="33b41-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="33b41-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="33b41-113">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="33b41-113">Mail.Read</span></span>    |
|<span data-ttu-id="33b41-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="33b41-114">Application</span></span> | <span data-ttu-id="33b41-115">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="33b41-115">Mail.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="33b41-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="33b41-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/messages/{id}/attachments
GET /users/{id | userPrincipalName}/messages/{id}/attachments
```
## <a name="optional-query-parameters"></a><span data-ttu-id="33b41-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="33b41-117">Optional query parameters</span></span>
<span data-ttu-id="33b41-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="33b41-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="33b41-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="33b41-119">Request headers</span></span>
| <span data-ttu-id="33b41-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="33b41-120">Name</span></span>       | <span data-ttu-id="33b41-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="33b41-121">Type</span></span> | <span data-ttu-id="33b41-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="33b41-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="33b41-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="33b41-123">Authorization</span></span>  | <span data-ttu-id="33b41-124">string</span><span class="sxs-lookup"><span data-stu-id="33b41-124">string</span></span>  | <span data-ttu-id="33b41-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="33b41-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="33b41-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="33b41-127">Request body</span></span>
<span data-ttu-id="33b41-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="33b41-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="33b41-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="33b41-129">Response</span></span>

<span data-ttu-id="33b41-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="33b41-130">If successful, this method returns a `200 OK` response code and collection of [Attachment](../resources/attachment.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="33b41-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="33b41-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="33b41-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="33b41-132">Request</span></span>
<span data-ttu-id="33b41-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="33b41-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_attachments"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages/{id}/attachments
```
##### <a name="response"></a><span data-ttu-id="33b41-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="33b41-134">Response</span></span>
<span data-ttu-id="33b41-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="33b41-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
      "contentType": "contentType-value",
      "contentLocation": "contentLocation-value",
      "contentBytes": "base64-contentBytes-value",
      "contentId": "null",
      "lastModifiedDateTime": "datetime-value",
      "id": "id-value",
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
