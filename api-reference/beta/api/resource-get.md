---
title: Obtener recurso
description: Recupera los datos binarios de un objeto resource de un archivo o una imagen.
localization_priority: Normal
ms.openlocfilehash: 1f8150e0449009eef4d1afe2ce014ae848153382
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27841261"
---
# <a name="get-resource"></a><span data-ttu-id="6d234-103">Obtener recurso</span><span class="sxs-lookup"><span data-stu-id="6d234-103">Get resource</span></span>

> <span data-ttu-id="6d234-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6d234-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6d234-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6d234-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6d234-106">Recupera los datos binarios de un objeto [resource](../resources/resource.md) de un archivo o una imagen.</span><span class="sxs-lookup"><span data-stu-id="6d234-106">Retrieve the binary data of a file or image [resource](../resources/resource.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="6d234-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="6d234-107">Permissions</span></span>
<span data-ttu-id="6d234-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6d234-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6d234-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6d234-110">Permission type</span></span>      | <span data-ttu-id="6d234-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6d234-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6d234-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6d234-112">Delegated (work or school account)</span></span> | <span data-ttu-id="6d234-113">Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6d234-113">Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="6d234-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6d234-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6d234-115">Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6d234-115">Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="6d234-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6d234-116">Application</span></span> | <span data-ttu-id="6d234-117">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6d234-117">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="6d234-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6d234-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/resources/{id}/content
GET /users/{id | userPrincipalName}/onenote/resources/{id}/content
GET /groups/{id}/onenote/resources/{id}/content
GET /sites/{id}/onenote/resources/{id}/content
```

## <a name="request-headers"></a><span data-ttu-id="6d234-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6d234-119">Request headers</span></span>
| <span data-ttu-id="6d234-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="6d234-120">Name</span></span>       | <span data-ttu-id="6d234-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="6d234-121">Type</span></span> | <span data-ttu-id="6d234-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d234-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="6d234-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="6d234-123">Authorization</span></span>  | <span data-ttu-id="6d234-124">string</span><span class="sxs-lookup"><span data-stu-id="6d234-124">string</span></span>  | <span data-ttu-id="6d234-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6d234-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6d234-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6d234-127">Request body</span></span>
<span data-ttu-id="6d234-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6d234-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6d234-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6d234-129">Response</span></span>

<span data-ttu-id="6d234-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y los datos binarios del archivo o la imagen en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6d234-130">If successful, this method returns a `200 OK` response code and the image or file binary data in the response body.</span></span>

<span data-ttu-id="6d234-131">Nota: Las imágenes no se procesan directamente en un explorador porque requieren autorización para recuperarlas, al igual que el resto del contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="6d234-131">Note: Images won't render directly in a browser because they require authorization to retrieve them, like the rest of the page content.</span></span>
## <a name="example"></a><span data-ttu-id="6d234-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6d234-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6d234-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6d234-133">Request</span></span>
<span data-ttu-id="6d234-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6d234-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_resource"
}-->
```http
GET https://graph.microsoft.com/beta/me/onenote/resources/{id}/content
```
##### <a name="response"></a><span data-ttu-id="6d234-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6d234-135">Response</span></span>
<span data-ttu-id="6d234-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6d234-136">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->
```http
HTTP/1.1 200 OK

...binary data...
```
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.onenoteResource"
} -->

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
