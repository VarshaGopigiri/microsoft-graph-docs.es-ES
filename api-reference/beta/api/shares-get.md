---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Obtener acceso a elementos compartidos
localization_priority: Normal
ms.openlocfilehash: 46779e40862c7056cc60ef4be55595da5615e9f6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27864242"
---
# <a name="accessing-shared-driveitems"></a><span data-ttu-id="f3a6c-102">Acceder a objetos DriveItem compartidos</span><span class="sxs-lookup"><span data-stu-id="f3a6c-102">Accessing shared DriveItems</span></span>

<span data-ttu-id="f3a6c-103">Acceda a un objeto [DriveItem](../resources/driveitem.md) compartido o a una colección de elementos compartidos mediante el uso de un **shareId** o una dirección URL para compartir.</span><span class="sxs-lookup"><span data-stu-id="f3a6c-103">Access a shared [DriveItem](../resources/driveitem.md) or a collection of shared items by using a **shareId** or sharing URL.</span></span>

<span data-ttu-id="f3a6c-104">Para usar una dirección URL para compartir con esta API, la aplicación debe [transformar la dirección URL en un token para compartir](#encoding-sharing-urls).</span><span class="sxs-lookup"><span data-stu-id="f3a6c-104">To use a sharing URL with this API, your app needs to [transform the URL into a sharing token](#encoding-sharing-urls).</span></span>

## <a name="permissions"></a><span data-ttu-id="f3a6c-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="f3a6c-105">Permissions</span></span>

<span data-ttu-id="f3a6c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f3a6c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f3a6c-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f3a6c-108">Permission type</span></span>      | <span data-ttu-id="f3a6c-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f3a6c-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f3a6c-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f3a6c-110">Delegated (work or school account)</span></span> | <span data-ttu-id="f3a6c-111">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f3a6c-111">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="f3a6c-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f3a6c-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f3a6c-113">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f3a6c-113">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="f3a6c-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f3a6c-114">Application</span></span> | <span data-ttu-id="f3a6c-115">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f3a6c-115">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="f3a6c-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f3a6c-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET https://graph.microsoft.com/beta/shares/{shareIdOrEncodedSharingUrl}
```

### <a name="path-parameters"></a><span data-ttu-id="f3a6c-117">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="f3a6c-117">Path Parameters</span></span>

| <span data-ttu-id="f3a6c-118">Nombre del parámetro</span><span class="sxs-lookup"><span data-stu-id="f3a6c-118">Parameter Name</span></span>        | <span data-ttu-id="f3a6c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f3a6c-119">Value</span></span>    | <span data-ttu-id="f3a6c-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3a6c-120">Description</span></span>                                                                         |
|:----------------------|:---------|:------------------------------------------------------------------------------------|
| <span data-ttu-id="f3a6c-121">**sharingTokenOrUrl**</span><span class="sxs-lookup"><span data-stu-id="f3a6c-121">**sharingTokenOrUrl**</span></span> | `string` | <span data-ttu-id="f3a6c-122">Necesario.</span><span class="sxs-lookup"><span data-stu-id="f3a6c-122">Required.</span></span> <span data-ttu-id="f3a6c-123">Un token para compartir como se devuelve mediante la API o una dirección URL para compartir codificada correctamente.</span><span class="sxs-lookup"><span data-stu-id="f3a6c-123">A sharing token as returned by the API or a properly encoded sharing URL.</span></span> |

### <a name="encoding-sharing-urls"></a><span data-ttu-id="f3a6c-124">Codificar direcciones URL para compartir</span><span class="sxs-lookup"><span data-stu-id="f3a6c-124">Encoding sharing URLs</span></span>

<span data-ttu-id="f3a6c-125">Para codificar una dirección URL para compartir, use la lógica siguiente:</span><span class="sxs-lookup"><span data-stu-id="f3a6c-125">To encode a sharing URL, use the following logic:</span></span>

1. <span data-ttu-id="f3a6c-126">Primero, use base64 para codificar la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="f3a6c-126">First, use base64 encode the URL.</span></span>
2. <span data-ttu-id="f3a6c-127">Convierta el resultado codificado en base64 en [formato unpadded base64url](https://en.wikipedia.org/wiki/Base64) quitando los caracteres `=` del final del valor, reemplazando `/` por `_` y `+` por `-`).</span><span class="sxs-lookup"><span data-stu-id="f3a6c-127">Convert the base64 encoded result to [unpadded base64url format](https://en.wikipedia.org/wiki/Base64) by removing `=` characters from the end of the value, replacing `/` with `_` and `+` with `-`.)</span></span>
3. <span data-ttu-id="f3a6c-128">Anexe `u!` al principio de la cadena.</span><span class="sxs-lookup"><span data-stu-id="f3a6c-128">Append `u!` to be beginning of the string.</span></span>

<span data-ttu-id="f3a6c-129">Como ejemplo, para codificar una dirección URL en C#:</span><span class="sxs-lookup"><span data-stu-id="f3a6c-129">As an example, to encode a URL in C#:</span></span>

```csharp
string sharingUrl = "https://onedrive.live.com/redir?resid=1231244193912!12&authKey=1201919!12921!1";
string base64Value = System.Convert.ToBase64String(System.Text.Encoding.UTF8.GetBytes(sharingUrl));
string encodedUrl = "u!" + base64Value.TrimEnd('=').Replace('/','_').Replace('+','-');
```

## <a name="response"></a><span data-ttu-id="f3a6c-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f3a6c-130">Response</span></span>

<span data-ttu-id="f3a6c-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un recurso [sharedDriveItem](../resources/shareddriveitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f3a6c-131">If successful, this method returns a `200 OK` response code and a [sharedDriveItem](../resources/shareddriveitem.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f3a6c-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f3a6c-132">Example</span></span>

### <a name="request"></a><span data-ttu-id="f3a6c-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f3a6c-133">Request</span></span>

<span data-ttu-id="f3a6c-134">Este es un ejemplo de la solicitud para recuperar un elemento compartido:</span><span class="sxs-lookup"><span data-stu-id="f3a6c-134">Here is an example of the request to retrieve a shared item:</span></span>

<!-- { "blockType": "request", "name": "get-shared-root" } -->

```http
GET https://graph.microsoft.com/beta/shares/{shareIdOrEncodedSharingUrl}
```

### <a name="response"></a><span data-ttu-id="f3a6c-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f3a6c-135">Response</span></span>

<span data-ttu-id="f3a6c-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f3a6c-136">Here is an example of the response.</span></span>

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

## <a name="access-the-shared-item-directly"></a><span data-ttu-id="f3a6c-137">Acceder directamente al elemento compartido</span><span class="sxs-lookup"><span data-stu-id="f3a6c-137">Access the shared item directly</span></span>

<span data-ttu-id="f3a6c-p103">Mientras que [**SharedDriveItem**](../resources/shareddriveitem.md) contiene alguna información útil, la mayoría de las aplicaciones querrán acceder directamente al objeto [DriveItem](../resources/driveitem.md) compartido. El recurso **SharedDriveItem** incluye un **root** y relaciones de **items** que pueden acceder al contenido del ámbito del elemento compartido.</span><span class="sxs-lookup"><span data-stu-id="f3a6c-p103">While the [**SharedDriveItem**](../resources/shareddriveitem.md) contains some useful information, most apps will want to directly access the shared [DriveItem](../resources/driveitem.md). The **SharedDriveItem** resource includes a **root** and **items** relationships which can access content within the scope of the shared item.</span></span>

## <a name="example-single-file"></a><span data-ttu-id="f3a6c-140">Ejemplo (archivo único)</span><span class="sxs-lookup"><span data-stu-id="f3a6c-140">Example (single file)</span></span>

### <a name="request"></a><span data-ttu-id="f3a6c-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f3a6c-141">Request</span></span>

<span data-ttu-id="f3a6c-142">Al solicitar la relación **driveItem**, se devolverá el objeto **DriveItem** compartido.</span><span class="sxs-lookup"><span data-stu-id="f3a6c-142">By requesting the **driveItem** relationship, the **DriveItem** that was shared will be returned.</span></span>

<!-- { "blockType": "request", "name": "get-shared-driveitem" } -->

```http
GET /shares/{shareIdOrUrl}/driveItem
```

### <a name="response"></a><span data-ttu-id="f3a6c-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f3a6c-143">Response</span></span>

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

## <a name="example-shared-folder"></a><span data-ttu-id="f3a6c-144">Ejemplo (carpeta compartida)</span><span class="sxs-lookup"><span data-stu-id="f3a6c-144">Example (shared folder)</span></span>

### <a name="request"></a><span data-ttu-id="f3a6c-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f3a6c-145">Request</span></span>

<span data-ttu-id="f3a6c-146">Al solicitar la relación **driveItem** y expandir la colección **children**, se devolverá el objeto **DriveItem** compartido junto con los archivos de la carpeta compartida.</span><span class="sxs-lookup"><span data-stu-id="f3a6c-146">By requesting the **driveItem** relationship and expanding the **children** collection, the **DriveItem** that was shared will be returned along with the files within the shared folder.</span></span>

<!-- { "blockType": "request", "name": "get-shared-driveitem-expand-children" } -->

```http
GET https://graph.microsoft.com/beta/shares/{shareIdOrUrl}/driveItem?$expand=children
```

### <a name="response"></a><span data-ttu-id="f3a6c-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f3a6c-147">Response</span></span>

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

## <a name="remarks"></a><span data-ttu-id="f3a6c-148">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f3a6c-148">Remarks</span></span>

* <span data-ttu-id="f3a6c-149">Para OneDrive para la Empresa y SharePoint, la API de recursos compartidos siempre requiere autenticación y no puede usarse para tener acceso a contenido compartido de manera anónima sin un contexto de usuario.</span><span class="sxs-lookup"><span data-stu-id="f3a6c-149">For OneDrive for Business and SharePoint, the Shares API always requires authentication and cannot be used to access anonymously shared content without a user context.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "Access the contents of a sharing link with the OneDrive API.",
  "keywords": "shares,shared,sharing,share link, sharing link, share id, share token",
  "section": "documentation",
  "tocPath": "Sharing/Use a link"
} -->
