---
title: Obtener recurso
description: Recupera los datos binarios de un objeto resource de un archivo o una imagen.
localization_priority: Normal
ms.openlocfilehash: ec28daacf61e18f16e5c6598d036759eac1fb131
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27884794"
---
# <a name="get-resource"></a><span data-ttu-id="2b075-103">Obtener recurso</span><span class="sxs-lookup"><span data-stu-id="2b075-103">Get resource</span></span>

<span data-ttu-id="2b075-104">Recupera los datos binarios de un objeto [resource](../resources/resource.md) de un archivo o una imagen.</span><span class="sxs-lookup"><span data-stu-id="2b075-104">Retrieve the binary data of a file or image [resource](../resources/resource.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="2b075-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="2b075-105">Permissions</span></span>
<span data-ttu-id="2b075-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2b075-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2b075-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2b075-108">Permission type</span></span>      | <span data-ttu-id="2b075-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2b075-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2b075-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2b075-110">Delegated (work or school account)</span></span> | <span data-ttu-id="2b075-111">Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2b075-111">Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="2b075-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2b075-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2b075-113">Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2b075-113">Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="2b075-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2b075-114">Application</span></span> | <span data-ttu-id="2b075-115">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2b075-115">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="2b075-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2b075-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/resources/{id}/content
GET /users/{id | userPrincipalName}/onenote/resources/{id}/content
GET /groups/{id}/onenote/resources/{id}/content
GET /sites/{id}/onenote/resources/{id}/content
```

## <a name="request-headers"></a><span data-ttu-id="2b075-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2b075-117">Request headers</span></span>
| <span data-ttu-id="2b075-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="2b075-118">Name</span></span>       | <span data-ttu-id="2b075-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="2b075-119">Type</span></span> | <span data-ttu-id="2b075-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b075-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="2b075-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="2b075-121">Authorization</span></span>  | <span data-ttu-id="2b075-122">string</span><span class="sxs-lookup"><span data-stu-id="2b075-122">string</span></span>  | <span data-ttu-id="2b075-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2b075-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="2b075-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2b075-125">Request body</span></span>
<span data-ttu-id="2b075-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2b075-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2b075-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b075-127">Response</span></span>

<span data-ttu-id="2b075-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y los datos binarios del archivo o la imagen en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2b075-128">If successful, this method returns a `200 OK` response code and the image or file binary data in the response body.</span></span>

<span data-ttu-id="2b075-129">Nota: Las imágenes no se procesan directamente en un explorador porque requieren autorización para recuperarlas, al igual que el resto del contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="2b075-129">Note: Images won't render directly in a browser because they require authorization to retrieve them, like the rest of the page content.</span></span>
## <a name="example"></a><span data-ttu-id="2b075-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2b075-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2b075-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2b075-131">Request</span></span>
<span data-ttu-id="2b075-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2b075-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_resource"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/resources/{id}/content
```
##### <a name="response"></a><span data-ttu-id="2b075-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b075-133">Response</span></span>
<span data-ttu-id="2b075-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2b075-134">Here is an example of the response.</span></span>
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
