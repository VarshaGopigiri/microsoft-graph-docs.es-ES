---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Obtener acceso a elementos compartidos
ms.openlocfilehash: d396e7bb79f3c2bbc9c824d48b6fa3df4a5ef26c
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="accessing-shared-driveitems"></a><span data-ttu-id="be7bd-102">Acceder a objetos DriveItem compartidos</span><span class="sxs-lookup"><span data-stu-id="be7bd-102">Accessing shared DriveItems</span></span>

<span data-ttu-id="be7bd-103">Acceda a un objeto [DriveItem](../resources/driveitem.md) compartido o a una colección de elementos compartidos mediante el uso de un **shareId** o una dirección URL para compartir.</span><span class="sxs-lookup"><span data-stu-id="be7bd-103">Access a shared [DriveItem](../resources/driveitem.md) or a collection of shared items by using a **shareId** or sharing URL.</span></span>

<span data-ttu-id="be7bd-104">Para usar una dirección URL para compartir con esta API, la aplicación debe [transformar la dirección URL en un token para compartir](#encoding-sharing-urls).</span><span class="sxs-lookup"><span data-stu-id="be7bd-104">To use a sharing URL with this API, your app needs to [transform the URL into a sharing token](#encoding-sharing-urls).</span></span>

## <a name="permissions"></a><span data-ttu-id="be7bd-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="be7bd-105">Permissions</span></span>

<span data-ttu-id="be7bd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="be7bd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="be7bd-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="be7bd-108">Permission type</span></span>      | <span data-ttu-id="be7bd-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="be7bd-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="be7bd-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="be7bd-110">Delegated (work or school account)</span></span> | <span data-ttu-id="be7bd-111">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="be7bd-111">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="be7bd-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="be7bd-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="be7bd-113">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="be7bd-113">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="be7bd-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="be7bd-114">Application</span></span> | <span data-ttu-id="be7bd-115">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="be7bd-115">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="be7bd-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="be7bd-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /shares/{shareIdOrEncodedSharingUrl}
```

### <a name="path-parameters"></a><span data-ttu-id="be7bd-117">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="be7bd-117">Path Parameters</span></span>

| <span data-ttu-id="be7bd-118">Nombre del parámetro</span><span class="sxs-lookup"><span data-stu-id="be7bd-118">Parameter Name</span></span>        | <span data-ttu-id="be7bd-119">Valor</span><span class="sxs-lookup"><span data-stu-id="be7bd-119">Value</span></span>    | <span data-ttu-id="be7bd-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="be7bd-120">Description</span></span>                                                                         |
|:----------------------|:---------|:------------------------------------------------------------------------------------|
| <span data-ttu-id="be7bd-121">**sharingTokenOrUrl**</span><span class="sxs-lookup"><span data-stu-id="be7bd-121">**sharingTokenOrUrl**</span></span> | `string` | <span data-ttu-id="be7bd-122">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="be7bd-122">Required.</span></span> <span data-ttu-id="be7bd-123">Un token para compartir como se devuelve mediante la API o una dirección URL para compartir codificada correctamente.</span><span class="sxs-lookup"><span data-stu-id="be7bd-123">A sharing token as returned by the API or a properly encoded sharing URL.</span></span> |

### <a name="encoding-sharing-urls"></a><span data-ttu-id="be7bd-124">Codificar direcciones URL para compartir</span><span class="sxs-lookup"><span data-stu-id="be7bd-124">Encoding sharing URLs</span></span>

<span data-ttu-id="be7bd-125">Para codificar una dirección URL para compartir, use la lógica siguiente:</span><span class="sxs-lookup"><span data-stu-id="be7bd-125">To encode a sharing URL, use the following logic:</span></span>

1. <span data-ttu-id="be7bd-126">Primero, use base64 para codificar la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="be7bd-126">First, use base64 encode the URL.</span></span>
2. <span data-ttu-id="be7bd-127">Convierta el resultado codificado en base64 en [formato unpadded base64url](https://en.wikipedia.org/wiki/Base64) quitando los caracteres `=` del final del valor, reemplazando `/` por `_` y `+` por `-`).</span><span class="sxs-lookup"><span data-stu-id="be7bd-127">Convert the base64 encoded result to [unpadded base64url format](https://en.wikipedia.org/wiki/Base64) by removing `=` characters from the end of the value, replacing `/` with `_` and `+` with `-`.)</span></span>
3. <span data-ttu-id="be7bd-128">Anexe `u!` al principio de la cadena.</span><span class="sxs-lookup"><span data-stu-id="be7bd-128">Append `u!` to be beginning of the string.</span></span>

<span data-ttu-id="be7bd-129">Como ejemplo, para codificar una dirección URL en C#:</span><span class="sxs-lookup"><span data-stu-id="be7bd-129">As an example, to encode a URL in C#:</span></span>

```csharp
string sharingUrl = "https://onedrive.live.com/redir?resid=1231244193912!12&authKey=1201919!12921!1";
string base64Value = System.Convert.ToBase64String(System.Text.Encoding.UTF8.GetBytes(sharingUrl));
string encodedUrl = "u!" + base64Value.TrimEnd('=').Replace('/','_').Replace('+','-');
```

## <a name="response"></a><span data-ttu-id="be7bd-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="be7bd-130">Response</span></span>

<span data-ttu-id="be7bd-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un recurso [sharedDriveItem](../resources/shareddriveitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="be7bd-131">If successful, this method returns a `200 OK` response code and a [sharedDriveItem](../resources/shareddriveitem.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="be7bd-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="be7bd-132">Example</span></span>

### <a name="request"></a><span data-ttu-id="be7bd-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="be7bd-133">Request</span></span>

<span data-ttu-id="be7bd-134">Este es un ejemplo de la solicitud para recuperar un elemento compartido:</span><span class="sxs-lookup"><span data-stu-id="be7bd-134">Here is an example of the request to retrieve a shared item:</span></span>

<!-- { "blockType": "request", "name": "get-shared-root" } -->

```http
GET /shares/{shareIdOrEncodedSharingUrl}
```

### <a name="response"></a><span data-ttu-id="be7bd-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="be7bd-135">Response</span></span>

<span data-ttu-id="be7bd-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="be7bd-136">Here is an example of the response.</span></span>

<!-- { "blockType": "response", "truncated": true, "@odata.type": "microsoft.graph.sharedDriveItem" } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "id": "B64397C8-07AE-43E4-920E-32BFB4331A5B",
  "name": "contoso project.docx",
  "owner": {
    "user": {
      "id": "98E88F1C-F8DC-47CC-A406-C090248B30E5",
      "displayName": "Ryan Gregg"
    }
  },
  "remoteItem": { 
    "driveId": "",
    "id": ""
  }
}
```

## <a name="access-the-shared-item-directly"></a><span data-ttu-id="be7bd-137">Acceder directamente al elemento compartido</span><span class="sxs-lookup"><span data-stu-id="be7bd-137">Access the shared item directly</span></span>

<span data-ttu-id="be7bd-p103">Mientras que [**SharedDriveItem**](../resources/shareddriveitem.md) contiene alguna información útil, la mayoría de las aplicaciones querrán acceder directamente al objeto [DriveItem](../resources/driveitem.md) compartido. El recurso **SharedDriveItem** incluye un **root** y relaciones de **items** que pueden acceder al contenido del ámbito del elemento compartido.</span><span class="sxs-lookup"><span data-stu-id="be7bd-p103">While the [**SharedDriveItem**](../resources/shareddriveitem.md) contains some useful information, most apps will want to directly access the shared [DriveItem](../resources/driveitem.md). The **SharedDriveItem** resource includes a **root** and **items** relationships which can access content within the scope of the shared item.</span></span>

## <a name="example-single-file"></a><span data-ttu-id="be7bd-140">Ejemplo (archivo único)</span><span class="sxs-lookup"><span data-stu-id="be7bd-140">Example (single file)</span></span>

### <a name="request"></a><span data-ttu-id="be7bd-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="be7bd-141">Request</span></span>

<span data-ttu-id="be7bd-142">Al solicitar la relación **driveItem**, se devolverá el objeto **DriveItem** compartido.</span><span class="sxs-lookup"><span data-stu-id="be7bd-142">By requesting the **root** relationship, the **DriveItem** that was shared will be returned.</span></span>

<!-- { "blockType": "request", "name": "get-shared-driveitem" } -->

```http
GET /shares/{shareIdOrUrl}/driveItem
```

### <a name="response"></a><span data-ttu-id="be7bd-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="be7bd-143">Response</span></span>

<!-- { "blockType": "response", "truncated": true, "@odata.type": "microsoft.graph.driveItem" } -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "id": "9FFFDB3C-5B87-4062-9606-1B008CA88E44",
  "name": "contoso project.docx",
  "eTag": "2246BD2D-7811-4660-BD0F-1CF36133677B,1",
  "file": {},
  "size": 109112
}
```

## <a name="example-shared-folder"></a><span data-ttu-id="be7bd-144">Ejemplo (carpeta compartida)</span><span class="sxs-lookup"><span data-stu-id="be7bd-144">Example (shared folder)</span></span>

### <a name="request"></a><span data-ttu-id="be7bd-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="be7bd-145">Request</span></span>

<span data-ttu-id="be7bd-146">Al solicitar la relación **driveItem** y expandir la colección **children**, se devolverá el objeto **DriveItem** compartido junto con los archivos de la carpeta compartida.</span><span class="sxs-lookup"><span data-stu-id="be7bd-146">By requesting the **root** relationship and expanding the **children** collection, the **DriveItem** that was shared will be returned along with the files within the shared folder.</span></span>

<!-- { "blockType": "request", "name": "get-shared-driveitem-expand-children" } -->

```http
GET /shares/{shareIdOrUrl}/driveItem?$expand=children
```

### <a name="response"></a><span data-ttu-id="be7bd-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="be7bd-147">Response</span></span>

<!-- { "blockType": "response", "truncated": true, "@odata.type": "microsoft.graph.driveItem" } -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "id": "9FFFDB3C-5B87-4062-9606-1B008CA88E44",
  "name": "Contoso Project",
  "eTag": "2246BD2D-7811-4660-BD0F-1CF36133677B,1",
  "folder": {},
  "size": 10911212,
  "children": [
    {
      "id": "AFBBDD79-868E-452D-AD4D-24697D4A4044",
      "name": "Propsoal.docx",
      "file": {},
      "size": 19001
    },
    {
      "id": "A91FE90A-2F2C-4EE6-B412-C4FFBA3F71A6",
      "name": "Update to Proposal.docx",
      "file": {},
      "size": 91001
    }
  ]
}
```

## <a name="error-responses"></a><span data-ttu-id="be7bd-148">Respuestas de error</span><span class="sxs-lookup"><span data-stu-id="be7bd-148">Error Responses</span></span>

<span data-ttu-id="be7bd-149">Lea el tema [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="be7bd-149">Read the [Error Responses][error-response] topic for more information about how errors are returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="be7bd-150">Comentarios</span><span class="sxs-lookup"><span data-stu-id="be7bd-150">Remarks</span></span>

* <span data-ttu-id="be7bd-151">Para OneDrive para la Empresa y SharePoint, la API de recursos compartidos siempre requiere autenticación y no puede usarse para tener acceso a contenido compartido de manera anónima sin un contexto de usuario.</span><span class="sxs-lookup"><span data-stu-id="be7bd-151">For OneDrive for Business and SharePoint, the Shares API always requires authentication and cannot be used to access anonymously shared content without a user context.</span></span>

[error-response]: ../../../concepts/errors.md

<!-- {
  "type": "#page.annotation",
  "description": "Access the contents of a sharing link with the OneDrive API.",
  "keywords": "shares,shared,sharing,share link, sharing link, share id, share token",
  "section": "documentation",
  "tocPath": "Sharing/Use a link"
} -->
