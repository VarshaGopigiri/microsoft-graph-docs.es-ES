---
title: Obtener recurso
description: Recupera los datos binarios de un objeto resource de un archivo o una imagen.
localization_priority: Normal
author: jewan-microsoft
ms.prod: onenote
ms.openlocfilehash: 9937040d9e53213946df9eb31cf9136bcfda7c71
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27946066"
---
# <a name="get-resource"></a><span data-ttu-id="29a12-103">Obtener recurso</span><span class="sxs-lookup"><span data-stu-id="29a12-103">Get resource</span></span>

<span data-ttu-id="29a12-104">Recupera los datos binarios de un objeto [resource](../resources/resource.md) de un archivo o una imagen.</span><span class="sxs-lookup"><span data-stu-id="29a12-104">Retrieve the binary data of a file or image [resource](../resources/resource.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="29a12-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="29a12-105">Permissions</span></span>
<span data-ttu-id="29a12-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="29a12-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="29a12-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="29a12-108">Permission type</span></span>      | <span data-ttu-id="29a12-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="29a12-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="29a12-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="29a12-110">Delegated (work or school account)</span></span> | <span data-ttu-id="29a12-111">Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="29a12-111">Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="29a12-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="29a12-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="29a12-113">Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="29a12-113">Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="29a12-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="29a12-114">Application</span></span> | <span data-ttu-id="29a12-115">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="29a12-115">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="29a12-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="29a12-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/resources/{id}/content
GET /users/{id | userPrincipalName}/onenote/resources/{id}/content
GET /groups/{id}/onenote/resources/{id}/content
GET /sites/{id}/onenote/resources/{id}/content
```

## <a name="request-headers"></a><span data-ttu-id="29a12-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="29a12-117">Request headers</span></span>
| <span data-ttu-id="29a12-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="29a12-118">Name</span></span>       | <span data-ttu-id="29a12-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="29a12-119">Type</span></span> | <span data-ttu-id="29a12-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="29a12-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="29a12-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="29a12-121">Authorization</span></span>  | <span data-ttu-id="29a12-122">string</span><span class="sxs-lookup"><span data-stu-id="29a12-122">string</span></span>  | <span data-ttu-id="29a12-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="29a12-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="29a12-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="29a12-125">Request body</span></span>
<span data-ttu-id="29a12-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="29a12-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="29a12-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="29a12-127">Response</span></span>

<span data-ttu-id="29a12-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y los datos binarios del archivo o la imagen en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="29a12-128">If successful, this method returns a `200 OK` response code and the image or file binary data in the response body.</span></span>

<span data-ttu-id="29a12-129">Nota: Las imágenes no se procesan directamente en un explorador porque requieren autorización para recuperarlas, al igual que el resto del contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="29a12-129">Note: Images won't render directly in a browser because they require authorization to retrieve them, like the rest of the page content.</span></span>
## <a name="example"></a><span data-ttu-id="29a12-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="29a12-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="29a12-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="29a12-131">Request</span></span>
<span data-ttu-id="29a12-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="29a12-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_resource"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/resources/{id}/content
```
##### <a name="response"></a><span data-ttu-id="29a12-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="29a12-133">Response</span></span>
<span data-ttu-id="29a12-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="29a12-134">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Edm.Stream"
} -->
```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

...binary data...
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
