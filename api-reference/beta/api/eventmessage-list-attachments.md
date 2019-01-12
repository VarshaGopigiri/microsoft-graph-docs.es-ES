---
title: List attachments
description: Recupera una lista de objetos attachment.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 5b54e26acbb08b7960693b3e5a1e531fc4c20708
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27951351"
---
# <a name="list-attachments"></a><span data-ttu-id="21c20-103">List attachments</span><span class="sxs-lookup"><span data-stu-id="21c20-103">List attachments</span></span>

> <span data-ttu-id="21c20-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="21c20-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="21c20-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="21c20-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="21c20-106">Recupera una lista de objetos attachment.</span><span class="sxs-lookup"><span data-stu-id="21c20-106">Retrieve a list of attachment objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="21c20-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="21c20-107">Permissions</span></span>
<span data-ttu-id="21c20-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="21c20-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="21c20-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="21c20-110">Permission type</span></span>      | <span data-ttu-id="21c20-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="21c20-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="21c20-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="21c20-112">Delegated (work or school account)</span></span> | <span data-ttu-id="21c20-113">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="21c20-113">Mail.Read</span></span>    |
|<span data-ttu-id="21c20-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="21c20-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="21c20-115">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="21c20-115">Mail.Read</span></span>    |
|<span data-ttu-id="21c20-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="21c20-116">Application</span></span> | <span data-ttu-id="21c20-117">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="21c20-117">Mail.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="21c20-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="21c20-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/messages/{id}/attachments
GET /users/{id | userPrincipalName}/messages/{id}/attachments
```
## <a name="optional-query-parameters"></a><span data-ttu-id="21c20-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="21c20-119">Optional query parameters</span></span>
<span data-ttu-id="21c20-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="21c20-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="21c20-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="21c20-121">Request headers</span></span>
| <span data-ttu-id="21c20-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="21c20-122">Name</span></span>       | <span data-ttu-id="21c20-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="21c20-123">Type</span></span> | <span data-ttu-id="21c20-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="21c20-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="21c20-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="21c20-125">Authorization</span></span>  | <span data-ttu-id="21c20-126">string</span><span class="sxs-lookup"><span data-stu-id="21c20-126">string</span></span>  | <span data-ttu-id="21c20-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="21c20-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="21c20-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="21c20-129">Request body</span></span>
<span data-ttu-id="21c20-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="21c20-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="21c20-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="21c20-131">Response</span></span>

<span data-ttu-id="21c20-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="21c20-132">If successful, this method returns a `200 OK` response code and collection of [Attachment](../resources/attachment.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="21c20-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="21c20-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="21c20-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="21c20-134">Request</span></span>
<span data-ttu-id="21c20-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="21c20-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_attachments"
}-->
```http
GET https://graph.microsoft.com/beta/me/messages/{id}/attachments
```
##### <a name="response"></a><span data-ttu-id="21c20-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="21c20-136">Response</span></span>
<span data-ttu-id="21c20-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="21c20-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
      "contentType": "contentType-value",
      "contentLocation": "contentLocation-value",
      "contentBytes": "contentBytes-value",
      "contentId": "null",
      "lastModifiedDateTime": "2016-10-19T10:37:00Z",
      "id": "id-value",
      "isInline": false,
      "isContactPhoto": false,
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
