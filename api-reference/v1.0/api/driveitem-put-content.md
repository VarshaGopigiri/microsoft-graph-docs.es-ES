---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Cargar archivos pequeños
localization_priority: Priority
ms.openlocfilehash: d3a1b504ae50fb09b9776e3f1eb269894d5f1167
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860329"
---
# <a name="upload-or-replace-the-contents-of-a-driveitem"></a><span data-ttu-id="b9f99-102">Cargar o reemplazar el contenido de un objeto DriveItem</span><span class="sxs-lookup"><span data-stu-id="b9f99-102">Upload or replace the contents of a DriveItem</span></span>

<span data-ttu-id="b9f99-p101">La API de carga simple le permite proporcionar el contenido de un archivo nuevo o actualizar el contenido de un archivo existente en una sola llamada API. Este método solo admite archivos de hasta 4 MB de tamaño.</span><span class="sxs-lookup"><span data-stu-id="b9f99-p101">The simple upload API allows you to provide the contents of a new file or update the contents of an existing file in a single API call. This method only supports files up to 4MB in size.</span></span>

<span data-ttu-id="b9f99-105">Para cargar archivos grandes, consulte [Cargar archivos de gran tamaño con una sesión de carga](driveitem-createuploadsession.md).</span><span class="sxs-lookup"><span data-stu-id="b9f99-105">To upload large files see [Upload large files with an upload session](driveitem-createuploadsession.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="b9f99-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="b9f99-106">Permissions</span></span>

<span data-ttu-id="b9f99-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b9f99-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b9f99-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b9f99-109">Permission type</span></span>      | <span data-ttu-id="b9f99-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b9f99-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b9f99-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b9f99-111">Delegated (work or school account)</span></span> | <span data-ttu-id="b9f99-112">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b9f99-112">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="b9f99-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b9f99-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b9f99-114">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b9f99-114">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="b9f99-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b9f99-115">Application</span></span> | <span data-ttu-id="b9f99-116">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b9f99-116">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request-to-replace-an-existing-item"></a><span data-ttu-id="b9f99-117">Solicitud HTTP (para reemplazar un elemento existente)</span><span class="sxs-lookup"><span data-stu-id="b9f99-117">HTTP request (to replace an existing item)</span></span>

<!-- { "blockType": "ignored" } -->

```http
PUT /drives/{drive-id}/items/{item-id}/content
PUT /groups/{group-id}/drive/items/{item-id}/content
PUT /me/drive/items/{item-id}/content
PUT /sites/{site-id}/drive/items/{item-id}/content
PUT /users/{user-id}/drive/items/{item-id}/content
```

## <a name="http-request-to-upload-a-new-file"></a><span data-ttu-id="b9f99-118">Solicitud HTTP (para cargar un archivo nuevo)</span><span class="sxs-lookup"><span data-stu-id="b9f99-118">HTTP request (to upload a new file)</span></span>

<!-- { "blockType": "ignored" } -->

```http
PUT /drives/{drive-id}/items/{parent-id}:/{filename}:/content
PUT /groups/{group-id}/drive/items/{parent-id}:/{filename}:/content
PUT /me/drive/items/{parent-id}:/{filename}:/content
PUT /sites/{site-id}/drive/items/{parent-id}:/{filename}:/content
PUT /users/{user-id}/drive/items/{parent-id}:/{filename}:/content
```

## <a name="request-body"></a><span data-ttu-id="b9f99-119">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b9f99-119">Request body</span></span>

<span data-ttu-id="b9f99-120">El contenido del cuerpo de la solicitud debe ser la secuencia binaria del archivo que se cargará.</span><span class="sxs-lookup"><span data-stu-id="b9f99-120">The contents of the request body should be the binary stream of the file to be uploaded.</span></span>

## <a name="response"></a><span data-ttu-id="b9f99-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b9f99-121">Response</span></span>

<span data-ttu-id="b9f99-122">Si se ejecuta correctamente, este método devuelve un objeto [driveItem](../resources/driveitem.md) en el cuerpo de la respuesta del archivo que se ha creado o actualizado.</span><span class="sxs-lookup"><span data-stu-id="b9f99-122">If successful, this method returns a [driveItem](../resources/driveitem.md) object in the response body for the newly created or updated file.</span></span>

## <a name="example-upload-a-new-file"></a><span data-ttu-id="b9f99-123">Ejemplo (se carga un nuevo archivo)</span><span class="sxs-lookup"><span data-stu-id="b9f99-123">Example (upload a new file)</span></span>

<span data-ttu-id="b9f99-124">Este ejemplo carga la cadena "The contents of the file goes here." (El contenido del archivo va aquí.)</span><span class="sxs-lookup"><span data-stu-id="b9f99-124">This example uploads the string "The contents of the file goes here."</span></span> <span data-ttu-id="b9f99-125">en un archivo en la unidad del usuario que ha iniciado sesión en FolderA denominado FileB.txt.</span><span class="sxs-lookup"><span data-stu-id="b9f99-125">to a file in the signed-in user's drive under FolderA named FileB.txt.</span></span>

<!-- { "blockType": "request", "name": "upload-via-put", "scopes": "files.readwrite" } -->

```http
PUT /me/drive/root:/FolderA/FileB.txt:/content
Content-Type: text/plain

The contents of the file goes here.
```

### <a name="response"></a><span data-ttu-id="b9f99-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b9f99-126">Response</span></span>

<span data-ttu-id="b9f99-127">Si se ejecuta correctamente, este método devuelve un recurso [driveItem][item-resource] en el cuerpo de la respuesta del archivo que se ha creado.</span><span class="sxs-lookup"><span data-stu-id="b9f99-127">If successful, this method returns an [driveItem][item-resource] resource in the response body for the newly created file.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItem", "truncated": true } -->

```http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "id": "0123456789abc",
  "name": "FileB.txt",
  "size": 35,
  "file": { }
}
```

## <a name="example-updating-an-existing-file"></a><span data-ttu-id="b9f99-128">Ejemplo (actualizar un archivo existente)</span><span class="sxs-lookup"><span data-stu-id="b9f99-128">Example (updating an existing file)</span></span>

<span data-ttu-id="b9f99-129">Este ejemplo reemplaza el contenido de un archivo con un identificador conocido.</span><span class="sxs-lookup"><span data-stu-id="b9f99-129">This example replaces the contents of a file with a known ID.</span></span>

<!-- { "blockType": "request", "name": "upload-via-put-id", "scopes": "files.readwrite" } -->

```http
PUT /me/drive/items/{item-id}/content
Content-Type: text/plain

The contents of the file goes here.
```

### <a name="response"></a><span data-ttu-id="b9f99-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b9f99-130">Response</span></span>

<span data-ttu-id="b9f99-131">Si se ejecuta correctamente, este método devuelve un recurso [driveItem][item-resource] en el cuerpo de la respuesta del archivo que se ha creado.</span><span class="sxs-lookup"><span data-stu-id="b9f99-131">If successful, this method returns an [driveItem][item-resource] resource in the response body for the newly created file.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItem", "truncated": true } -->

```http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "id": "0123456789abc",
  "name": "FileB.txt",
  "size": 35,
  "file": { }
}
```

## <a name="error-responses"></a><span data-ttu-id="b9f99-132">Respuestas de error</span><span class="sxs-lookup"><span data-stu-id="b9f99-132">Error responses</span></span>

<span data-ttu-id="b9f99-133">Vea [Respuestas de error][error-response] para obtener los detalles sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="b9f99-133">See [Error Responses][error-response] for details about how errors are returned.</span></span>

[error-response]: /graph/errors
[item-resource]: ../resources/driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "Create a new file with content or update a file's content.",
  "keywords": "insert,upsert,update,upload",
  "section": "documentation"
} -->
