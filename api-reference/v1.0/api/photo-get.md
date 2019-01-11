---
title: Get photo
description: Recupera las propiedades y las relaciones del objeto photo.
localization_priority: Normal
ms.openlocfilehash: 808eda22550eb6c9affed42bdac9a21189a22cf0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27837222"
---
# <a name="get-photo"></a><span data-ttu-id="779f2-103">Get photo</span><span class="sxs-lookup"><span data-stu-id="779f2-103">Get photo</span></span>

<span data-ttu-id="779f2-104">Recupera las propiedades y las relaciones del objeto photo.</span><span class="sxs-lookup"><span data-stu-id="779f2-104">Retrieve the properties and relationships of photo object.</span></span>
## <a name="permissions"></a><span data-ttu-id="779f2-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="779f2-105">Permissions</span></span>
<span data-ttu-id="779f2-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="779f2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="779f2-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="779f2-108">Permission type</span></span>      | <span data-ttu-id="779f2-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="779f2-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="779f2-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="779f2-110">Delegated (work or school account)</span></span> | <span data-ttu-id="779f2-111">Files.Read</span><span class="sxs-lookup"><span data-stu-id="779f2-111">Files.Read</span></span>    |
|<span data-ttu-id="779f2-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="779f2-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="779f2-113">Files.Read</span><span class="sxs-lookup"><span data-stu-id="779f2-113">Files.Read</span></span>    |
|<span data-ttu-id="779f2-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="779f2-114">Application</span></span> | <span data-ttu-id="779f2-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="779f2-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="779f2-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="779f2-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/photo
GET /groups/{id}/photo
GET /drive/root/createdByUser/photo
```
## <a name="optional-query-parameters"></a><span data-ttu-id="779f2-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="779f2-117">Optional query parameters</span></span>
<span data-ttu-id="779f2-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="779f2-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="779f2-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="779f2-119">Request headers</span></span>
| <span data-ttu-id="779f2-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="779f2-120">Name</span></span>       | <span data-ttu-id="779f2-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="779f2-121">Type</span></span> | <span data-ttu-id="779f2-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="779f2-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="779f2-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="779f2-123">Authorization</span></span>  | <span data-ttu-id="779f2-124">string</span><span class="sxs-lookup"><span data-stu-id="779f2-124">string</span></span>  | <span data-ttu-id="779f2-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="779f2-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="779f2-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="779f2-127">Request body</span></span>
<span data-ttu-id="779f2-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="779f2-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="779f2-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="779f2-129">Response</span></span>

<span data-ttu-id="779f2-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [photo](../resources/photo.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="779f2-130">If successful, this method returns a `200 OK` response code and [photo](../resources/photo.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="779f2-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="779f2-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="779f2-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="779f2-132">Request</span></span>
<span data-ttu-id="779f2-133">Este es un ejemplo de la solicitud de metadatos de fotos.</span><span class="sxs-lookup"><span data-stu-id="779f2-133">Here is an example of the request for photo metadata.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_photo"
}-->
```http
GET https://graph.microsoft.com/v1.0/users/{id|userPrincipalName}/photo
```
##### <a name="response"></a><span data-ttu-id="779f2-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="779f2-134">Response</span></span>
<span data-ttu-id="779f2-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="779f2-135">Here is an example of the response.</span></span>
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
##### <a name="request"></a><span data-ttu-id="779f2-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="779f2-136">Request</span></span>
<span data-ttu-id="779f2-137">Este es un ejemplo de la solicitud de bytes de fotos.</span><span class="sxs-lookup"><span data-stu-id="779f2-137">Here is an example of the request for the photo bytes.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_photo_value"
}-->
```http
GET https://graph.microsoft.com/v1.0/users/{id|userPrincipalName}/photo/$value
```
##### <a name="response"></a><span data-ttu-id="779f2-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="779f2-138">Response</span></span>
<span data-ttu-id="779f2-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="779f2-139">Here is an example of the response.</span></span>

<!-- { "blockType": "response", "@odata.type": "Edm.Stream" } -->

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
