---
title: Obtener recurso
description: Recupera los datos binarios de un objeto resource de un archivo o una imagen.
ms.openlocfilehash: 81c07dca78381ede096c62eba73b0842ae294d55
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083741"
---
# <a name="get-resource"></a><span data-ttu-id="6363b-103">Obtener recurso</span><span class="sxs-lookup"><span data-stu-id="6363b-103">Get resource</span></span>

> <span data-ttu-id="6363b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6363b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6363b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6363b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6363b-106">Recupera los datos binarios de un objeto [resource](../resources/resource.md) de un archivo o una imagen.</span><span class="sxs-lookup"><span data-stu-id="6363b-106">Retrieve the binary data of a file or image [resource](../resources/resource.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="6363b-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="6363b-107">Permissions</span></span>
<span data-ttu-id="6363b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6363b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6363b-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6363b-110">Permission type</span></span>      | <span data-ttu-id="6363b-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6363b-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6363b-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6363b-112">Delegated (work or school account)</span></span> | <span data-ttu-id="6363b-113">Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6363b-113">Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="6363b-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6363b-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6363b-115">Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6363b-115">Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="6363b-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6363b-116">Application</span></span> | <span data-ttu-id="6363b-117">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6363b-117">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="6363b-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6363b-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/resources/{id}/content
GET /users/{id | userPrincipalName}/onenote/resources/{id}/content
GET /groups/{id}/onenote/resources/{id}/content
GET /sites/{id}/onenote/resources/{id}/content
```

## <a name="request-headers"></a><span data-ttu-id="6363b-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6363b-119">Request headers</span></span>
| <span data-ttu-id="6363b-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="6363b-120">Name</span></span>       | <span data-ttu-id="6363b-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="6363b-121">Type</span></span> | <span data-ttu-id="6363b-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="6363b-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="6363b-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="6363b-123">Authorization</span></span>  | <span data-ttu-id="6363b-124">string</span><span class="sxs-lookup"><span data-stu-id="6363b-124">string</span></span>  | <span data-ttu-id="6363b-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6363b-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6363b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6363b-127">Request body</span></span>
<span data-ttu-id="6363b-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6363b-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6363b-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6363b-129">Response</span></span>

<span data-ttu-id="6363b-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y los datos binarios del archivo o la imagen en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6363b-130">If successful, this method returns a `200 OK` response code and the image or file binary data in the response body.</span></span>

<span data-ttu-id="6363b-131">Nota: Las imágenes no se procesan directamente en un explorador porque requieren autorización para recuperarlas, al igual que el resto del contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="6363b-131">Note: Images won't render directly in a browser because they require authorization to retrieve them, like the rest of the page content.</span></span>
## <a name="example"></a><span data-ttu-id="6363b-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6363b-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6363b-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6363b-133">Request</span></span>
<span data-ttu-id="6363b-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6363b-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_resource"
}-->
```http
GET https://graph.microsoft.com/beta/me/onenote/resources/{id}/content
```
##### <a name="response"></a><span data-ttu-id="6363b-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6363b-135">Response</span></span>
<span data-ttu-id="6363b-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6363b-136">Here is an example of the response.</span></span>
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
