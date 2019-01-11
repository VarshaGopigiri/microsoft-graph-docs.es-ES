---
title: List attachments
description: Recupera una lista de objetos attachment.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: 7799c0d5adffca64e56c10e9ea49b5d5944bc6eb
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27815886"
---
# <a name="list-attachments"></a><span data-ttu-id="035cd-103">List attachments</span><span class="sxs-lookup"><span data-stu-id="035cd-103">List attachments</span></span>

<span data-ttu-id="035cd-104">Recupera una lista de objetos attachment.</span><span class="sxs-lookup"><span data-stu-id="035cd-104">Retrieve a list of attachment objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="035cd-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="035cd-105">Permissions</span></span>
<span data-ttu-id="035cd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="035cd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="035cd-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="035cd-108">Permission type</span></span>      | <span data-ttu-id="035cd-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="035cd-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="035cd-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="035cd-110">Delegated (work or school account)</span></span> | <span data-ttu-id="035cd-111">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="035cd-111">Mail.Read</span></span>    |
|<span data-ttu-id="035cd-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="035cd-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="035cd-113">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="035cd-113">Mail.Read</span></span>    |
|<span data-ttu-id="035cd-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="035cd-114">Application</span></span> | <span data-ttu-id="035cd-115">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="035cd-115">Mail.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="035cd-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="035cd-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/messages/{id}/attachments
GET /users/{id | userPrincipalName}/messages/{id}/attachments
```
## <a name="optional-query-parameters"></a><span data-ttu-id="035cd-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="035cd-117">Optional query parameters</span></span>
<span data-ttu-id="035cd-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="035cd-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="035cd-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="035cd-119">Request headers</span></span>
| <span data-ttu-id="035cd-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="035cd-120">Name</span></span>       | <span data-ttu-id="035cd-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="035cd-121">Type</span></span> | <span data-ttu-id="035cd-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="035cd-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="035cd-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="035cd-123">Authorization</span></span>  | <span data-ttu-id="035cd-124">string</span><span class="sxs-lookup"><span data-stu-id="035cd-124">string</span></span>  | <span data-ttu-id="035cd-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="035cd-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="035cd-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="035cd-127">Request body</span></span>
<span data-ttu-id="035cd-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="035cd-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="035cd-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="035cd-129">Response</span></span>

<span data-ttu-id="035cd-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="035cd-130">If successful, this method returns a `200 OK` response code and collection of [Attachment](../resources/attachment.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="035cd-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="035cd-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="035cd-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="035cd-132">Request</span></span>
<span data-ttu-id="035cd-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="035cd-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_attachments"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages/{id}/attachments
```
##### <a name="response"></a><span data-ttu-id="035cd-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="035cd-134">Response</span></span>
<span data-ttu-id="035cd-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="035cd-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
