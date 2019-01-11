---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Descargar un archivo
localization_priority: Normal
ms.openlocfilehash: ac391f5ffb6af9fc288bdc22cf0dbf3c77dca0b9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27854758"
---
# <a name="download-the-contents-of-a-driveitem"></a><span data-ttu-id="778c1-102">Descargar el contenido de un objeto DriveItem</span><span class="sxs-lookup"><span data-stu-id="778c1-102">Download the contents of a DriveItem</span></span>

> <span data-ttu-id="778c1-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="778c1-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="778c1-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="778c1-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="778c1-105">Descargue el contenido de la secuencia principal (archivo) de un DriveItem.</span><span class="sxs-lookup"><span data-stu-id="778c1-105">Download the contents of the primary stream (file) of a DriveItem.</span></span> <span data-ttu-id="778c1-106">Solo se pueden descargar objetos driveItem con la propiedad **file**.</span><span class="sxs-lookup"><span data-stu-id="778c1-106">Only driveItems with the **file** property can be downloaded.</span></span>

## <a name="permissions"></a><span data-ttu-id="778c1-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="778c1-107">Permissions</span></span>

<span data-ttu-id="778c1-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="778c1-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="778c1-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="778c1-110">Permission type</span></span>      | <span data-ttu-id="778c1-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="778c1-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="778c1-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="778c1-112">Delegated (work or school account)</span></span> | <span data-ttu-id="778c1-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="778c1-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="778c1-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="778c1-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="778c1-115">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="778c1-115">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="778c1-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="778c1-116">Application</span></span> | <span data-ttu-id="778c1-117">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="778c1-117">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="778c1-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="778c1-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /drives/{drive-id}/items/{item-id}/content
GET /groups/{group-id}/drive/items/{item-id}/content
GET /me/drive/root:/{item-path}:/content
GET /me/drive/items/{item-id}/content
GET /sites/{siteId}/drive/items/{item-id}/content
GET /users/{userId}/drive/items/{item-id}/content
```

## <a name="optional-request-headers"></a><span data-ttu-id="778c1-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="778c1-119">Optional request headers</span></span>

| <span data-ttu-id="778c1-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="778c1-120">Name</span></span>          | <span data-ttu-id="778c1-121">Valor</span><span class="sxs-lookup"><span data-stu-id="778c1-121">Value</span></span>  | <span data-ttu-id="778c1-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="778c1-122">Description</span></span>                                                                                                                                              |
|:--------------|:-------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="778c1-123">if-none-match</span><span class="sxs-lookup"><span data-stu-id="778c1-123">if-none-match</span></span> | <span data-ttu-id="778c1-124">String</span><span class="sxs-lookup"><span data-stu-id="778c1-124">String</span></span> | <span data-ttu-id="778c1-125">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada coincide con la etiqueta actual del archivo, se devuelve una respuesta `HTTP 304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="778c1-125">If this request header is included and the eTag (or cTag) provided matches the current tag on the file, an `HTTP 304 Not Modified` response is returned.</span></span> |

## <a name="example"></a><span data-ttu-id="778c1-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="778c1-126">Example</span></span>

<span data-ttu-id="778c1-127">Este es un ejemplo para descargar un archivo completo.</span><span class="sxs-lookup"><span data-stu-id="778c1-127">Here is an example to download a complete file.</span></span>


<!-- { "blockType": "request", "name": "download-item-content", "scopes": "files.read" } -->

```http
GET /me/drive/items/{item-id}/content
```

### <a name="response"></a><span data-ttu-id="778c1-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="778c1-128">Response</span></span>

<span data-ttu-id="778c1-p104">Devuelve una respuesta `302 Found` que redirige a una URL de descarga autenticada previamente para el archivo. Se trata de la misma dirección URL disponible mediante la propiedad `@microsoft.graph.downloadUrl` del objeto DriveItem.</span><span class="sxs-lookup"><span data-stu-id="778c1-p104">Returns a `302 Found` response redirecting to a pre-authenticated download URL for the file. This is the same URL available through the `@microsoft.graph.downloadUrl` property on the DriveItem.</span></span>

<span data-ttu-id="778c1-p105">Para descargar el contenido del archivo, la aplicación tendrá que seguir el encabezado `Location` de la respuesta. Muchas bibliotecas de cliente HTTP seguirán de forma automática el redireccionamiento 302 e iniciarán la descarga del archivo de forma inmediata.</span><span class="sxs-lookup"><span data-stu-id="778c1-p105">To download the contents of the file your application will need to follow the `Location` header in the response. Many HTTP client libraries will automatically follow the 302 redirection and start downloading the file immedately.</span></span>

<span data-ttu-id="778c1-133">Las URL de descarga autenticadas previamente solo son válidas durante un breve período de tiempo (unos minutos) y no requieren un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="778c1-133">Pre-authenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header to download.</span></span>

<!-- { "blockType": "response", "@odata.type": "stream" } -->

```http
HTTP/1.1 302 Found
Location: https://b0mpua-by3301.files.1drv.com/y23vmagahszhxzlcvhasdhasghasodfi
```

## <a name="partial-range-downloads"></a><span data-ttu-id="778c1-134">Descargas de rango parcial</span><span class="sxs-lookup"><span data-stu-id="778c1-134">Partial range downloads</span></span>

<span data-ttu-id="778c1-p106">Para descargar un rango parcial de bytes del archivo, la aplicación puede usar el encabezado `Range` como se especifica en [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt). Tenga en cuenta que debe anexar el encabezado `Range` a la dirección URL `@microsoft.graph.downloadUrl` real y no a la solicitud de `/content`.</span><span class="sxs-lookup"><span data-stu-id="778c1-p106">To download a partial range of bytes from the file, your app can use the `Range` header as specified in [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt). Note that you must append the `Range` header to the actual `@microsoft.graph.downloadUrl` URL and not to the request for `/content`.</span></span>

<!-- { "blockType": "request", "name": "download-item-partial", "scopes": "files.read" } -->

```http
GET https://b0mpua-by3301.files.1drv.com/y23vmag
Range: bytes=0-1023
```

<span data-ttu-id="778c1-p107">Esto devolverá una respuesta `HTTP 206 Partial Content` con el rango de solicitud de bytes del archivo. Si no se puede generar el rango, se puede omitir el encabezado Range y se devolverá una respuesta `HTTP 200` con el contenido completo del archivo.</span><span class="sxs-lookup"><span data-stu-id="778c1-p107">This will return an `HTTP 206 Partial Content` response with the request range of bytes from the file. If the range cannot be generated the Range header may be ignored and an `HTTP 200` response would be returned with the full contents of the file.</span></span>

<!-- { "blockType": "response", "name": "download-item-partial", "@odata.type": "stream" } -->

```http
HTTP/1.1 206 Partial Content
Content-Range: bytes 0-1023/2048

<first 1024 bytes of file>
```

### <a name="error-responses"></a><span data-ttu-id="778c1-139">Respuestas de error</span><span class="sxs-lookup"><span data-stu-id="778c1-139">Error responses</span></span>

<span data-ttu-id="778c1-140">Vea [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="778c1-140">See [Error Responses][error-response] for more info about how errors are returned.</span></span>

[error-response]: /graph/errors

<!-- {
  "type": "#page.annotation",
  "description": "Download the contents of a DriveItem.",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Items/Download"
} -->
