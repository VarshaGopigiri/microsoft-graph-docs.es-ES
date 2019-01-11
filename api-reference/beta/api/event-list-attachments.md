---
title: List attachments
description: Recupera una lista de objetos attachment asociados a un evento.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: d05bb4194a60346b97e6be368d6790fdebf8e12b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27854708"
---
# <a name="list-attachments"></a><span data-ttu-id="53a7e-103">List attachments</span><span class="sxs-lookup"><span data-stu-id="53a7e-103">List attachments</span></span>

> <span data-ttu-id="53a7e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="53a7e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="53a7e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="53a7e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="53a7e-106">Recupera una lista de objetos [attachment](../resources/attachment.md) asociados a un evento.</span><span class="sxs-lookup"><span data-stu-id="53a7e-106">Retrieve a list of [attachment](../resources/attachment.md) objects attached to an event.</span></span>

## <a name="permissions"></a><span data-ttu-id="53a7e-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="53a7e-107">Permissions</span></span>

<span data-ttu-id="53a7e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="53a7e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="53a7e-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="53a7e-110">Permission type</span></span>      | <span data-ttu-id="53a7e-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="53a7e-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="53a7e-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="53a7e-112">Delegated (work or school account)</span></span> | <span data-ttu-id="53a7e-113">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="53a7e-113">Calendars.Read</span></span>    |
|<span data-ttu-id="53a7e-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="53a7e-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="53a7e-115">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="53a7e-115">Calendars.Read</span></span>    |
|<span data-ttu-id="53a7e-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="53a7e-116">Application</span></span> | <span data-ttu-id="53a7e-117">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="53a7e-117">Calendars.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="53a7e-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="53a7e-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /me/events/{id}/attachments
GET /users/{id|userPrincipalName}/events/{id}/attachments
```

<!--
GET /groups/{id}/events/{id}/attachments
-->

## <a name="optional-query-parameters"></a><span data-ttu-id="53a7e-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="53a7e-119">Optional query parameters</span></span>

<span data-ttu-id="53a7e-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="53a7e-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="53a7e-121">En concreto, puede usar el `$expand` parámetro para incluir todos los datos adjuntos de (evento) en línea con el resto de las propiedades de evento de consulta.</span><span class="sxs-lookup"><span data-stu-id="53a7e-121">In particular, you can use the `$expand` query parameter to include all of the event attachments inline with the rest of the event properties.</span></span> <span data-ttu-id="53a7e-122">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="53a7e-122">For example:</span></span>

```http
GET https://graph.microsoft.com/beta/me/events/{id}?$expand=attachments
```

## <a name="request-headers"></a><span data-ttu-id="53a7e-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="53a7e-123">Request headers</span></span>

| <span data-ttu-id="53a7e-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="53a7e-124">Name</span></span>       | <span data-ttu-id="53a7e-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="53a7e-125">Type</span></span> | <span data-ttu-id="53a7e-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="53a7e-126">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="53a7e-127">Autorización</span><span class="sxs-lookup"><span data-stu-id="53a7e-127">Authorization</span></span>  | <span data-ttu-id="53a7e-128">string</span><span class="sxs-lookup"><span data-stu-id="53a7e-128">string</span></span>  | <span data-ttu-id="53a7e-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="53a7e-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="53a7e-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="53a7e-131">Request body</span></span>

<span data-ttu-id="53a7e-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="53a7e-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="53a7e-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="53a7e-133">Response</span></span>

<span data-ttu-id="53a7e-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="53a7e-134">If successful, this method returns a `200 OK` response code and collection of [Attachment](../resources/attachment.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="53a7e-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="53a7e-135">Example</span></span>

### <a name="request"></a><span data-ttu-id="53a7e-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="53a7e-136">Request</span></span>

<span data-ttu-id="53a7e-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="53a7e-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_attachments"
}-->

```http
GET https://graph.microsoft.com/beta/me/events/{id}/attachments
```

### <a name="response"></a><span data-ttu-id="53a7e-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="53a7e-138">Response</span></span>

<span data-ttu-id="53a7e-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="53a7e-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
