---
title: Get photo
description: Recupera las propiedades y las relaciones del objeto photo.
ms.openlocfilehash: 16e0849d3cc1a9a98226b6f34221a8a37cec72b1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083134"
---
# <a name="get-photo"></a><span data-ttu-id="5029b-103">Obtener foto</span><span class="sxs-lookup"><span data-stu-id="5029b-103">Get photo</span></span>

> <span data-ttu-id="5029b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5029b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5029b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5029b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5029b-106">Recupera las propiedades y las relaciones del objeto photo.</span><span class="sxs-lookup"><span data-stu-id="5029b-106">Retrieve the properties and relationships of photo object.</span></span>
## <a name="permissions"></a><span data-ttu-id="5029b-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="5029b-107">Permissions</span></span>
<span data-ttu-id="5029b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5029b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5029b-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5029b-110">Permission type</span></span>      | <span data-ttu-id="5029b-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5029b-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5029b-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5029b-112">Delegated (work or school account)</span></span> | <span data-ttu-id="5029b-113">Files.Read</span><span class="sxs-lookup"><span data-stu-id="5029b-113">Files.Read</span></span>    |
|<span data-ttu-id="5029b-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5029b-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5029b-115">Files.Read</span><span class="sxs-lookup"><span data-stu-id="5029b-115">Files.Read</span></span>    |
|<span data-ttu-id="5029b-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5029b-116">Application</span></span> | <span data-ttu-id="5029b-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5029b-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="5029b-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5029b-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/photo
GET /groups/{id}/photo
GET /drive/root/createdByUser/photo
```
## <a name="optional-query-parameters"></a><span data-ttu-id="5029b-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="5029b-119">Optional query parameters</span></span>
<span data-ttu-id="5029b-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5029b-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="5029b-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5029b-121">Request headers</span></span>
| <span data-ttu-id="5029b-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="5029b-122">Name</span></span>       | <span data-ttu-id="5029b-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="5029b-123">Type</span></span> | <span data-ttu-id="5029b-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="5029b-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="5029b-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="5029b-125">Authorization</span></span>  | <span data-ttu-id="5029b-126">string</span><span class="sxs-lookup"><span data-stu-id="5029b-126">string</span></span>  | <span data-ttu-id="5029b-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5029b-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="5029b-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5029b-129">Request body</span></span>
<span data-ttu-id="5029b-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5029b-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5029b-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5029b-131">Response</span></span>

<span data-ttu-id="5029b-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [photo](../resources/photo.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5029b-132">If successful, this method returns a `200 OK` response code and [photo](../resources/photo.md) object in the response body.</span></span>
## <a name="examples"></a><span data-ttu-id="5029b-133">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5029b-133">Examples</span></span>
##### <a name="request"></a><span data-ttu-id="5029b-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5029b-134">Request</span></span>
<span data-ttu-id="5029b-135">Este es un ejemplo de la solicitud de metadatos de fotos.</span><span class="sxs-lookup"><span data-stu-id="5029b-135">Here is an example of the request for photo metadata.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_photo"
}-->
```http
GET https://graph.microsoft.com/beta/users/{id|userPrincipalName}/photo
```
##### <a name="response"></a><span data-ttu-id="5029b-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5029b-136">Response</span></span>
<span data-ttu-id="5029b-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5029b-137">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.profilePhoto"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 53

{
  "height": 99,
  "width": 99,
  "id": "id-value"
}
```
##### <a name="request"></a><span data-ttu-id="5029b-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5029b-138">Request</span></span>
<span data-ttu-id="5029b-139">Este es un ejemplo de la solicitud de bytes de fotos.</span><span class="sxs-lookup"><span data-stu-id="5029b-139">Here is an example of the request for the photo bytes.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_photo"
}-->
```http
GET https://graph.microsoft.com/beta/users/{id|userPrincipalName}/photo/$value
```
##### <a name="response"></a><span data-ttu-id="5029b-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5029b-140">Response</span></span>
<span data-ttu-id="5029b-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5029b-141">Here is an example of the response.</span></span>

<!-- { "blockType": "ignored","@odata.type": "stream" } -->

```http
HTTP/1.1 200 OK
Cache-Control: private
Content-Type: image/jpeg
ETag: "A19A6498"
request-id: 16e1bff0-6d74-47d6-944c-61707916a74c
client-request-id: 16e1bff0-6d74-47d6-944c-61707916a74c
x-ms-ags-diagnostic: {"ServerInfo":{"DataCenter":"West US","Slice":"SliceA","Ring":"5","ScaleUnit":"003","Host":"AGSFE_IN_14","ADSiteName":"WST"}}
Access-Control-Allow-Origin: *
Access-Control-Expose-Headers: ETag, Location, Preference-Applied, Content-Range, request-id, client-request-id
Duration: 125.9389
Date: Wed, 13 Dec 2017 22:02:17 GMT
Content-Length: 250526

<binary image data>
```




<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get photo",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
